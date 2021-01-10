---
layout: page
title: 媒体查询给网页带来了哪些便利？这里有你想要的！
excerpt_separator: "<!--more-->"
categories:
     - 学习笔记
---

# 媒体查询给网页带来了哪些便利？这里有你想要的！
## 章节二
### 以下是关于媒体查询的学习笔记介绍：
<!--more-->
### 什么是媒体查询？
* RWD利用弹性网格布局(fluid grid)、弹性图片／媒体(flexible images)、媒体查询(media queries)等技术实现。
* 利用媒体查询，可以根据设备的能力应用特定的CSS样式。比如，根据视口宽度、屏幕宽高比和朝向（水平或垂直），只用几行CSS代码就改变内容的显示方式。
* 媒体查询包含媒体类型和零个或多个检测媒体特性的表达式。Width、height和color都是可用于媒体查询的特性。使用媒体查询，可以不必修改内容本身，而让网页适配不同的设备。

### 媒体查询的写法
在CSS文件中直接使用媒体查询

@media +设备 +（条件）{执行的代码}

* 注：设备默认为screen（屏幕），因此在大多数情况下，“设备”可以省略，直接写@media  +（条件） {执行的代码}

### 深入了解

* 媒体查询开始于css2  

* css3加强来媒体查询

主要包含两个方面：媒体类型  函数

@media all and (min-width:800px) and (orientation:landscape) {

...//样式

}

解释：如果and后面的表达式为true，执行花括号代码里面的样式

all:代表类型，还有screen ,print

and:逻辑操作符，还有 not only

当逻辑为真的时候，就返回一个布尔值true,此时执行花括号里面的样式

@media not screen and (color),print and (color)   <=>  @media not screen and (color) or print and (color)

and:与   全部匹配

or:或 匹配一个就可以

not: 非

only:防止老旧的浏览器不支持媒体查询，而应用到给定的样式

### 媒体查询可以测试哪些特性？ 
媒体查询用的最多的特性是视口宽度（width），很少需要用到其他特性（偶尔会用到分辨率和视口高度）。
* Width：视口宽度
* Height: 视口高度
* Device-width：渲染表面的宽度（设备屏幕宽度）
* Device-height:渲染表面的高度（设备屏幕宽高度）
* Orientation：设备方向是水平还是垂直
* Aspect-ratio：视口的宽高比。aspect-ratio：16/9
* Color：颜色组分的位深。
* Color-index: 设备颜色查找表中的条目数。
* Resolution: 屏幕或打印分辨率。
* Scan：针对电视的逐行扫描和各行扫描。
* Grid：设备基于栅格还是位图。

### 关于概念的解释：
* viewport:视口

视口宽度 和 设备宽度 的区别：

viewport分为三个 即 布局视口 ，可视视口 ，理想视口

* 布局视口：先以960px虚拟显示，将网页的布局显示出来


* 可视视口：手机页面当前显示的视口，用户的缩放会改变可是视口的大小，但是不会改变布局视口的大小


* 理想视口：布局视口在一个设备上的最佳尺寸（理想视口的页面便于浏览器浏览，阅读）

