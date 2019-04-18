---
layout: content
title: Installation
permalink: /installation/
---

We currently provide Nexus 5X image file applying ExLL Congestion Control patchs on its kernel.
We also provide sender(Ubuntu Desktop) & receiver(Nexus 5X) application to evaluate ExLL's performance on real world LTE environment.

Download links are:
- [Nexus 5X image and tools]()
  (includes twrp and SuperSU)
- [Sender application]()
- [Receiver application]()
 </br>
# Installation Guide
 </br>
 </br>
1. Ubuntu Sender
</br>
  - Download & Install Ubuntu 16.04 LTS .iso file at http://www.ubuntu.com/download/desktop
</br>  
  - Install sender application using upper link and compile.
</br>  
  - Sender-side preparation is done.
</br>  
</br>    
2. Nexus 5X Receiver
</br>
  - Downliad Nexus 5X image and tools at Ubuntu PC using upper link and connect Nexus 5X device via USB.
</br>  
  - Flash Nexus 5X image.
</br>
    `# adb reboot-bootloader`
</br>    
    `# fastboot oem unlock`
</br>    
    `# cd /your-path/bullhead-opm2.171019.029/`
</br>    
    `# ./flash-all.sh`
</br>    
  - Install twrp recovery.
</br>  
    `# adb reboot-bootloader`
</br>    
    `# fastboot flash recovery twrp-3.2.1-0-bullhead.img`
</br>    
  - Boot Nexus 5X as recovery mode.    
</br>    
  - Give Nexus 5X a root privilege.
</br>  
    `# adb push SR5-SuperSU-v2.82-SR5-20171001224502.zip /sdcard/`
</br>  
    `Install SuperSU in your device through recovery and reboot`
</br>    
  - Install receiver application using apk file.
</br>  
  - Receiver-side preparation is done.
</br>    
</br>    
# Execution Guide
</br>
</br>
1. Ubuntu Sender
</br>
  - Execute shell script at sender-side.
</br>  
    `# ./start.sh`
</br>    
</br>  
2. Nexus 5X Receiver
</br>
  - Launch receiving application.
</br>  
  - Set ExLL related parameters.
</br>  
      `alpha: constant value in ExLL control formula. In the paper, we use 100 as a default value.`
</br>      
      `gamma: 10x value of parameter gamma. In the paper, we use 0.5(in the app, 5) as a default value`
</br>      
      `rttmin_gain: Minimum RTT Compensation value. This value is simply added to calculated minimum RTT. Default value is 10 ms.`
</br>      
      `You can activate ExLL TCP by checking TCP_ExLL checkbox.`
</br>      
      `If you check Multi_Flow checkbox, you could test three flow test.`
</br>      
      `AUTOMATED TEST & Uplink is currently depreciated.`
</br>      
  - Push RUN ONE-TIME TEST button to test.      
</br>
