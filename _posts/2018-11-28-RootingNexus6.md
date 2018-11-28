---
layout: post 
title: "Rooting Nexus 6" 
date: 2018-11-28
---
## Overview:  
Working on upgrading the OS of my old Nexus 6 phone currently running android 7.1.1  

This post will be about unlocking the bootloader.  

## Steps with references:   

####Disclaimers:
First, I just followed the steps in this youtube video, 
    so all credit goes to wwjoshdew: https://www.youtube.com/watch?v=IEjynlQgJCI
 
Second, I have been learning to develop android apps recently
    (without blogging about it ... because I use intelliJ for my blog) 
    so I already have the android SDK installed on my machine. 
     
Third, because the youtube video is pretty good quality, 
    I am just going to briefly outline the steps rather than give in-depth descriptions
####Steps:
1. Backup everything on the device I didn't want to lose
2. Enable developer options by clicking on the "Build number" field multiple times.
    The path on my pixel xl phone is Settings -> System -> About phone
3. Enable OEM unlocking and usb debugging
4. Shutoff the device
5. Enter the bootloader by pressing the down volume button and the power button
6. Connect the phone to a computer with the android SDK on it. 
7. Navigate to the platform-tools folder (for me "~/Android/Sdk/platform-tools") in terminal
8. Verify device is connected by running "./fastboot devices" in terminal
9. Unlock device by running "./fastboot oem unlock" and confirm all of the security questions
10. DEBUG! For me, the terminal responded with 
    "Failed() /n Finished. Total time: 76.411s" 
    but the phone was reset and unlocked properly
  

## Conclusion:
I was able to successfully unlock the device 
    and will now be researching how to change out the OS!