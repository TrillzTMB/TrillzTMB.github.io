---
title: 'Installing Visual Studio Code on a Galaxy Note 10+ '
categories:
  - Termux
  - Development
tags:
  - Termux
  - Galaxy Note 10+
  - Smart Phone
  - arm64
  - Android
  - DEX
  - Linux
  - LinuxOnDex
published: true
---

## Visual Studio Code on Arm64 Platform on Termux


This is for installing Visual Studio Code on my Galaxy Note 10+ within Termux/Debian Container

The Follwing site [VS Code for Arm64 architecture](https://code.headmelted.com/) has community build of Visual Studio Code and specifically arm64 versions in DEB, RPM packages.


Within your Debian shell install VSCode using following:
	
```bash
. <( wget -O - https://code.headmelted.com/installers/apt.sh )
```

then you can run Visual Studio Code in your desktop envrionment using
```bash
code-oss --user-data-dir="Path to Code settings folder"
```

  * Extensions work unless they are using x86 binaries
