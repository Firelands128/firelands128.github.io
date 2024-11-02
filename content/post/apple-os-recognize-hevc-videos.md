---
title: 'How to make Apple OS Recognize HEVC Videos Using FFmpeg'
summary: 'Steps to make Apple OS Recognize HEVC Videos Using FFmpeg'
description: 'Steps to make Apple OS Recognize Hevc Videos Using FFmpeg'
categories: [FFmpeg]
tags: [FFmpeg, Apple, HEVC]
date: '2024-11-03T02:03:12+08:00'
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

### Background
HEVC (High Efficiency Video Coding), also known as H.265, is a video compression standard that, compared to it predecessor H.264, offers from 25 % to 50 % better data compression at the same level of video quality. Apple’s operating systems natively support HEVC since iOS 11 and macOS High Serria.
FFmpeg can create those files, however, a certain tag is needed for the files to be recognized by Apple software.


### Solution
Use the -tag:v hvc1 parameter in your FFmpeg command make your HEVC file work on Apple devices.

```shell
ffmpeg -i input.mp4 -tag:v hvc1 -c copy output.mp4
```