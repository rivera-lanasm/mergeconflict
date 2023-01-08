+++ 
draft = true
date = 2023-01-01T19:05:04-05:00
title = "Raspberry Pi Utility"
description = "command line tool for running RbPi Diagnostics"
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++


### Pi diagnostic commands, and other system utilities for seeing what is going on 

Now that we're interacting with the Pi via ssh, what routines does the OS offer to inform me about the health of my Pi. Unless it caught fire, at first glance, I'm not sure I'd be able to tell if something was wrong. 

So this is excluding the hardware alerts, which come in the form of the green and red LED lights on the Pi. Those are helpful, but pretty easily accessible and interpretable. [here](...)

First, [here](https://www.circuitbasics.com/useful-raspberry-pi-commands/) are some commonly used commands for file/directory, system information, and networking actions and retrievals. 

Here are a few I commonly use, mostly in lieu of interacting with the Pi in headless mode:
- cat /proc/meminfo
- df -h


package for everything



