---
title: "A Comprehensive Guide to Securing SSH on Ubuntu 22.04"
date: 2023-07-23T12:16:00-04:00
categories:
  - Linux
tags:
  - cybersecurity
  - linux
  - ssh
---

SSH (Secure Shell) is a widely used protocol for securely accessing remote servers. However, its popularity also makes it a target for potential attackers. To ensure the safety of your Ubuntu 22.04 server, it is crucial to implement robust security measures for SSH. In this article, we will discuss essential steps to secure SSH on Ubuntu 22.04, safeguarding your server from unauthorized access and potential security breaches.

1.  Update and Upgrade:  
    Before diving into SSH security configurations, ensure your Ubuntu system is up-to-date. Use the following commands to update the package list and upgrade installed packages:

```
sudo apt update
sudo apt upgrade
```

2.  Disable Root Login:  
    By default, SSH allows the root user to log in directly. Disable this to minimize the risk of brute force attacks. Edit the SSH configuration file using a text editor like nano or vim:

```
sudo nano /etc/ssh/sshd_config
```

Locate the line containing `PermitRootLogin` and set it to `no`:

```
PermitRootLogin no
```

Save the file and restart the SSH service:

```
sudo service ssh restart
```

3.  Use SSH Key Authentication:  
    Instead of relying on passwords, implement SSH key authentication for increased security. Generate an SSH key pair on your local machine:

```
ssh-keygen
```

Copy the public key to the remote server using ssh-copy-id:

```
ssh-copy-id user@your_server_ip
```

Once the key is copied, disable password-based authentication in the SSH configuration file:

```
PasswordAuthentication no
```

Restart the SSH service again:

```
sudo service ssh restart
```

4.  Limit User Access:  
    Restrict SSH access to specific users or user groups only. This minimizes the number of potential entry points for attackers. Edit the SSH configuration file:

```
sudo nano /etc/ssh/sshd_config
```

Add the following line to allow access for specific users or groups:

```
AllowUsers user1 user2
```

Save the file and restart the SSH service.

5.  Use SSH Configurations for Increased Security:  
    Within the SSH configuration file, you can implement additional security measures:

-   Set a specific SSH port (avoid using the default port 22) by changing the `Port` option.
-   Use a specific IP address to bind SSH to, limiting access to only that IP using the `ListenAddress` option.
-   Implement an idle session timeout to automatically disconnect inactive SSH sessions by setting the `ClientAliveInterval` and `ClientAliveCountMax` options.

5.  Use Fail2ban:  
    Install and configure Fail2ban, a tool that scans log files and bans IP addresses with too many failed login attempts. Install Fail2ban using apt:

```
sudo apt install fail2ban
```

Configure Fail2ban by creating a new local configuration file:

```
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local
sudo nano /etc/fail2ban/jail.local
```

Adjust the `maxretry` and `bantime` values according to your needs. Save the file and restart Fail2ban:

```
sudo service fail2ban restart
```

Securing SSH on Ubuntu 22.04 is crucial to protect your server from potential threats and unauthorized access. By following the steps outlined in this guide, you can significantly enhance your SSH security and ensure a safer environment for your remote server operations. Remember to regularly update your system and stay informed about the latest security best practices to maintain a secure and reliable SSH setup.