---
title: The Content Delivery Network
tags: 
	- Writing
  - Theoretical
  - Network
  - Hightech
categories:
  - 原创
date: 2018-01-02 16:08:27
---

{% blockquote ——写在前面，致自己 %}
年龄不是衡量一个人成熟的刻度，只有责任的叠加才会让人逐渐成长。 ​​​​经历越多就越不想说话，环境的不同，想说的话别人未必能懂。不要顾全大局，大局是顾全不了的，你只能找合适的人合作。工作和婚姻都是如此。入对行，找对伴，嫁对人，人生才会顺溜，否则，刚绕过一座山，抬眼又是一座。。
{% endblockquote %}

<!-- more -->

## 插图


{% img /gallery/origin/0006-CDNLogo.png 500 CDN Learning Logo %}
<p align="center"><b>CDN Learning Logo</b></p>

-----

# CDN网络加速学习笔记

## 一、阿里云CDN简介

> 原文链接 https://help.aliyun.com/document_detail/27101.html?spm=5176.doc27247.6.539.cXLJUc

1.阿里云 CDN（内容分发网络）全称是 Alibaba Cloud Content Delivery Network，建立并覆盖在承载网之上、由分布在不同区域的边缘节点服务器群组成的分布式网络，替代传统以WEB Server为中心的数据传输模式。

2.将源内容发布到边缘节点，配合精准的调度系统；将用户的请求分配至最适合他的节点，使用户可以以最快的速度取得他所需的内容，有效解决Internet网络拥塞状况，提高用户访问的响应速度。

3.使用CDN后的http请求处理流程如下图：

-----

 {% img /gallery/origin/0006-CDNProcessing.png 500 CDN processing %}
 <p align="center"><b>CDN Processing Model</b></p>

-----

4.功能介绍：节点缓存、精准调度、多场景业务支持、多组件配合服务、自助式管理、实时服务。

5.CDN的域名加速需要用到CNAME记录，在阿里云控制台配置完成CDN加速后，您会得到一个加速后的域名，称之为CNAME域名（该域名一定是\*.\*kunlun.com）， 用户需要将自己的域名作CNAME指向这个\*.\*kunlun.com的域名后，域名解析的工作就正式转向阿里云，该域名所有的请求都将转向阿里云CDN的节点。

6.Alibaba CDN 加速业务分类：

|  业务类型  | 内容                                                                                                                                                                        |
|:-----:| -------------------------------------------------------------------------------------- |
| 图片小文件 | 若加速内容多为 小型的静态资源 （如小文件、图片、网页样式文件等），推荐选择“图片小文件”业务类型。                                                                            |
| 大文件下载 | 若加速内容为 较大的文件（大于20MB的静态文件），例如游戏安装包、应用更新、手机ROM升级、应用程序包下载等场景，推荐选择“大文件下载”业务类型。                                  |
| 视音频点播 | 若大文件为 音频、视频文件，例如音乐、视频的点播业务场景，推荐使用“视音频点播”业务类型。                                                                                     |
| 直播流媒体 | 提供 直播流媒体 加速服务，目前支持 RTMP 和 HLS 方式的直播加速，直播业务类型不支持自定义源站，目前统一提供直播中心服务器：video-center.alivecdn.com                          |
|  全站加速  | 即 动态加速，适用于动静态内容混合、含较多 动态资源请求 的站点。通过配置区分站点的动静态内容，静态内容高速缓存，动态内容通过阿里云的最优链路算法及协议层优化得到最快的响应。 |

7.移动加速（Mobile Accelerator)是针对移动应用推出的动静态全网加速产品，旨在依托阿里云遍布全国的CDN节点，海量带宽网络等优越的基础设施资源，以及使用智能域名解析、无线协议优化、内容动态压缩、运营商级别优化等技术，为开发者提供更快、更稳定的网络接入能力，有效提升移动应用的可用性及用户体验。

8.移动加速服务主要通过：
 - 协议优化：采用深度优化定制的私有协议替换传统的HTTP协议，收获多路复用、请求头压缩、请求优先级支持等收益，防止内容劫持现象发生。同时我们也为云加速服务终端与加速节点间长连复用，最小化TCP的建连开销，提高连接利用率和请求响应速度；
 - 链路优化：以阿里云遍布全国的优质边缘节点，海量的带宽资源为基础设施，结合HTTPDNS智能路由精准的调度，实现快速选路，就近接入；云加速节点会缓存热点内容，大大提高访问效率；云加速节点和ECS间搭建专线进行链路加速，如果您已经在使用阿里云ECS作为服务后端，加速结果更是锦上添花；
 - 全站加速：支持HTTP/HTTPS的动态和静态请求的全站加速

## 二、移动端加速相关知识

1.Why is my CDN 'slow' for mobile clients
> 原文链接 https://www.igvita.com/2014/03/26/why-is-my-cdn-slow-for-mobile-clients/

2. Last-mile 最后一公里，通信行业经常使用“最后一公里”来指代从通信服务提供商的机房交换机到用户计算机等终端设备之间的连接。

3.使用CDN时用户访问流程和延迟信息

-----

 {% img /gallery/origin/0006-LatencyInCDNProcessing.png 500 Latency in CDN processing %}
 <p align="center"><b>Latency in CDN Processing Model</b></p>

-----

4.CDN加速主要是缓存优化，网络优化(TCP协议优化，降低连接次数)，内容优化(内容尺寸优化，内容压缩)三方面内容：
> 原文链接 https://www.zhihu.com/question/24759400/answer/28893522

 - 缓存优化：
   - 1.内容针对cache 优化，比如expire header之类。没错，假如内容在客户端cache了就不需要网络访问的时间了，这个是传统cdn就很重视的技术 , 而且可以无视网络的高延迟。
 - 网络优化：
    - 2.tcp优化，高延迟环境下丢包会大大增加tcp延迟和降低传输速度，tcp协议栈优化有助于改进这点, 特别是下载内容的时候 -- 请google "fast tcp"
   - 3.减少tcp连接数量，比如利用http1.1 Persistent Connections 和 pipeline 技术。 还有网宿的利用sdk来减少连接
   - 4.刚才说的pipeline可以提高发送请求速度
   - 5.合并小文件，比如 css , js 等， 这会修改html内容。合并以后会减少请求次数
   - 6.CDN 更改内容，将小文件内容 inline 话，比如将一些 js 脚本从独立文件改为直接放到 html 中间去，这下省了好几个包往返，很划得来。
 - 内容优化：
   - 7.优化内容尺寸，比如html、js优化和图片优化，这可以改善下载时间。 图片压缩（比如webP等更高压缩率的图片压缩方式等），图片文件尺寸相对较大，在不影响质量的情况下压缩个30-60%可以获得很好的效果，CDN还可以识别手机设备和浏览器的特性，来获得更高的压缩效果。
   - 8.gzip等传输方式可以节约带宽缩短网络传输时间。
   - 9.js 解析优化，比如js文件放到页面后面防止阻塞页面解析，这个对于前端优化不错，但是对于cdn更改页面可能会造成一些bug。

三、关于ICN移动应用加速的相关信息

1. Neumob Protocol, 宣称 Neumob accelerates app performance by a factor of 2-10x，各层加速原理简述如下图：
-----

 {% img /gallery/origin/0006-neumobProtocol.png 500 Neumob Protocol %}
 <p align="center"><b>Neumob Protocol</b></p>
 
-----

2. 
