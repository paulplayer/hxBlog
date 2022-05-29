---
title: The Information Centric Network
tags: 
	- Writing
	- Theoretical
	- Network
	- Hightech
categories:
	- 原创
date: 2017-12-29 15:08:27
---

{% blockquote ——写在前面，致自己 %}
未来已经发生,只是尚未流行。
{% endblockquote %}

<!-- more -->

## 插图


{% img /gallery/origin/0005-icnlearningLogo.png 300 ICN Learning Logo %}
<p align="center"><b>ICN Learning Logo</b></p>

-----

# ICN信息中心网络学习笔记

## 一、A Survey of information-centric networking，Ahlgren et al.

> 原文链接 http://ieeexplore.ieee.org/abstract/document/6231276/

1.The ICN architectures leveerage in-network storage for caching, multiparty Comunication through replicaton, and interaction models that decouple sender and receivers.

2.The common goal is to achieve efficient and reliable distribution of content by proving a general platform for communication services that are today only available in dedicated systems such as peer-to-peer (P2P) overlays and proprietary content distribution networks.

3.ICN approach was pioneered in TRIAD (www-dsg.stanford.edu/triad/)

4.More recent projects representing four approaches being actively develped:
- Data-Oriented Network Architecture (DONA)
- Content-Centric Networking (CCN), currently in the Named Data Networking (NDN) project,(www.named-data.org)
- publish-Subscribe Internet Routing Paradigm (PSIRP), now in the Publish-Subscribe Internet Technology (PURSUIT) project,(www.fp7-pursuit.eu)
- Network of Information (NetInf) from the Design for the Future Internet (4WARD) project, currently in the scalable and Adaptive Internet Solutions (SAIL) project,(www.sail-project.eu)

5.Main Components of ICN Design
- Named Data Objects
- Naming and Security
- Application Programming Interface
- Routing and Forwarding
- Caching

-----
 {% img /gallery/origin/0005-ICN.jpg 500 ICN Comunication Model %}
 <p align="center"><b>ICN Comunication Model</b></p>
-----

6.Advantages with the ICN approach
- scalable and Cost-efficient content distribution
- persistent and unique naming
- security model
- mobility and multihoming
- disruption tolerance

7.Data-Oriented Network Architecture
- In DONA, NDOs are published into the network by the sources.
- Nodes that are authorized to serve data, register to the resolution infrastructure consisting of resolution handlers.

8.Content-Centric networking
- NDOs are published at nodes, and routing protocols are employed to distribute information about NDO location.

9.Publish-Subscribe Internet Routing Paradigm

10.Network of Information (NetInf)
- NetInf offers two models for retriebing NDOs, via name resolution.

## 二、Custodian-Based Information Sharing, Van Jacobson, et al.

1.A Sharing sustem that does not require infrastructure yet supports robust, distributed, secure Sharing by opportunistically using any and all connectivity, local or global, permanent or transient, to communicate.



## 三、Summary of Characteristics of ICN approaches

1.Note from "A Survey of information-centric networking".

-----
 {% img /gallery/origin/0005-icnapproaches.png 500 ICN approaches %}
 <p align="center"><b>Table 1. Summary of Characteristics of the ICN approaches</b></p>
-----

## 四、信息中心网络缓存技术研究综述，张天魁，等

1.为了适应互联网应用由发送者驱动的端对端通信模式向由接收者驱动的海量内容获取模式的转变，从网络体系架构层面提供对高效内容获取的原生支持，以信息为中心的网络(ICN,information centric networking)作为一种新型网络体系架构，得到了越来越多研究人员的关注，并成为了未来网架构相关研究的重大工程项目之一。

2.ICN核心概念和网络架构已经度过了花样繁多的阶段，初步相互融合形成了以内容中心网络(CCN,content centric networking)和命名数据网络(NDN,named data networking)为代表的主流网络架构。

3.在CCN/NDN中，每块数据都具备唯一的、与位置无关的名字，名字可以用来进行内容搜索和检索. 请求者根据内容名字用兴趣包首先发起请求，内容源或者其他存储内容的节点回应包含内容名字、附加认证和完整信息的数据包。

4.CCN/NDN研究关注的关键技术包括内容命名方法、内容名称解析、内容/信息路由与转发以及网络内置缓存等。
