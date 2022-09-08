---
title: 'ssh开机自动启动的设置方法'
date: 2022-09-04 16:56:59
tags: [ssh,Linux]
published: true
hideInList: false
feature: 
isTop: false
---
# 安装

```shell
apt-get install openssh-server
```

# 设置开机启动

```shell
# 开机自动启动ssh命令
$ sudo systemctl enable ssh
# 关闭ssh开机自动启动命令
$ sudo systemctl disable ssh
# 单次开启ssh
$ sudo systemctl start ssh
# 单次关闭ssh
$ sudo systemctl stop ssh
# 设置好后重启系统
$ reboot
# 查看ssh是否启动,看到Active: active (running)即表示成功
$ sudo systemctl status ssh
```
