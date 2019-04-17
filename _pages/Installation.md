---
layout: content
title: Installation
permalink: /installation/
---

We currently provide Nexus 5X image file applying ExLL Congestion Control patchs on its kernel.
We also provide sender(Ubuntu Desktop) & receiver(Nexus 5X) application to evaluate ExLL's performance on real world LTE environment.

Download links are:
- [Nexus 5X image and tools]()
  includes twrp and SuperSU
- [Sender application]()
- [Receiver application]()

# Installation Guide
1. Ubuntu Server
  - Download & Install Ubuntu 16.04 LTS .iso file at http://www.ubuntu.com/download/desktop
  - Install sender application using upper link and compile.
  - Server-side preparation is done.
  
2. Nexus 5X Receiver
  - Downliad Nexus 5X image and tools at Ubuntu PC using upper link and connect Nexus 5X device via USB.
  - Flash Nexus 5X image.
    '# adb reboot-bootloader
    '# fastboot oem unlock
    '# cd /your-path/bullhead-opm2.171019.029/
    '# ./flash-all.sh

# Execution Guide
- 

