---
title: How to modify PVE VM ID
summary: Read about how to modify PVE VM ID
description: Read about how to modify PVE VM ID
categories: [PVE]
tags: [PVE, VM, ID]
date: '2024-08-19T22:16:48+08:00'
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

# Modify PVE VM ID
If we want to modify PVE VM ID, the following steps would be helpful.
#### Steps
* Close the VM that you want to change ID
* Open Terminal and ssh to PVE
* Change directory into ```/etc/pve/nodes/```
* Get into node directory, which name is PVE node name
* Get into ```qemu-server``` directory, if you are changing LXC container id, go to lxc directory
* Rename the original configuration file to destination ID
* Edit this configuration file and modify disk file path. Two places totally
* Edit the configuration file and modify the directory where the disk file is stored (2 in total)
* Change directory into ```/var/lib/vz/images```
* Rename the directory to destination ID
* Rename disk file to destinationo ID
* Refresh web page, and start VM


### Reference
* https://blog.kuretru.com/posts/40c861d5/
