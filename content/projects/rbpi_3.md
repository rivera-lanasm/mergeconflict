+++ 
draft = false
date = 2023-01-01T19:05:04-05:00
title = "SBCMeter: Time series System Monitor for Linux"
description = "Track system resource utlization for SBC's hosting sensitive applications"
slug = ""
authors = []
tags = ["sbc"]
categories = []
externalLink = ""
series = []
+++

### Hosting sensitive applications on self hosted SBC's

Linux tools like `htop`, `du`, and `ps` monitor system and process status and resource utilization at a point in time. This project provides a convenient tool set and user interface for collecting and visualizing longitudinal data at the system and process level for measures such as CPU utilization, hardware temperature, as well as user defined metrics. 

The tool provides a CLI entry point written in **bash**, uses **systemd** to set up and configure data collecting services, and **Flask/D3/JQuery** for web dashboard visualizing metrics.  

Principles embedded in development ("I" the user):
- I am not a web developer and do not want to spend time mired in the shifting landscape of front end development, so will only use tried/tested/stable web development tools
- I would like to interact with the tool as much as possible through the CLI, and the CLI should be as helpful as possible. See [here](https://clig.dev/)

For anyone hosting applications on SBC's, this tool can be used to:
- Measure and analyze a process's resource consumption patterns over time
- Anticipate and handle resource utilization limit breaches for processes sensitive to downtime

You can see project Github repo [here]() and project feature roadmap [here]()



