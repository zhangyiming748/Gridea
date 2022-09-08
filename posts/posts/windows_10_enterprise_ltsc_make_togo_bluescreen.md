---
title: 'Windows 10 Enterprise LTSC做Windows To Go蓝屏无法进入系统'
date: 2022-09-04 22:02:25
tags: [Windows,Windows To Go]
published: true
hideInList: false
feature: 
isTop: false
---

1. 管理员运行cmd或powershell
`compact.exe /U E:\Windows\System32\drivers\*.sys`
2. 替换WTG文件
`c:\windows\system32\drivers\wpprecorder.sys`为1803版
