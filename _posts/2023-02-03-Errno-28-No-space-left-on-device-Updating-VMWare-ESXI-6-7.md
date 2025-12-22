---
title: "[Errno 28] No space left on device - Updating VMWare ESXI 6.7"
date: 2023-02-03T13:43:00-04:00
categories:
  - System Administration
tags:
  - esxi
  - vmware
  - homelab
---

When updating VMWare ESXI 6.7, which runs my homelab, I always get the error "[Errno 28] No space left on device". But wait... There is enough space on the disk!

```
[root@esxi:~] esxcli software profile update -p ESXi-6.7.0-20220104001-standard -d https://hostupdate.vmware.com/software/VUM/PRODUCTION/main/vmw-depot-index.xml
 [InstallationError]
 [Errno 28] No space left on device
       vibs = VMware_locker_tools-light_11.3.5.18557794-18812553
 Please refer to the log file for more details.
[root@esxi:~]  [Errno 28] No space left on device
```

A quick search on the package name returned several articles addressing the same issue. It is a common issue with VMWare ESXI 6.7. To fix the issue, the package needs to be installed manually.

Let's begin by enabling HTTP Client in ESXI. The first step is pulling the latest version of the package from VMWare.com

```
[root@esxi:/tmp] esxcli network firewall ruleset set -e true -r httpClient
```

Now that the system has access to the internet, let's query VMWare's ESXI software repository for the package. The command below will list all "tool-light" packages available for download (older, current, and newer versions).  
Note: You could modify the grep command to filter out for Update only.

```
[root@esxi:~] esxcli software sources vib list --depot=https://hostupdate.vmware.com/software/VUM/PRODUCTION/main/vmw-depot-index.xml | grep tools-light | sort
```

![](/assets/images/2023/02/image-1024x107.png)

Pick the latest version of the "tools-light" package, download the package to ESXI's /tmp folder, and install the package manually.

```
[root@esxi:~] cd /tmp
[root@esxi:/tmp] wget http://hostupdate.vmware.com/software/VUM/PRODUCTION/main/esx/vmw/vib20/tools-light/VMware_locker_tools-light_11.3.5.18557794-19193900.vib
Connecting to hostupdate.vmware.com (184.31.3.90:80)
saving to 'VMware_locker_tools-light_11.3.5.18557794-19193900.vib'
VMware_locker_tools- 100% |************************************************************************|  177M  0:00:00 ETA
'VMware_locker_tools-light_11.3.5.18557794-19193900.vib' saved
[root@esxi:/tmp] esxcli software vib install -f -v /tmp/VMware_locker_tools-light_11.3.5.18557794-19193900.vib
Installation Result
   Message: Operation finished successfully.
   Reboot Required: false
   VIBs Installed: VMware_locker_tools-light_11.3.5.18557794-19193900
   VIBs Removed: VMware_locker_tools-light_11.2.5.17337674-17867351
   VIBs Skipped:
```

After the installation of 'tools-light' finishes successfully, re-run the ESXI profile update command again. It will take several minutes to run.

```
[root@esxi:/tmp] esxcli software profile update -p ESXi-6.7.0-20220104001-standard -d https://hostupdate.vmware.com/software/VUM/PRODUCTION/main/vmw-depot-index.xml
Update Result
   Message: The update completed successfully, but the system needs to be rebooted for the changes to be effective.
   Reboot Required: true
   VIBs Installed: VMW_bootbank_brcmfcoe_11.4.1078.26-14vmw.670.3.159.18828794,
...
   VIBs Removed: VMW_bootbank_brcmfcoe_11.4.1078.25-14vmw.670.3.73.14320388, 
...
 VIBs Skipped: VMW_bootbank_ata-libata-92_3.00.9.2-16vmw.670.0.0.8169922, 
...


```

For security reasons, disable the HTTP Client again, and then reboot the ESXI host  
Note: Remember to turn off VMs, set host to maintenance mode, or whatever steps are necessary in your environment.

```
[root@esxi:/tmp] esxcli network firewall ruleset set -e false -r httpClient
```

Verify the new Profile Name is being used by checking the ESXI Web Admin app.

![](/assets/images/2023/02/image-2.png)

Thanks for reading!