---
layout: post 
title: "Jekyll on Windows" 
date: 2018-08-24
---
## Overview:  
I want to install Jekyll on my machine as a step in setting up a local env for development of my github website.  
 Jekyll appears to be a webserver used to deploy apps built with Ruby 
 (I think this is akin to Tomcat and Maven in a Java stack)  

## Steps with references:   
Enabling linux subsystem on windows: https://docs.microsoft.com/en-us/windows/wsl/install-win10  
Verifying ubuntu version (18.04): https://www.hostingadvice.com/how-to/ubuntu-show-version/  
```$xslt
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install make build-essential
sudo apt-get install ruby ruby-dev
export GEM_HOME=$HOME/gems
export PATH=$HOME/gems/bin:$PATH
source ~/.bashrc
gem install bundler
gem install jekyll
```

## Conclusion:
Jekyll is now installed. Next, I will learn to use Ruby and Jekyll to build and run my website locally for local 
testing before deploying code in the future. 