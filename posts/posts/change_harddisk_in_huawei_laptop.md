---
title: '为魔法书扩容的惨痛经历'
date: 2019-11-13 14:58:51
tags: [华为]
published: true
hideInList: false
feature: 
isTop: false
---
刚开始做电脑不代表做的差就天经地义,工作人员不先培训,硬件不是先准备好而是谁需要给谁调货,这真的是"川普优选"公司的正常行为?

我的观点是:在性能和体验上差不多或者偏低的情况下,我会优先选择国产的电脑,这是爱国的表现,但我没必要为了支持国货一味的迁就你.

我确实买电脑了
![开箱图片](https://s2.ax1x.com/2019/11/03/KXEqKK.jpg)<center>其他图片之后再找个国内图床上传</center>


## 按照时间发展顺序

#### 2019-10-15

购买之前询问华为商城客服是否可以扩容,他跟我保证说有第二个硬盘位可以进行扩容,因为我从来不相信这种一点儿技术能力都没有的,客服说的话,我又发电子邮件问了华为客户服务中心,回复我的消息也是说可以扩容,并且他们回复最底下有个标准的一段文字说是不能复制和转发,我电话询问华为客服的时候也是有电话录音的,电子邮件我也保留了.
![下单图片](https://s2.ax1x.com/2019/11/03/KXET81.jpg)<center>华为商城购买</center>

#### 2019-10-16

到货之后询问华为商城客服需要扩容买什么样的硬盘,然后就是答非所问,教我给硬盘分区看起来就像多了一块硬盘,无果,不能指望销售客服也是意料之中的

#### 2019-10-17

电话询问华为售后客服,用了各种话术逼问出是sata3口

#### 2019-10-18

email华为客服中心多次后得知sata3 7mm硬盘
>本邮件含有华为公司的保密信息,仅限于发送给上面地址中的个人.禁止以任何形式使用(包括但不限于全部或部分地泄露\复制\或散发)本邮件中的信息.如果您错收了本邮件,请您立即邮件通知发件人并删除本邮件!This email contains confidential information of Huawei Inc. and is only sent to individuals in the above address. The use of the information in this email in any form, including but not limited to, in whole or in part, disclosure,duplication, or distribution, is prohibited.If you have received this email in error, please notify the sender immediately and delete this email!

#### 2019-10-19

购买硬盘后直接预约北京市石景山王思聪广场华为客户服务中心,去华为客户服务中心网点去换的时候,工作人员跟我说有可能没有第二个接口,为了防止出现工作人员认为多一事不如少一事的情况发生,我跟他们说的是:如果有接口就给我换上,如果没有接口的话就给我拍一张照.拆开电脑后各种洗脑,大致说的是:你买的硬盘不符合规格,没有硬盘架没有排线我们没法安,我们这里没有,安装需要你自己带齐配件,总之各种推脱没硬盘线和支架是我的责任![第一次拆机](https://s2.ax1x.com/2019/11/03/KXEoCR.jpg)<center>在第二个接口还没有安装之前硬盘位是被垫起来的,应该是防止电池被挤压</center>

#### 2019-10-27

辗转崇文门国瑞城华为客户服务中心,电脑拿走说一个小时之后打电话你回来取,漫无目的逛街一个多小时之后回来告知没配件,你没配件直接说不行?非要等我实在逛累了回来才说?刚开始直接说不行?

#### 2019-10-30

三天后主动电话询问客服说正在定

#### 2019-11-01

两天后再次电话询问周六去是否能换上,答不一定,你来看看吧

#### 2019-11-02

周六去了正赶上服务日,人特别多,等了很长时间后询问确实有货,办理,一小时后拿到电脑,开机检查,问题来了:Windows下diskpart检测不到disk1;Deepin下fdisk检测不到sdb;BIOS里检测不到第二块硬盘,所谓的工程师解释得那叫一个苍白无力:之前只换过预装Windows的,安装硬盘之后在磁盘管理里格式化一下就好了,还说自己之前没做过预装Linux电脑加硬盘的操作,我虽然只是一个三本大学计算机毕业的社畜,好歹我该学的还是学会了,骗傻子也不用这样吧,话说回来,华为工程师的门槛这么低吗?但是我不想在这件事上浪费口舌了,靠谁不如靠自己![预约](https://s2.ax1x.com/2019/11/03/KXEHv6.jpg)<center>四次预约,而且电脑是R7,不知为什么这种小错误都要犯</center>

#### 2019-11-02深夜

既然不能识别,就要开始找原因.首先想到的是供电问题,打开后盖发现这条线能提供的电流大概是1A,而我的硬盘是西部数据5400RPM黑盘,有可能是供电不足导致的,随即自己动手更换.

#### 2019-11-03凌晨

拆机过程中,一件令人气愤的事情发生了,硬盘托架固定硬盘的螺丝本来应该是四个,修电脑的 **大师** 只给我装了两个(左上和右下),以前只见过电脑城的奸商在装机的时候习惯能不装的螺丝一定不装,没想到眉清目秀的华为居然也敢这么做.翻箱倒柜找出新买的光威真香盘,由于固态硬盘基本上不存在耗电量巨大的情况,更换,开机,同样的结果:Windows下diskpart检测不到disk1;Deepin下fdisk检测不到sdb;BIOS里检测不到第二块硬盘.排除供电问题,剩下的嫌疑就是排线了,明天自制一条排线换上试试![deepin下](https://s2.ax1x.com/2019/11/03/KXE7gx.jpg)<center>话说Deepin真的对小白用户太友好了,大包大揽</center>

#### 2019-11-03下午

无意间通过串口查看了一下磁盘的S.M.A.R.T,其中的通电次数并没有增加,也就是说硬盘安装在电脑内并没有通过电,看来大概率是排线的问题![通电次数](https://s2.ax1x.com/2019/11/03/KXE559.jpg)<center>硬盘买来之后通电次数一次(由于是OEM拆机盘),用作移动硬盘通电两次(收货后检测一次,节能断电重启一次),**大师** 安装后自行拆卸通电一次</center>

#### 2019-11-03晚

找到问题所在了,所谓的 **大师** 居然把排线装反了,更可笑的是,右侧明晃晃的有一个正确方向的排线,就算您老没看见,小时候没没偷拆过遥控器?
![正过来的排线](https://s2.ax1x.com/2019/11/03/KXGn7n.jpg)<center>后悔没保留图片证据</center>

看来华为客户服务中心的专业性真的是有待查证的了,反正对于我来说,买不到的配件上你那里找,操作只能靠我自己来,拜拜官方

#### 2019-11-03 深夜

卸掉了没有任何受力的\缺少螺丝的硬盘架,在某宝上买到了排线和硬盘缓冲条,经此一事,我深刻的了解了所谓官方能有多水,同时附上这家[淘宝店铺的购买链接](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.45f92e8dKcC9OQ&id=605894154583&_u=32cc9fmu6156)在花粉俱乐部里看到了许多和我有同样需求的朋友,我觉得,北京的华为客服中心尚且是这样的水平,不在北京的你们还是相信自己的双手吧,这家店包教包会包分配,不能指望每个买电脑的人都是~~像我这样的~~电脑高手,这家店甚至比华为官方还值得你信赖.加上第二块硬盘,我实现了Windows 10&Ubuntu18.04双系统双EFI主板直接控制系统的选择,双系统之间互不干预,设立的交换分区800G
![hardDisk](https://s2.ax1x.com/2019/11/03/KjnjRH.jpg)
<center>西数SSHD加上缓冲条</center>

## 总结

#### 2019-11-04

回顾一下整个过程,给后来人一个经验,拆机应该不会影响保修,因为官方人员维修时撕毁的防拆条也不会去复原,不想教会维修人员应该怎么加装第二块硬盘就去淘宝自己买一套工具,同时买一个规格为`sata3接口 7mm 2.5寸 1T及以下容量的机械硬盘`(7mm能保证是单盘片硬盘,肉眼观察排线不能提供500G双盘片需要的1A以上电流)或`sata3接口 2.5寸 2.1T及以下容量的固态硬盘`(容量存疑,不过官方就是这么说的)兼容SATA通道和PCI-E通道,接触电路板之前手上记得做好去静电处理,安装前拔掉电源和电池排线(然而官方的维修人员带电操作,不知道华为找的都是什么工具人,我老家那边十八线小城市电脑城维修人员都知道搞机前先断电)SATA硬盘位会被识别为第一块硬盘也就是`sda`/`disk 0`安装系统的时候千万别搞错了,这也许是我最后一次找官方售后
