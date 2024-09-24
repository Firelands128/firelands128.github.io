---
title: Configure Google Chrome Geolocation to enable platform location API
summary: Steps to configure Google Chrome Geolocation to enable platform location API
description: Steps to configure Google Chrome Geolocation to enable platform location API
categories: [Google Chrome]
tags: [Googe Chrome, Geolocation, Platform]
date: '2024-09-25T02:23:02+08:00'
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

## Problem
If you cannot get correct geolocation result from map website on Google Chrome, it may be because geolocation didn't enable operation system location API.

## Solution
Enter ```chrome://flags``` in address bar. There would show some experimental features.

![1](images/1.png)

Search ```geolocation``` on this page. \
Next, change setting ```Enable location provider manager for Geolocation API``` value to ```Enabled HybirdPlatform```.

![2](images/2.png)

Last, relaunch the Google Chrome, by pressing ```Relaunch``` button.

![3](images/3.png)

After the Google Chrome restarted, geolocation would using platform api to location on map website.