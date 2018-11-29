---
layout: post 
title: "Installing LineageOS" 
date: 2018-11-29
---
## Overview:  
Installing the OS now has 3 main parts (as far as I can tell)
1. Install recovery software - I am using TWRP
2. Install LineageOS and google apps

## Steps with references:   

####References:
1. Primary reference: https://wiki.lineageos.org/devices/shamu/install
2. https://dl.twrp.me/shamu/twrp-3.2.3-0-shamu.img.html
3. https://download.lineageos.org/shamu
4. https://wiki.lineageos.org/gapps.html

####Steps:
#####Installing Recovery Software: 
1. Connected nexus phone to computer and booted into fastboot mode  
Note that this seems to be a temp thing on my device
```$xslt
sudo ./fastboot devices
sudo ./fastboot flash recovery twrp-3.2.3-0-shamu.img
```
2. restart fastboot mode using reboot option then start recovery mode
3. Backup the device's default stuff by following the instructions in TWRP

#####Installing LineageOS and google apps:
From the TWRP recovery screen, I followed these steps 
(several of these are taken directly from first reference):
1. From third link, download the lineageos file. 
2. https://wiki.lineageos.org/devices/shamu/install#installing-lineageos-from-recovery
  

## Conclusion:
I was able to successfully boot into lineageOS and the initial use 
    appears to be many times better than the previous default installation
    (no more 2 second delay on typing vibrations!).