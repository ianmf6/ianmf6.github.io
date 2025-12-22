---
title: "Verify if a media device or file is bootable"
date: 2022-08-25T21:21:00-04:00
categories:
  - Linux
tags:
  - linux
---

To verify if a removable media (e.g. USB, DVD, or ISO) is bootable, you could use file tool on Linux systems. The command `file -s /path/to/media` reads block special files, such as partitions, and outputs the information.

To test this, I inserted RHEL 8.2 Installation ISO as a disk in a VM. The device path is `/dev/sr0`. Once I verified the disk is accessible, I ran `file -s /dev/sr0`. The output for RHEL Installation ISO shows the disk as a DOS / Master Boot Record partition, meaning it is a bootable media. For the second test, I used a Windows 10 Installation ISO. The output shows the media is a CD-ROM filesystem that is bootable.

An observation: Notice the Windows media output states the media is bootable, unlike the Linux media, that only shows partition information.

![](/assets/images/2022/08/image-1.png)

Screenshot

References:

[file(1) - Linux manual page (man7.org)](https://www.man7.org/linux/man-pages/man1/file.1.html)