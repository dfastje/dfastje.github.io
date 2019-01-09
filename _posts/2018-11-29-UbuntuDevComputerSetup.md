---
layout: post 
title: "Setting Up Dev Machine Running Ubuntu" 
date: 2018-1-08
---
## Overview:  
I am tired of switching cords between my desktop and my laptop whenever I want to do any programming,
 so I am finally configuring the ubuntu OS on the desktop for dev work. For background, one of the first
 things that I did after leaving Capital One was to install Ubuntu on all of my devices. Reasons aside,
 I am now much more comfortable working with a linux based machine for development (truthfully, there
 wasn't that much of a learning curve and it removes a lot of the frustrations of windows!). As the OS
 is already installed, I will not be covering anything about the OS installation process. 

1. Install OS (not discussed)
2. Install Chrome
3. Install git
4. Install IntelliJ 
5. Install Java
6. Install Maven

## Steps with references:   

#### 2. Install Chrome
1. For installation, I download it through google's website (https://www.google.com/chrome/) rather than
 the ubuntu software store and then just followed the prompts. 
2. For usage, I am very fond of the chrome profiles based on separate accounts for different tasks. 
    
    A. Click on profile icon -> Manage people -> Add person -> Input name and click Add

#### 3. Install git
From the command prompt, enter the installation command:
```$xslt
sudo apt install git
git --version
```
###### References
I wanted to know what the -y modifier often seen in apt does because I see it commonly, but this was
 surprisingly hard to find out: https://www.computerhope.com/unix/apt.htm

#### 4. Install IntelliJ
This can be done by going through the Ubuntu Software Store. I am using IntelliJ Ultimate and 
 it is very much worth the license fee! 

#### 5. Install Java 8
I typically use the open JDK for personal use, but most organizations use the oracle JDK (for now!).

```$xslt
sudo apt install openjdk-8-jdk
java -version
```

###### References
I always look up these repos to be sure that I have the names right: 
 https://linuxconfig.org/how-to-install-java-on-ubuntu-18-04-bionic-beaver-linux

#### 6. Install Apache Maven
For this one, ubuntu will actually provide the proper command for you if you type "mvn -version"
 into the command prompt. 
 
 ```$xslt
sudo apt install maven
mvn -version
 ```


## Conclusion: 
There are many other things that can be done to setup the computer, but this will get you started with
 java development! Also, that was incredibly easy compared to the process on Windows!  