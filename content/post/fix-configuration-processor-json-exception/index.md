---
title: How to fix JSONException from Spring Boot Configuration Processor
summary: Read about how to fix JSONException from Spring Boot Configuration Processor
description: Read about how to fix JSONException from Spring Boot Configuration Processor
categories: [Spring Boot]
tags: [Spring Boot, Configuration Processor, JSONException]
date: '2024-08-14T23:18:32+08:00'
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
If getting this JSONException like below:
![Configuration Processor Json Exception](images/JsonException.png)
You can try to check gradle dependencies whether if add ```spring-boot-configuration-processor``` dependency.

## Solution
Add the following dependency:
```gradle
implementation 'org.springframework.boot:spring-boot-configuration-processor'
```

## Reference
* https://stackoverflow.com/questions/73071773/how-to-fix-java-lang-classnotfoundexception-org-springframework-boot-configurat
