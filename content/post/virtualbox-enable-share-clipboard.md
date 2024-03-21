---
title: Enable clipboard share and folder share on VirtualBox
summary: Read about how to enable clipboard share and folder share on VirtualBox.
description: Read about how to enable clipboard share and folder share on VirtualBox.
categories: [Virtualization]
tags: [VirtualBox, Configuration]
date: 2018-02-17
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

1. Add virualbox USB extension pack  
2. Insert guest addition CD images  
3. Run software in CD driver  
4. Add user into vboxsf group:
``` bash {linenos=true}
sudo adduser [username] vboxsf  
```