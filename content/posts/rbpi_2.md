+++ 
draft = true
date = 2023-01-01T14:07:52-05:00
title = "ARM Assembler, a shallow introduction"
description = "for the mildly curious"
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

### The computer processor, for the impatient

I feel like the impulse to understand how a CPU really works is more of a impulse curiosity. Unless you are working directly on system architecture related problems, you likely won't have to deliberate between the pros and cons of two processors. When I compare EC2 instance types, I'm usually focusing on memory, cores, network,.... Instance versions may have differences of processors, but after having sorted isntances by the factors I already mentioned, I rarely find need to add additional depth to that decision making. 

I don't really have a strong retort to this; however, I'll see if by the end of this post I will have changed my mind. 

### Ask the internet


First, as I only really care about CPU architecture insofar as it helps me compare two CPU models, I'll start with the performance measures commonly used. This is probably going to be very incomplete:
- ...


If you want some primers on how a CPU is organized, here are some good explainers I've come across. At its most basic, as I've understood it, the concepts that form what we understand as the CPU and its functions can be broken down as follow:
- ...

https://www.cs.utexas.edu/~lin/cs380p/Free_Lunch.pdf

### Assembly


If you're interested in a more in depth look at how Assembly language works on ARM, I would check [this guide by ...](https://thinkingeek.com/arm-assembler-raspberry-pi/). 

https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/os/introduction.html

https://helloworld.raspberrypi.org/articles/hw16-assembly-language-on-the-pi

https://opensource.com/article/20/10/arm6-assembly-language

### Example: Writing a simple calculator program

- also using Makefile
https://makefiletutorial.com/#running-the-examples

- directives
- put data after a .data directive and code after a .text. code vs data?

- If our processor were only able to work on registers it would be rather limited. memory 
- These two special operations, loading and store, are instructions on their own called usually load and store.
- Loading data from memory is a bit complicated because we need to talk about addresses.
- So after the first ldr, in r1 we have the real address of myvar1. But we do not want the address at all, but the contents of the memory at that address, thus we do a second ldr.
- example code 

- Now we can unveil their deep meaning: labels in the assembler are just symbolic names to addresses in your program.




The processor on the Raspberrypi 4 is Broadcom'S BCM2711, a quad-core Cortex-A72 64-bit CPU. You can read [here](http://sandsoftwaresound.net/raspberry-pi-4-arm-cortex-a72-processor/) for an in depth description of the improvements of this processor over earlier Raspberry Pi models. 


### Development Project
Docker service that 
- https://data.cityofnewyork.us/City-Government/Recent-Contract-Awards/qyyg-4tf5




