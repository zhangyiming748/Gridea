---
title: 'ssh问题排除'
date: 2022-09-04 16:54:34
tags: [ssh,Linux]
published: true
hideInList: false
feature: 
isTop: false
---
如果服务器安装了open-ssh,然后发现客户端无法连接,并出现了 
connection reset by (server_ip_address) port 22 
那么你可以试试以下两个指令来重置ssh的配置
```shell
rm /etc/ssh/ssh_host_*
sudo dpkg-reconfigure openssh-server
```