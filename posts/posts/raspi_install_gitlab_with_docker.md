---
title: '树莓派4安装Gitlab(Docker实现)'
date: 2022-09-04 01:56:02
tags: [Raspberry]
published: true
hideInList: false
feature: 
isTop: false
---
# 下载我制作好的镜像并导入
[百度妙传](c28bf31568588e46467b055ca6326d40#ce8159c6781be298281c8f61b5bc1c7d#2667214336#/docker/gitlab_for_arm64.tar)
# 编辑启动脚本
```shell
DATA_HOME=/home/$USER/Documents/Gitlab
sudo docker run --detach \
    --hostname 192.168.1.5 \
    --publish 10086:10086 \
    --name gitlab \
    --restart always \
    --volume $DATA_HOME:/mnt/git-data \
    gitlab_for_arm64:1.0.0

```
```shell
参数说明:
--detach: 设置容器后台运行
--hostname: 设置容器的 hostname,如果是本地localhost ,否则使用外网ip
--publish: 端口转发规则(80:Http 访问端口,443:Https 访问端口,10080:主机的 ssh 访问端口,22:Docker 容器中 ssh 访问端口)
--name:容器名称
--restart always:每次启动容器就重启GitLab
--volume: 共享目录挂载,即 docker 容器内外数据共享
--e:配置 Gitlab 运行的环境变量
```
# 准备用来映射代码仓库的位置
默认代码仓库保存到`/var/opt/gitlab/git-data`

我习惯换个方便导出的位置

编辑 `/etc/gitlab/gitlab.rb`

找到`git_data_dirs({ "default" => { "path" => "/mnt/git-data" } })`相关字样

改动之后重新部署

`sudo gitlab-ctl reconfigure`
