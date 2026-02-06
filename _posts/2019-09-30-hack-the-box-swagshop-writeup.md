---
title: 'Hack The Box - Swagshop Writeup'
date: '2019-09-30T20:58:24-04:00'
categories:
    - 'Hack The Box'
tags:
    - hackthebox
    - ctf
    - writeups
---

## Content

- Information
- Reconnaissance and Scanning
- Initial Access Execution
- User
- Privilege Escalation
- Root Privilege Escalation
- Cleanup

## Information

- Target OS: Linux
- IP: 10.10.10.140
- Owned on: 09/24/2019

## Reconnaissance and Scanning

I started conducting basic enumeration on the target.

```
     root@kali:~# nmap -A -sC -sV 10.10.10.140
     Starting Nmap 7.80 ( https://nmap.org ) at 2019-09-26 13:56 EDT
     Nmap scan report for 10.10.10.140
     Host is up (0.12s latency).
     Not shown: 998 closed ports
     PORT   STATE SERVICE VERSION
     22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu
     Linux; protocol 2.0)
     | ssh-hostkey:
     |   2048 b6:55:2b:d2:4e:8f:a3:81:72:61:37:9a:12:f6:24:ec (RSA)
     |   256 2e:30:00:7a:92:f0:89:30:59:c1:77:56:ad:51:c0:ba (ECDSA)
     |_  256 4c:50:d5:f2:70:c5:fd:c4:b2:f0:bc:42:20:32:64:34 (ED25519)
     80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
     |_http-server-header: Apache/2.4.18 (Ubuntu)
     |_http-title: Home page
     No exact OS matches for host (If you know what OS is running on
     it, see https://nmap.org/submit/ ).
     ...
```

Awesome! SSH and HTTP services are available. After a bit of password guessing attacks, nothing fruitful over SSH. Let’s move on to the HTTP service, starting with *dirbuster* the server. While that is running, let’s visit the website.

![](/assets/images/2019/09/image.png)

I encountered *Magento*, an e-commence webapp. Poking for SQL Injection on the search fields, login boxes, but nothing worked. Let’s look at what *dirbuster* discovered.

![](/asset/2019/09/image-1.png)

In these directories, I encountered installation scripts that wouldn’t run and a *config.xml* containing credentials and an encryption key but we don’t know the algorithm used. However, I found the version of *Magento* at *http://10.10.10.140/RELEASE\_NOTES.txt*. Next, I searched for exploits available at <https://www.exploit-db.com> using *searchsploit*.

```
root@kali:~# searchsploit magento
 ---------------------------------- ----------------------------------------
  Exploit Title                    |  Path
                                   | (/usr/share/exploitdb/)
 ---------------------------------- ----------------------------------------
 …
 Magento eCommerce - Remote Code E | exploits/xml/webapps/37977.py
 …
```

## Initial Access &amp; Execution

Found a RCE exploit python script, which I modified to work on the target and changed the default credentials to prevent conflicting with others using the same exploit. Let's run the exploit… And we got admin credentials!

![](/assets/images/2019/09/image-2.png)
```
root@kali:~# python 37977.py 
 WORKED
```

I used the new credentials at the *Admin Dashboard* @ *http://10.10.10.140/admin* with the credentials *hax:hax*

![](/assets/images/2019/09/image-3.png)

Inside the Admin section, I started looking for vulnerable areas where I could open a shell session with the host, added my own php backdoor code into one of the pages but *Magento* comments them out, preventing them from running. What I found of interest is that I could edit an existing *Product* from the *Catalog* and allow custom file uploads from a customer. I will use this to upload my custom php backdoor.

![](/assets/images/2019/09/image-4.png)

I visited the homepage again, and selected the *Product* that allows file uploads. I configured my reverse shell php payload with my IP address. Once again, changed default port number, avoided common ports, and low/restricted ports.

![](/assets/images/2019/09/image-5.png)

![](/assets/images/2019/09/image-6.png)

I have now uploaded the payload and started looking for the php payload file in the directories *dirbuster* discovered. Found it under */media*, and clicked on the link to execute the payload on the host. Now, I have a shell.

![](/assets/images/2019/09/image-7.png)

![](/assets/images/2019/09/image-8.png)

## User Privilege Escalation

Got a shell running as *www-data*. I checked the history to see if there is anything interesting but history file variable was unset. Then, I ran “sudo -l” to see if I have sudo rights, and I find that I can run “*sudo /usr/bin/vi /opt/bitnami/wordpress/test.html*” without being prompted for credentials. This will be useful to get the root flag, let’s begin with getting user.

I proceed to navigate to the */home/haris/* directory and *cat flag.txt*.

```
$ cat user.txt
 a448877277e82f05e5ddf9f90aefbac8
```

## Root Privilege Escalation

Next, I used the command “*sudo /usr/bin/vi /opt/bitnami/wordpress/test.html*” to get a *vi* session as root. *vi* allows to execute command from its command-mode. Because *vi* is running as root, we can execute commands with root privileges.

```
 :!cat /root/root.txt
 c2b087d66e14a652a3b86a130ac56721
 

    ___ ___
  /| |/|\| |\
 /_| ´ |.` |_\           We are open! (Almost)
   |   |.  |
   |   |.  |         Join the beta HTB Swag Store!
   |___|.__|       https://hackthebox.store/password
 

                    PS: Use root flag as password!
```

We got root!

## Cleanup

Lastly, I cleaned all the files uploaded and revert changes done to the system to leave little to no evidence that I was there (and avoid other players from piggybacking from my work).