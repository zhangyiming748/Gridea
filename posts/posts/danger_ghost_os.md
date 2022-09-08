---
title: 'ghost(盗版)系统的危害'
date: 2022-09-04 18:33:24
tags: [Windows]
published: true
hideInList: false
feature: 
isTop: false
---
Ghost 系统是指使用Ghost软件做成镜像压缩包的Windows系统,俗称Ghost版系统.
除了安装速度快,省事,没有多少优点.
电脑店一般给你安装的都是这种系统,因为又快又赚钱.曾几何时,Ghost XP系统曾大行其道,各种什么番茄花园\电脑公司的Ghost系统充斥于市面.目前,一些Ghost版的Windows7也随处可见,Ghost Windows7虽然安装方便,用克隆版的目的是节省安装时间.它通过一键分区\一键装系统\自动装驱动\一键Ghost备份(恢复)等一系列手段,使装系统花费的时间缩至最短,极大地提高了工作效率.可是使用起来却非常的不稳定与不安全.
先说它的**稳定性**.在Windows7的正常安装过程中,其实也是Windows7与用户的硬件系统契合过程,通过一系列的Windows7自动安装调试过程,这样安装的系统才够稳定.而Ghost系统却直接跳过了安装过程(其实是将别人电脑中装好的Windows7做个Ghost镜像,然后进行一些修改),别人的电脑硬件系统大多数情况下都与你的不同,那么导致软硬件兼容性出现问题,系统的稳定性可想而知.
谁也不愿自己的电脑时不时的出现错误提示,时不时的蓝屏,导致未保存的资料瞬间消失,一上午甚至几天的辛苦便付之流水.
再来说说Ghost Windows7的 **安全性**.十个Ghost 八个坑.Ghost系统的制作人员真的这么好心花费大量的时间为的就是帮网友们一个忙么?其实不然,Ghost系统中通常都安装了一系列软件,浏览器主页\搜索引擎也给修改了.制作者甚至在系统中集成各类流氓插件,制作者就是依靠这些安装软件厂商及绑定网页提供的返点分成而获得利益的,而用户无意中就成为了他们的赚钱工具.甚至有些Ghost Windows7还预设了后门与木马程序,当用户安装上这个Ghost Windows7后一连接网络,系统里边内置的木马程序就会向黑客们报告,黑客们就可以如入无人之境那样进入你的Windows7,什么重要资料呀\什么网银密码呀,都给黑客们一览无遗.
友情提醒网上各种Ghost万能克隆系统可能存在的后门:
1. **修改IE浏览器的相关文件**,将里面默认的无效提示页面的指向改成指向后门者设置的页面(广告或放毒或什么都不做都行,随便他在页面上放什么);
2. **修改默认搜索引擎**,在不影响你使用的情况下,添加他的合作标识,这样你每用一次搜索,他就能够从搜索提供商获利.
3. **更改系统actxprxy.dll等系统上网相关的关键文件**,其中预留后门,让系统文件成为木马病毒下载器.这样被修改的文件本身并没有破坏性,但其充当下载器后,下载回来并行的程序就五花八门,甚至可以是上百个后门.
4. **采取不安全的做法**,打安全补丁时只打一部分,预留几个关键的不打(即系统中并没有相应版本的系统文件),但同时将相关补丁的标识写入注册表,让此后任何方法打补丁时,都识别为补丁已经打过,从而导致系统中这几个漏洞的永久性开放.而且无法再修补(你根本不清楚预留了哪些补丁没有真实打上去),除非干净重装.
5. **一些隐藏的行为**(这个可以更多,比如预装暴风影音\QQ的搜索,推广迅雷\搜狗拼音\推广自己的劣质导航页面或网站(其中绝大多数带毒),都是可以与合作方分银子的.而且你可不要以为会给你"干净"的东西).
6. **一些类似东海系统对系统默认安全设置进行修改的行为**.类似的还比如故意采用FAT32格式的系统分区等,有意降低系统的安全性能;还比如以文件流的方式隐藏恶意程序,等等.
7. **即使自己Ghost,也请小心使用网上提供的万能克隆封装工具**,因为上述有关手脚已经被融合到封装工具中,使用工具封装后,某些后门就已经留好了!因此自己封装也建议不要怕麻烦,手工进行.
如`dism /capture-image /capturedir:D:\ /imagefile:E:\HCT_Windows10_RS2_Pro_X64_332.wim /name:"HCT Windows 10 RS2 Pro X64 332" /compress:fast`
8. 至于 **公开设定甚至锁定主页\加几个收藏夹条目** 之类更是小儿科的做法.
9. **稳定性低,兼容性差** 在重新封装系统时,作者会删除认为用户用不到的系统组件,修改一些系统设置,导致系统不完整,系统设置并不符合用户的电脑.所以用户会发现ghost版系统经常蓝屏\无缘无故死机,隔段时间就要重新安装系统.
10. **内置软件太多** 删也删不掉."天下没有免费的午餐",基本上没有人愿意免费封装系统的."我下载ghost版系统也没花一分钱,他们是怎么得到利益的呢?"很简单,和软件提供商合作,在系统中内置他们的软件,作者就能拿到一部分利益.而对于用户来说,被迫使用内置的软件,没有选择权,还不能删除.
11. **驱动不正确** 降低电脑性能,作者在封装系统时,不可能内置所有驱动,只能集成所谓的通用版驱动.殊不知,驱动没有安装好,是很容易拖慢系统的.
12. **安全性得不到保障** 用户下载安装的ghost版系统,作者是否内置了病毒?是否预留了后门漏洞?内置的软件是否有偷看并上传用户隐私?以及其他我们不知道的东西.因为ghost版系统安不安全,完全取决于封装作者的良心.而用户是没有任何选择权的,在使用ghost版系统造成的损失也是无法估计的.

网络上的什么系统之家\深度技术\雨林木风\风林火山......之类的.纯净版,精简版均是ghost系统.系统镜像扩展名为gho的,或者iso镜像解压后会看到.gho的一般都是ghost系统.
原版就是折腾起来麻烦些,但是换来稳定,安心.
关于原版镜像推荐去[MSDN](https://msdn.itellyou.cn/)下载
不要指望电脑城,给你一步一步安装系统,弄驱动什么的,有些电脑白,你给他弄个纯净系统,他还会觉得,你什么都没给他装,很不负责