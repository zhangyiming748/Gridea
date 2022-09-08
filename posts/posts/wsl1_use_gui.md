---
title: 'WSL1使用GUI方法'
date: 2022-09-04 19:23:57
tags: [WSL]
published: true
hideInList: false
feature: 
isTop: false
---
# 前期准备

`sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get upgrade -y && sudo apt-get dist-upgrade -y && sudo apt-get autoremove -y`

# Ubuntu端

```
sudo apt-get update
sudo apt-get install xorg
sudo apt-get install xfce4
sudo apt-get install xrdp
sudo sed -i ‘s/port=3365/port=3365/g’ /etc/xrdp/xrdp.ini
sudo echo xfce4-session >~/.xsession
sudo service xrdp restart
```

# Windows端

`mstsc`中填写`127.0.0.1:3365`

# 善后

以后需要再用的时候输入`sudo service xrdp restart`

----

没想到这么简单吧?
