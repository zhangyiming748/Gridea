---
title: '如何"优雅"地发布go module模块'
date: 2022-09-03 22:46:37
tags: [Golang]
published: true
hideInList: false
feature: 
isTop: false
---

截止到go1.13, go 官方推出的包管理工具go module已经发布三个版本了,网上也有很多文章介绍如何使用go module,但是大部分都是讲如何引用别人的go module模块,鲜有提到如何发布自己的go module包的文章.本文将主要介绍如何"优雅"地发布自己的go module模块.
本文的代码和命令均在 Windows 10  中运行,go 的版本为 1.17.2

go.dev 是go官方团队于2019年11月上线的集合go开发资源的网站,包括一些学习课程和一些go的案例,当然最重要的就是提供了go的第三方包的检索功能.没错,他就是用来取代原来的godoc.org的,现在godoc.org上也有提示提醒用户迁移到pkg.go.dev.在这篇文章中,我们将把go module模块发布到pkg.go.dev

----

# 发布第一个版本


这次要发布的代码放在github,所以新建一个项目叫calendar, 新增SubDay.go 文件

为SubDay.go添加方法和相关注释

```Golang
package calendar

import (
	"fmt"
	"strconv"
	"strings"
	"time"
)

const (
	NewYear             = "01-01" //新年
	ValentinesDay       = "02-14" //情人节
	WomensDay           = "03-08" //妇女节
	ArborDay            = "03-12" //植树节
	AprilFoolsDay       = "04-01" //愚人节
	LaborDay            = "05-01" //劳动节
	YouthDay            = "05-04" //青年节
	ChildrensDay        = "06-01" //儿童节
	NationalDay         = "10-01" //国庆节
	Halloween           = "10-31" //万圣夜
	ThanksgivingDay     = "11-25" //感恩节
	NationalMemorialDay = "12-13" //国家公祭日
	ChristmasEve        = "12-24" //平安夜
	Christmas           = "12-25" //圣诞节
)

//获取当前年份
func thisYear() string {
	ret := fmt.Sprint(time.Now().Format("2006"))
	return ret
}
func SubDay() {
	fmt.Println(time.Now().Format("早上好,摸鱼人!今天是2006年01月02日"))
	fmt.Println("[摸鱼办]提醒您")
	fmt.Println("工作再累,一定不要忘记摸鱼哦!")
	fmt.Println("有事没事起身去茶水间,去厕所,去廊道走走")
	fmt.Println("别老在工位上坐着,钱是老板的,但命是自己的")
	nextNewYear()
	defer func() {
		fmt.Println("上班是帮老板赚钱,摸鱼是赚老板的钱!")
		fmt.Println("最后,祝愿天下所有摸鱼人,都能愉快的渡过每一天")
	}()
	subValentinesDay()
	subWomensDay()
	subArborDay()
	subAprilFoolsDay()
	subLaborDay()
	subYouthDay()
	subChildrensDay()
	subNationalDay()
	subHalloween()
	subThanksgivingDay()
	subNationalMemorialDay()
	subChristmasEve()
	subChristmas()
}

//情人节
func subValentinesDay() {
	day := strings.Join([]string{thisYear(), ValentinesDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离情人节还有%v天\n", int(unsub.Hours())/24)
}

//妇女节
func subWomensDay() {
	day := strings.Join([]string{thisYear(), WomensDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离妇女节还有%v天\n", int(unsub.Hours())/24)
}

//植树节
func subArborDay() {
	day := strings.Join([]string{thisYear(), ArborDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离植树节还有%v天\n", int(unsub.Hours())/24)
}

//愚人节
func subAprilFoolsDay() {
	day := strings.Join([]string{thisYear(), AprilFoolsDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离愚人节还有%v天\n", int(unsub.Hours())/24)
}

//劳动节
func subLaborDay() {
	day := strings.Join([]string{thisYear(), LaborDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离劳动节还有%v天\n", int(unsub.Hours())/24)
}

//青年节
func subYouthDay() {
	day := strings.Join([]string{thisYear(), YouthDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离青年节还有%v天\n", int(unsub.Hours())/24)
}

//儿童节
func subChildrensDay() {
	day := strings.Join([]string{thisYear(), ChildrensDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离儿童节还有%v天\n", int(unsub.Hours())/24)
}

//国庆节
func subNationalDay() {
	day := strings.Join([]string{thisYear(), NationalDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离国庆节还有%v天\n", int(unsub.Hours())/24)
}

//感恩节
func subThanksgivingDay() {
	day := strings.Join([]string{thisYear(), ThanksgivingDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离感恩节还有%v天\n", int(unsub.Hours())/24)
}

//国家公祭日
func subNationalMemorialDay() {
	day := strings.Join([]string{thisYear(), NationalMemorialDay}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离国家公祭日还有%v天\n", int(unsub.Hours())/24)
}

//万圣夜
func subHalloween() {
	day := strings.Join([]string{thisYear(), Halloween}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离万圣夜还有%v天\n", int(unsub.Hours())/24)
}

//平安夜
func subChristmasEve() {
	day := strings.Join([]string{thisYear(), ChristmasEve}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离平安夜还有%v天\n", int(unsub.Hours())/24)
}

//圣诞节
func subChristmas() {
	day := strings.Join([]string{thisYear(), Christmas}, "-")
	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离圣诞节还有%v天\n", int(unsub.Hours())/24)
}

//计算和元旦的差值
func nextNewYear() {
	thisYearInt, _ := strconv.Atoi(thisYear())
	nextYearInt := thisYearInt + 1
	nextYearStr := strconv.Itoa(nextYearInt)
	day := strings.Join([]string{nextYearStr, NewYear}, "-") //2021-01-01

	ret, _ := time.Parse("2006-01-02", day)
	unsub := ret.Sub(time.Now())
	if unsub < 0 {
		return
	}
	fmt.Printf("距离明年还有%v天\n", int(unsub.Hours())/24)
}
```


执行 go mod init 生成go.mod文件

```shell
go mod init
go: creating new go.mod: module github.com/zhangyiming748/calendar
```

我们把代码push 到远端分支,看起来好像第一个版本就发布完毕了.我们打开pkg.go.dev搜索一下github.com/zhangyiming748/calendar

已经有了

第一个版本至此就算发布完了

# 发布新版本

go module 实际上是可以通过tag来发布版本的.当我们需要发布新版本时,对应的,我们需要使用git tag为这个版本打上标签.假设我们发布的下个版本是v2.0.0

```shell
$ git tag v2.0.0
$ git push --tags
$ git push master
```
