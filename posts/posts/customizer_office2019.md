---
title: '定制安装office2019'
date: 2022-09-04 22:36:48
tags: [Office]
published: true
hideInList: false
feature: 
isTop: false
---
代码如下

configure.xml
```
<?xml version="1.0"?>
-<Configuration>
	-<Add  SourcePath="H:\" ForceUpgrade="TRUE" AllowCdnFallback="TRUE" Channel="PerpetualVL2019" OfficeClientEdition="64">
		-<Product ID="ProPlus2019Volume">
			<Language ID="zh-cn"/>
			<Language ID="en-us"/>
			<ExcludeApp ID="Groove"/>
			<ExcludeApp ID="OneNote" />
			<ExcludeApp ID="Access" />
			<ExcludeApp ID="Lync" />
			<ExcludeApp ID="PowerPoint" />
			<ExcludeApp ID="Excel" />
			<ExcludeApp ID="OneDrive" />
			<ExcludeApp ID="Outlook" />
			<ExcludeApp ID="Publisher" />
			<ExcludeApp ID="Word" />
		</Product>
		-<Product ID="VisioPro2019Volume">
			<Language ID="zh-cn"/>
			<Language ID="en-us"/>
			<ExcludeApp ID="Groove"/>
		</Product>
		-<Product ID="ProjectPro2019Volume">
			<Language ID="zh-cn"/>
			<Language ID="en-us"/>
			<ExcludeApp ID="Groove"/>
		</Product>
	</Add>
	<Property Value="0" Name="SharedComputerLicensing"/>
	<Property Value="TRUE" Name="PinIconsToTaskbar"/>
	<Property Value="0" Name="SCLCacheOverride"/>
	<Updates Enabled="TRUE"/>
</Configuration>
```
其中
+ ExcludeApp表示不安装,相反IncludeApp表示安装
+ SourcePath="H:\"表示安装镜像挂载的位置,比如H:\
+ ProPlus2019Volume表示安装你常见的office组件
+ VisioPro2019Volume表示安装VISIO
+ ProjectPro2019Volume表示安装Project
+ 剩下的靠猜也能猜出来


<iframe width="560" height="315" src="https://www.youtube.com/embed/kewFfaHMfOc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

2019同理
