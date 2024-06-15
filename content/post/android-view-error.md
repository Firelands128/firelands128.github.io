---
title: How to fix Android View(SurfaceView and TextureView) Error
summary: Read about how to fix Android View(SurfaceView and TextureView) Error
description: Read about how to fix Android View(SurfaceView and TextureView) Error
categories: [Android]
tags: [Android, SurfaceView, TextureView]
date: '2024-06-16T02:40:31+08:00'
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
If the code is getting the below error:
```bash
E/BufferQueueProducer(15428): [SurfaceTexture-0-15428-0] connect: already connected (cur=1 req=1)
```

## Solution
You can try to change ```SurfaceView``` to ```TextureView```.