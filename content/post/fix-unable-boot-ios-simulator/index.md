---
title: Fix bug of unable to boot iOS simulator
summary: Steps to fix bug of unable to boot iOS simulator.
description: Steps to fix bug of unable to boot iOS simulator.
categories: [Simulator/Emulator]
tags: [iOS Simulator, boot]
date: '2024-03-24T17:26:45+08:00'
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

​		If you encounter the following exception when boot the iOS simulator:

![1](images/1.png)

​		Or:

![2](images/2.png)

​		You can try this```Mac --- > System Settings --- > Storage --- > Developer --- > Delete Xcode Caches```. And then restart the simulator, it may work fine.

![3](images/3.png)

![4](images/4.png)

![5](images/5.png)
