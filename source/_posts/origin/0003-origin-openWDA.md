---
title: Open Wireless Display Adapter
tags: 
	- Writing 
	- Project
	- Open Source Software
	- OpenWDA
categories: 
	- 原创
date: 2016-07-23 19:08:27
---

{% blockquote --Definition from WhatIs.com %}  
Social coding is an approach to software development that places an emphasis on formal and informal collaboration. 
{% endblockquote %} 

<!-- more -->

## 插图

{% img /gallery/origin/0003-wirelessDisplayDemo.jpg 500 无线显示适配器 %}
<p align="center"><b>Open Source Wireless Display</b></p>

-----

# OpenWDA 简介

OpenWDA是我接触[GitHub](https://github.com/OpenWDA)之后，尝试发起的第一个开源项目，项目初期目的是开发一款通用跨平台、灵活易操作、性能价格适中的一款无线显示适配器，该项目由软件部分[OpenWDA-Software](https://github.com/OpenWDA/OpenWDA-Software)和硬件部分[OpenWDA-Hardware](https://github.com/OpenWDA/OpenWDA-Hardware)构成，并且对应项目的关键技术难点，模仿成熟的开源项目搭建了专门的论坛，添加了专题模块进行讨论。

起初，找了两个小伙伴，大家兴趣盎然的加入了码代码的行列，然而各种各样的原因，代码写了一小半，项目被搁置了。本质上还是没有需求牵引，又没有办法当成使命任务去推进，而且我们的技术实力相对还比较薄弱，难度较大，代码量较大，占用精力较多，而大家凭兴趣开发渐渐的也就被拖累的没有了激情，因此也就搁置了，而且搁置的越久，市面上类似的产品也越来越成熟，第一次Social Coding的尝试也就宣告失败。也是隔了这么段时间，回过去看，毕竟是social coding,所以也应当是靠兴趣驱动的，而且吸引人加入的很关键的一个地方，是要自己先来拿出一个版本，当自己提供的demo质量和效果还不错的时候，大家才有可能会跟进来，从而迎来社会化编程的happy ending.

这里就先将以往零零碎碎的方案和想法简单汇总在下面：

{% img /gallery/origin/0003-wirelessDisplayDemo1.jpg 500 无线显示概念图 %}

## OpenWDA软件相关部分技术解决方案研讨

大家好，在讨论OpenWDA软件相关的解决方案之前，我把自己对于OpenWDA项目已经积累的想法，进行一个梳理，方便大家与我讨论。

首先，OpenWDA(Open Wireless Display Adapter)是一个以构造软硬件结合的无线显示适配器的开源项目，跟目前市面上的无线显示适配器设备即有关联又有区别。

目前，市面上无线显示适配器也有一些，主要的几款有：Google的Chromecast，微软的Miracast适配器, 以及面向苹果技术的Airplay适配器。从功能上来讲，这三款都具备无线镜像显示的功能，通过扩展DLNA协议，都可以实现音频、视频文件的推送播放，然而Airplay还支持控 制回调，支持投影屏幕和设备自身显示内容不一致，既方便用户在投影观看电影的时候可以轻松的收发邮件，又拓展了用户使用的新的交互模式，例如，针对Airplay功能，游戏开发者可 以将游戏内容投影到大屏幕上，而手机设备显示游戏的控制面板，大大增加了操作的趣味性。然而苹果设备加个较贵，而且与其他设配并不兼容，其他的无线投影设备功能也不够完善，Chro mecast需要依赖于Chrome浏览器且要安装特殊插件，Miracast设备使用起来需要额外的usb供电，而且只兼容Windows，价格也不够亲民。而且就当前阶段而言， 无线显示设备尚未普及，事实上，无线显示的标准目前也是存在多家，尚未有统一的标准，而且就目前国内电器市场现状，很长一段时间内，大量的普通家庭用户中依旧会存在很多不具备无线显 示功能的显示设备，因此，该无线显示适配器有其使用上的现实需求。这里给大家附上一张家庭应用无线显示适配器的图片。

{% img /gallery/origin/0003-wirelessDisplayDemo2.jpg 380 无线显示概念图 %}

接下来，我主要从**需求，功能，硬件选型，软件基本构想**几个方面，说下我的想法：

### 1、OpenWDA 需求定位

关于OpenWDA的需求，我认为主要瞄准在两类应用场景，一个是办公会议室集中讨论交流应用场景，另一个是家庭居家娱乐应用场景。对于办公讨论环境来讲，由于讨论中需要频繁的与会 议成员交流，镜像功能显示就可以满足大部分的需求，然而讨论中经常需要更换发言人，因此该适配器需要支持多用户快速切换，从而快速的投影显示下一位发言者的内容，另外讨论中，成员听 到另一位的idea，经常会希望找他要一些资料，因此也应当提供供用户交流的文件和通信的功能，同时，也经常会发现需要补充扩展一些内容，如果投影过程中，可以上网一下子就方便多了 ，因此考虑提供当前投影用户上网的功能。对于居家娱乐使用，考虑用户常常投影的内容为视频影像，播放时间较长，因此在播放时，考虑提供控制回调的功能，用户在投影播放视频的时候，可 以进行控制回调，正常投影播放影音内容的同时，可以通过设备收发邮件，回复微信等。

### 2、OpenWDA 功能设计

针对以上需求，OpenWDA应当具备以下功能：

{% img /gallery/origin/0003-wirelessDisplayDemo3.jpg 500 无线显示概念图 %}

- 多显示器适配，最少支持vga，hdmi两种，考虑支持avi输出；
- 多系统适配，支持Windows, Linux, MAC, Android, IOS等系统；
- 支持多用户连接，可快速转换投影，可相互通信，可上外网；
- 支持镜像显示功能，支持分辨率720p以下视频输出，支持控制回调功能；
- 扩展支持建议会务系统功能。

值得注意的是，在功能实现时，要充分的考虑用户体验，对用户的操作习惯的继承和培养要格外重视，最好的操作就是静默，用户几乎啥都不用做，就可以完成，甚至啥都不用安装，访问个网页 就可以完成，然而目前视频标准都没有很好的定下来，因此不考虑跟各个操作系统实用的无线视频显示标准做适配，事实上，Linux上还没有推出满足无线显示标准的系统级应用。总之，设 计时要牢记，对用户来讲，讲究极简，讲究继承，越熟悉越好，越傻瓜越好。

### 3、OpenWDA 硬件选型

OpenWDA的功能可以笼统的概括成，一个智能路由设备+支持回调功能的无线显示设备，结合目前火的不行的开源硬件设计理念，主要考虑两种选型和设计模式：

{% img /gallery/origin/0003-BeagleBoneBlack.jpg 200 BeagleBoneBlack开发板 %}

思路1：通过使用支持嵌入式操作系统如arm-Linux系列的通用开发板，进行必要的外设和驱动的扩展开发，如选定Beaglebone black（一款性价比超高的完全开源的硬件板）开发板，前期的vga输出接口和hdmi输出接口以及网络连接接口，可以通过购买usb通用外设，通过usbhub集中挂载到板子上 , 后期在针对性的优化和调整。

{% img /gallery/origin/0003-openWRT.jpg 180 OpenWRT系统 %}

思路2：通过一些通用智能路由器的开发板（支持openwrt系统的），这样一来，网络功能和硬件的网络吞吐能力都已经是设计好的了，只用针对性的开发vga,hdmi等的视频输出 扩展，大概就是一个D/A转换，然而输出到vga上面，具体我不是学硬件的，不是很懂。然而路由器的扩展要比开发板的少很多，而且开发门槛比较高，驱动软件要复杂的多。

另外硬件的选型和设计，还有一个十分重要的功能考虑，由于OpenWDA本质上涉及到大量的流媒体的编解码工作，所以要考虑是否需要硬件支持，这里我特别推荐一个叫做WRTnode Hi的开发板，如下图，可以让我们在视频相关处理中可以充分的利用硬件加速编解码，也恰巧符合了前面说的第二种思路。

{% img /gallery/origin/0003-WRTNode.jpg 200 WRTNode开发板 %}

全球第一款H.265 5MP开源硬件，H.265提供超过H.264一倍以上的压缩效率，WRTnode携手海思呈现的WRTnodeHi 采用全球第一颗H.265硬编码芯片，Hi3516A 提供在视频采集与处理领域前所未有的2560*1920(5MP五百万像素)/30fps/约4Mbps码流的极致参数，配合全面的接口引出与便利的开发框架，让您在视频相关智能设 备的创意可以源源不断。

### 4、OpenWDA 软件架构设计

在讨论OpenWDA的软件架构时，我希望达到的效果是：1）轻量级架构，轻巧快速，适合arm-Linux系列；2）可扩展，可升级，模块化开发思路，代码复用程度高，维护方便； 3）尽量集成，从开源项目中遴选优秀的源代码，选取的技术也要具备一定的先进性。

在讨论确定软件架构时，首先应当先来了解下当前主流无线显示标准。

{% img /gallery/origin/0003-softwareDesign.jpg 300 主流无线显示协议 %}

这里我罗列了一些，别人的总结和讨论, 主要参考[Black Pea](http://www.zhihu.com/question/21864811/answer/95054630)的一篇博文。

airplay是苹果推出的基于wifi的无线显示标准。一般只支持在苹果系产品和通过苹果认证的产品间。支持两种模式：推送和镜像。所谓推送就是把移动终端的内容（图片、视频等） 推到TV等显示设备。镜像是将一个设备的显示推送到另一个显示设备，最棒的应用就是双屏玩游戏：手机做手柄，tv做显示，地图都在手机上显示，TV只显示游戏画面。

miracast是业界为了抗衡airplay推出的无线显示标准，由wifi联盟推出的基于wifi direct的技术，功能和airplay一样。安卓4.2和win8支持。理论上miracast是一个很棒的协议，如果用的溜，基于安卓和window的普及率我们现在应该不会 产生题主的这种疑问了。原因就在于现在各家设备对miracast支持的都不太好，延迟大，兼容性不好。下面这个链接就是外国宝宝对miracast兼容性测试结果（Miracas t Intercompatibility Test Results : Android ）。而且作为一个标准，miracast似乎没有对厂家有统一的"miracast"mark授权。大部分厂家还是各干各的起了新名字，比如LG叫smartshare，三星叫al lshare cast，索尼叫screen mirroring，松下叫display mirroring。各厂商产品之间的兼容性也可想而知。

chromecast是一个插在HDMI口上的接收器。基于DIAL协议，运行简化的chrome操作系统，通过终端设备为chromecast设备建立链接，由chromecas t设备自行去network上down内容来显示，国外流行的netflix在电视上播就是基于这个功能的。这是一个搜索&操作与下载显示相互分离的过程，分别在两个设备上进行。c hromecast也支持将终端设备内容stream推送到显示设备的功能。但是不支持镜像。google更进一步推出了针对音频流的google cast for audio。chromecast可能可以看做google开始放弃miracast的一个征兆。

WiDi是intel的wireless display技术，基于wifi direct，从WiDi 3.5似乎开始兼容miracast。然后再看看DLNA。DLNA是基于UPnP的，严格上讲不算是wireless display，而是一种单纯的无线播放功能，即从一个设备的本地存储中拿内容到另外一个设备上去display。所以内容是基于本地存储的，不能从network自动down 内容去显示。

高清画质的无线音视频传输技术应该是成熟了，市面上已有多款产品。技术规范有UWB（有效距离短，较便宜），WiDi（直接用发送设备的WiFi将视频发送至接收端，有效距离长，0 .3s延迟），WHDI（使用5GHz，传输率3Gbps，有效距离长，0.5ms延迟）等。以后不必拉长长的线了

另外，一些该类别的之前的开源项目，也值的关注和学习，这里我搜集到的有github上的基于nodejs的nodecast，有leapcast，使用DIAL协议提供链接设备; 另外还有一个DLNA的开源的DMS服务器，miniDLNA，并且有对应的DLNA的客户端；再者还有支持Airplay的Shareport的开源项目。还有几个linux平台 上不错的开源项目，Althercast, OpenWFD, Miraclecast，基于无线显示标准进行开发。

通过之前的这么一系列分析,在决定软件架构之前要先选定一个最基本的无线传输方案，虽然UWD，WHDI，传输速率高，视频可以不经过压缩直接传输，然而目前大多数PC和移动式设备 的无线网卡并不支持，pc可以通过扩展usb设备增加，移动式设备就很难进行设备扩展了，因此我建议还是选择目前覆盖率最高的wifi设备，采取必要的编解码处理，参考Miraca st和Airplay无线投影标准，进行设计实现，具体的软件架构实现方案的设想过几天再更新。