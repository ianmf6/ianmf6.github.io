---
title: 'pfSense and Verizon FiOS'
date: '2020-02-17T17:03:55-05:00'
categories:
    - Networking
    - Homelab
tags:
    - fios
    - moca
    - pfsense
    - verizon
    - homelab
---

I have a small homelab setup at home that I use to practice cyber ninja skills and test new technology. My homelab consist of a refurbished HP Z420 Workstation with 64 GB RAM and over 2 TB of SSD storage used as a server. The server is running VMware ESXI 6.7, which hosts several VMs. One of the VMs is pfSense and has a 2 NIC adapter assigned for LAN and WAN. I also have Verizon’s FiOS G1100 router that I use for its MoCA support (Video On Demand, DVR, Caller ID, etc). However, I do not need it any of its other functionalities.

## Network Layout

![](/assets/images/2020/02/image-5-1024x364.png)

## Configuration

The first thing I configured was pfSense to work as a router between WAN and LAN. The connection between the ONT and my server is ethernet which is plugged in to one of the 2-port NIC. I had no issue receiving an IP address assigned by Verizon. However, I have read instances where clients had to clone Verizon router’s MAC address to retrieve an IP address. The second port goes to a TP-Link unmanaged switch that works as the main switching device for my entire house (Wireless AP, Printers, PlayStation, etc). After running the initial pfSense setup, a working network with access to the internet should be available.

Next step is to configure Verizon’s router. The router is connected to the main switch via the router’s WAN interface. The WAN interface should be configured for a Static/Manual IP address or create a static IP/MAC assignment via pfSense’s DHCP server module. Because ports will be forwarded to Verizon’s router, it is important that its IP do not change. Additionally, Verizon’s router LAN needs to be configured to use a different private network than pfSense’s LAN. For example, pfSense LAN could have 10.0.0.0/8 network and Verizon router LAN could have 192.168.1.1/24 network. In the Network configuration’s Network (Home/Office) section, the privacy setting should be disabled (see image below). If privacy setting is enabled, the Set-Top Box will be unable to access the internet and features such as On Demand and Interactive Guide will not work. Lastly, I disabled the router’s WiFi to avoid radio-waves congestion because I use another Wireless AP device.

![](/assets/images/2020/02/image-1024x509.png)

Now that Verizon’s router has an IP assigned, I am back to the pfSense web console. I configured port forwarding in pfSense to allow the necessary connectivity for VOD, DVR, Caller ID to work. A list of required ports can be viewed in the router’s Firewall – Port Forwarding section (see image below). pfSense’s port forwarding rules (pfSense -&gt; Firewall -&gt; NAT) are:

- TCP
    - 4567 (used by Verizon to push firmware upgrades to the router and other Verizon FiOS services)
    - 35000 (used by the primary Set-Top Box)
    - 35001-35013 (Optional. +1 Used for additional Set-Top Boxes)
- UDP
    - 63145 (used by the primary Set-Top Box)
    - 63146-63149 (Optional. +1 Used for additional Set-Top Boxes).

![Verizon Router Firewall – Port Forwarding automatically created rules.](/assets/images/2020/02/image-1-1024x492.png)
![pfSense Firewall – Port Forwarding rules](/assets/images/2020/02/image-6-1024x258.png)

The setup is now complete. A hard reboot on the Set-Top Boxes and Verizon router should automatically configure themselves with the network changes. TV, VOD, Interactive Guide, and Caller-ID should be functioning. If not, I have ran into the issue where Verizon router retains previous network routes from the previous configuration. The routes can be deleted via Verizon router Web interface -&gt; Advanced -&gt; Routing -&gt; Routing.

## References

- <http://www.dslreports.com/faq/verizonfios>
- [https://www.reddit.com/r/PFSENSE/comments/4ydgs4/pfsense\_and\_verizon\_fios\_router/](https://www.reddit.com/r/PFSENSE/comments/4ydgs4/pfsense_and_verizon_fios_router/)
- <https://www.pfsense.org/>

If it didn’t work for you, leave a comment.