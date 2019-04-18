---
layout: content
title: Installation
permalink: /installation/
---

We currently provide Nexus 5X image file applying ExLL Congestion Control patchs on its kernel.
We also provide sender(Ubuntu Desktop) & receiver(Nexus 5X) application to evaluate ExLL's performance on real world LTE environment.  
 
Download links are:
- [Nexus 5X image and tools](https://unistackr0-my.sharepoint.com/:u:/g/personal/sipark_unist_ac_kr1/ESL_Qysjfk1Il5jSJB2n5iMBAUhij9RmYLAdgFeQPZgAVw?e=GmXFj5)
  (includes twrp and SuperSU)  
- [Sender application](https://unistackr0-my.sharepoint.com/:u:/g/personal/sipark_unist_ac_kr1/EfHgObOqKxBAlSNz_Oj-C-QBWHQX_GhklcG1AnJzqCZFFA?e=Yhhvlm)  
- [Receiver application](https://unistackr0-my.sharepoint.com/:u:/g/personal/sipark_unist_ac_kr1/EUqiE_IWqbxPn0CHnsXVIpUBEwLXasgxh_h3wupG_tMaOw?e=P56WUe)  
   
# Installation Guide  
 
 
## Ubuntu Sender  
 
  - Download & Install Ubuntu 16.04 LTS .iso file at http://www.ubuntu.com/download/desktop.  
 
  
  - Install sender application using upper link and compile.  
 
  
  - Sender-side preparation is done.  
 
  
 
## Nexus 5X Receiver  
 
  - Downliad Nexus 5X image and tools at Ubuntu PC using upper link and connect Nexus 5X device via USB.  
 
  - Flash Nexus 5X image.  
  
  
    ```
    # adb reboot-bootloader
    # fastboot oem unlock
    # cd /your-path/bullhead-opm2.171019.029/
    # ./flash-all.sh
    ```  
 
  - Install twrp recovery.  
 
  
    ```
    # adb reboot-bootloader    
    # fastboot flash recovery twrp-3.2.1-0-bullhead.img
    ```  
  
  - Boot Nexus 5X as recovery mode.  
  
  - Give Nexus 5X a root privilege.  
 
  
    ```
    # adb push SR5-SuperSU-v2.82-SR5-20171001224502.zip /sdcard/
    ```  
    
  - Install SuperSU in your device through recovery and reboot.  
  
  - Install receiver application using apk file.  
 
  - Receiver-side preparation is done.  
 
 
# Execution Guide  
 
 
## Ubuntu Sender  
 
  - Execute shell script at sender-side.  
 
    ```
    # ./start.sh
    ```  
    
  - After one test run, you should execute another shell script.
    ```
    # ./stop.sh
    ```  
  
 
## Nexus 5X Receiver  
 
  - Launch receiving application.  
 
  - Set ExLL related parameters.  
 
      `alpha: constant value in ExLL control formula. In the paper, we use 100 as a default value.`  
 
      `gamma: 10x value of parameter gamma. In the paper, we use 0.5(in the app, 5) as a default value`  
 
      `rttmin_gain: Minimum RTT Compensation value. This value is simply added to calculated minimum RTT. Default value is 10 ms.`  
 
      `You can activate ExLL TCP by checking TCP_ExLL checkbox.`  
 
      `If you check Multi_Flow checkbox, you could test three flow test.`  
 
      `AUTOMATED TEST & Uplink is currently depreciated.`  
 
  - Push RUN ONE-TIME TEST button to test.      
 
