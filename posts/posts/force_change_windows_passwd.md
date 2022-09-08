---
title: '忘记 Windows 10 密码解决办法'
date: 2022-09-05 13:40:58
tags: [Windows,Windows RE]
published: true
hideInList: false
feature: 
isTop: false
---

# 以下教程,不要拿来干坏事
----
相信还是有很多人不知道/或者不会用Microsoft账号,依然使用的本地账号,而且还不小心忘记了密码,这里提供了一种方法,挽救那些2019年,还在傻傻使用PE的人.

假设当前用户Virtu密码为1234,我们要在不输入原密码的前提下把密码改成12342345.

电脑进入RE环境,在正常开机输入密码界面右下角电源按钮点击小箭头,同时按住键盘shift点击重启,电脑进入recover界面

![1](https://s1.ax1x.com/2022/09/05/vT2EpF.png)

选择疑难解答

![2](https://s1.ax1x.com/2022/09/05/vT2kfU.png)

选择advanced option,然后打开命令提示符

![3](https://s1.ax1x.com/2022/09/05/vT2FYT.png)

在命令提示符里cd到系统所在的盘.注意这时系统所在盘符不一定是c盘,输入dir或者打开notepad确认一下,假设这里系统盘是`D:/`

`cd d:`

`cd windows\system32`

`Copy sethc.exe sethc_bk.exe`

`Copy /y cmd.exe sethc.exe`

重启电脑,等待进入正常登陆界面,连按左边shift五次,这个动作原本是用来激活滞粘键的,也就是执行sethc.exe,但是在上面的操作中,已经覆盖成cmd.exe了,这样执行这个动作后,会打开命令提示符.

插播科普,Windows系统在载入我们自己的账户之前,已经默认登陆了一个账户.这个账户是system账户,俗称最高管理员账户,所有账户的家长,这个账户权限非常高,高过administrator,甚至比华莱士还高,今天我们要跟他谈笑风生.

在命令提示符中输入

`net user`

列出所有用户

![4](https://s1.ax1x.com/2022/09/05/vT2ikV.png)

命令写法:`net user [账户名]空格[新密码]`

接下来修改Virtu帐户的密码

`net user Virtu 12342345`

----
# 以上教程,不要拿来干坏事

# 如果上面的方法不好用,恭喜你用的是新版系统,往下看

<iframe width="100%" height="480" src="https://player.bilibili.com/player.html?aid=847062336&bvid=BV1b54y177G3&cid=379523737&page=1" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture,enablejsapi" allowfullscreen></iframe>

