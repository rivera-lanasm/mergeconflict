+++ 
draft = true
date = 2023-04-08T00:18:52-04:00
title = "Setting Up Raspberry Pi 4"
description = "An Indoor Cloud"
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

### The Internet is as large as you imagine


### Setup 

**Setting Up MicroSD Card**
- I just followed the official [documentation](https://www.raspberrypi.com/documentation/computers/getting-started.html#sd-cards) to set up Raspberry Pi [OS](https://www.raspberrypi.com/software/) on a 32 GB SD cards
- Once connected, the [raspi-config](https://www.raspberrypi.com/documentation/computers/configuration.html#the-raspi-config-tool) tool is great for updating other system settings

**SSH into Raspberry Pi**
- I set up my Raspberry Pi with network credentials to my local wifi network, so I can discover the server's IP address using this command from my laptop, `ping HOSTNAME.local`

**I have a second Raspberry Pi and need to change Hostname on the first**
- edit hostname under following files on root file system  
    - `/etc/hostname/`
    - `/etc/hosts`
- Upon reboot, you can verify your hostname on your Raspberry Pi with the `hostname` command

### Pi diagnostic commands, and other system utilities for seeing what is going on 

Now that we're interacting with the Pi via ssh, what routines does the OS offer to inform me about the health of my Pi? 

This is aside from the hardware alerts, which come in the form of the green and red LED lights on the Pi. Those are helpful, but pretty easily accessible and interpretable. [here](...)

Raspberry Pi Monitoring Clock Frequency, Voltage and Temperature:
- vcgencmd measure_temp

Process Management:
- htop


### SystemCtl process for recording diagnostics 

- create bash script recording data, chmod x it 
- create new systemd service file under /etc/systemd/system/
- add new service to system d: 
    - sudo nano /etc/systemd/system/temp_monitor.service
    - Save and close the service file.
    - Enable the service to start automatically at boot time by running the following command:
    - sudo systemctl enable temp_monitor.service --> enable service 
    - sudo systemctl start temp_monitor.service --> start service 
    - systemctl list-units --type=service --state=active | grep -i temp
    - systemctl status temp_monitor



### Diagnostic Dashboard Setup

package for everything



### Development Project
Docker service that 
- https://data.cityofnewyork.us/City-Government/Recent-Contract-Awards/qyyg-4tf5


### References 






