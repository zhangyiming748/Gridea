---
title: 'homebrew设置代理'
date: 2022-09-04 01:08:19
tags: [Proxy]
published: true
hideInList: false
feature: https://s1.ax1x.com/2022/09/04/vofoRO.jpg
isTop: false
---
brew用curl下载,所以给curl挂上代理即可
在`~/.curlrc`文件中输入代理地址
```shell
socks5 = "127.0.0.1:1089"
```