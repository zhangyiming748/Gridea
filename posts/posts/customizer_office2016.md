---
title: '定制安装office2016'
date: 2022-09-04 22:36:13
tags: [Office]
published: true
hideInList: false
feature: 
isTop: false
---

代码如下

configure.xml
```
<Configuration>
	<Add SourcePath="H:\" OfficeClientEdition="64" Branch="Current">
		<Product ID="O365ProPlusRetail">
			<Language ID="zh-CN" />
			<ExcludeApp ID="Access" />
			<ExcludeApp ID="Groove" />
			<ExcludeApp ID="InfoPath" />
			<ExcludeApp ID="Lync" />
			<ExcludeApp ID="Publisher" />
			<ExcludeApp ID="SharePointDesigner" />
			<ExcludeApp ID="OneNote" />
			<ExcludeApp ID="Outlook" />
		</Product>
		<Product ID="VisioProRetail">
			<Language ID="zh-CN" />
		</Product>
		<Product ID="proplusretail">
			<Language ID="zh-cn" />
			<ExcludeApp ID="Access" />
			<ExcludeApp ID="Groove" />
			<ExcludeApp ID="InfoPath" />
			<ExcludeApp ID="Lync" />
			<ExcludeApp ID="Publisher" />
			<ExcludeApp ID="SharePointDesigner" />
			<ExcludeApp ID="OneNote" />
			<ExcludeApp ID="Outlook" />
		</Product>
	</Add>
</Configuration>
```
其中
+ ExcludeApp表示不安装,相反IncludeApp表示安装
+ SourcePath="H:\"表示安装镜像挂载的位置,比如H:\
+ ProPlus2019Volume表示安装你常见的office组件
+ VisioPro2019Volume表示安装VISIO
+ 剩下的靠猜也能猜出来
