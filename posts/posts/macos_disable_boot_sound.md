---
title: 'macOS取消开盖自动开机'
date: 2022-09-03 23:42:28
tags: [macOS]
published: true
hideInList: false
feature: 
isTop: false
---
取消自动开机:

`sudo nvram AutoBoot=%00`

重新启用自动开机:

`sudo nvram AutoBoot=%03`

开启开机音效:

`sudo nvram BootAudio=%01`

取消开机音效:

`sudo nvram BootAudio=%00`
