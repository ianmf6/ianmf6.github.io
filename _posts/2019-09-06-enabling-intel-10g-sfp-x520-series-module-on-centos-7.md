---
title: 'Enabling Intel 10G SFP+ X520 Series module on Centos 7'
date: '2019-09-06T21:18:45-04:00'
categories:
    - Linux
tags:
    - centos
    - kernel
    - linux
    - sfp
    - troubleshooting
---

By default, Centos 7 doesn’t support Intel’s 10G SFP+ X520 module. When you look at the **dmesg**  you find the following error: **“failed to load because an unsupported SFP+ or QSFP module type was detected.”** The workaround is to allow unsupported SFP modules in the kernel by enabling **ixgbe** kernel module. Let’s start by editing **/etc/default/grub** file and   
change the line :

```
GRUB_CMDLINE_LINUX=""
```

to

```
GRUB_CMDLINE_LINUX=" ixgbe.allow_unsupported_sfp=1" 
# note the space between " and ixgbe.
```

Now, we create the new **grub** configuration with the new option.

```
cp /boot/grub2/grub.cfg /boot/grub2/grub.cfg.bak
grub2-mkconfig -o /boot/grub2/grub.cfg
```

Next, the configuration file for the **ixgbe** kernel module must be created with the option to allow unsupported SFP. The file should not already exist. The one-liner command is:

```
echo "options ixgbe allow_unsupported_sfp=1" > /etc/modprobe.d/ixgbe.conf
```

The last step is to regenerate the **initrd image** with the new kernel configuration and reboot.

```
dracut --regenerate-all --force
reboot
```

After the reboot, the SFP should be recognized and ready for use.