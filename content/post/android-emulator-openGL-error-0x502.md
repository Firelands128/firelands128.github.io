---
title: How to fix Android Emulator OpenGL Error 0x502
summary: Read about how to fix Android Emulator OpenGL Error 0x502
description: Read about how to fix Android Emulator OpenGL Error 0x502
categories: [Android]
tags: [Android, Emulator, OpenGL]
date: '2024-06-15T21:36:22+08:00'
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
If the code is working fine on Android real device but not working on Android Emulator. For example, getting the below error:
```bash
E/emuglGLESv2_enc( 4288): device/generic/goldfish-opengl/system/GLESv2_enc/GL2Encoder.cpp:s_glGetUniformLocation:2206 GL error 0x502
```

## Solution
Downgrade the Android Emulator version to ```34.2.13```, which is the latest stable version that don't throw the error.

#### How to manually install a specified version of Android Emulator
To manually install a specified version of Android Emulator on Android Studio, you need to paste the desired emulator package contents into your SDK installation directory, and change the emulator version specified in the package.xml file. Specifically, follow these steps:

1. Locate your SDK installation directory. The default location of this directory varies by platform:
* On Windows, it's the ```%LocalAppData%\Android\Sdk``` directory. This normally expands to ```C:\Users\<username>\AppData\Local\Android\Sdk```, although it might vary based on your system.
* On macOS, it's the ```$HOME/Library/Android/sdk directory```.
* On Linux, it's the ```$HOME/Android/Sdk directory```.\
You can also check where your SDK installation directory is by opening Android Studio and clicking **Android Studio > Preferences > Appearances & Behavior > System Settings > Android SDK**. The Android SDK Location file path is your SDK installation directory location.\
If you're using macOS and browsing using Finder, the Library folder might not be visible by default. To navigate there, open Finder and click Go > Go to Folder and search for "Library."
2. Rename the existing ```emulator``` directory in the SDK installation directory, because you'll unzip the newly downloaded ```emulator``` directory here in the next step. For example, call it ```emulator_original```.
3. Download the emulator archive that you want to use from [here](https://developer.android.com/studio/emulator_archive)
4. Unzip the emulator zip file you downloaded, and then move the contents into the SDK installation directory.
5. On macOS: After unzipping the emulator zip file, clear the quarantine attribute on the emulator package by running:\
```xattr -dr com.apple.quarantine emulator/```\
This should reduce messages about whether the package should be checked or blocked.
6. Paste the ```package.xml``` file from the ```emulator_original``` directory into the new ```emulator``` directory.
Change the emulator version specified in the ```package.xml``` file to the version you have downloaded and want to use. To do this, scroll to the bottom of the package.xml file and find the text that looks like:\
```<revision><major>31</major><minor>1</minor><micro>4</micro></revision>```\
This is where you should specify the emulator version you downloaded and want to install.

## Reference
1. https://github.com/flutter/flutter/issues/146890
2. https://developer.android.com/studio/emulator_archive