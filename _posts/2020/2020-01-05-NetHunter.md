---
title: Installing Kali Nethunter Rootless on Android Device
categories:
  - Android
  - Termux
  - LinuxOnDex
tags:
  - Termux
  - Galaxy Note 10+
  - arm64
  - Android
  - DEX
  - LinuxOnDex
published: true
toc: false
---

[Article Source](https://www.kali.org/docs/nethunter/nethunter-rootless/ "Article Source")

The Galaxy Note 10+ is a great phone, and it had a feature called Linux On Dex, which was consequently discontinued; 

This page outlines a process on setting up an envrionment that replicates Linux On Dex using Temux, and NetHunter on a Non Rooted Android Phone (specifically in this case a Galaxy Note10+)

###  -- Installation

1. Install NetHunter store app, [NetHunter Store](https://store.nethunter.com)
2. Within NetHunter Store 
  * **Install Termux**
  * **Install NetHunter-KeX Client** 
  * **Hacker's Keyboard** 

3. Open Termux and enter the following:
   ```bash
	termux-setup-storage
    pkg install wget
    wget -O install-nethunter-termux https://offs.ec/2MceZWr
    chmod +x install-nethunter-termux
    ./install-nethunter-termux
	```

###  -- Nethunter Command Line Options

Within the Termux CLI you can start or stop Kali Nethunter using one of :

Command | Result
------------ | -------------
nethunter | start Kali NetHunter command line interface
nethunter kex passwd | Configure the KeX password (only needed before 1st use)
nethunter kex & | start Kali NetHunter Desktop Experience
nethunter kex stop | stop Kali NetHunter Desktop Experience

###  -- What to Do First Run

1.Update and perform full install of Kali within Nethunter:
```bash
Nethunter
apt update && apt full-upgrade
apt install kali-linux-full
```   

2.Install Chromium, and remove Firefox (Firefox fails to run unless you have root):
```bash
apt remove firefox-esr
apt install chromium
```   
From within the Kali Desktop
```
Find the “Chromium Web Browser” item in the application menu
right click and select “Edit Application”
Change the “Command” to /usr/bin/chromium --no-sandbox %U
```  
  
