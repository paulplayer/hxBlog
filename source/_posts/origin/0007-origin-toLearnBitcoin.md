---
title: Bitcoin & BlcokChain
tags: 
	- Writing
	- Theoretical
	- Network
	- Fintech
categories:
	- 原创
date: 2018-01-10 16:08:27
---

{% blockquote ——写在前面，致自己 %}
很多时候善良的建议反而会让人变得平庸，人生总需要一些一意孤行。
{% endblockquote %}

<!-- more -->

## 插图

{% img /gallery/origin/0007-bitcoin.jpg 500 Bitcoin & BlcokChain %}
<p align="center"><b>Bitcoin & BlcokChain</b></p>
-----

# Bitcoin & BlcokChain学习笔记

## 学习 Bitcoin & BlockChain 思路

>from https://www.zhihu.com/question/48049768/answer/121446591 宝术, 五阿哥CTO
>我把知乎上的比特币，区块链大部分文章看了一遍，发现没有几个人能真正理解《比特币白皮书》，能基于加密技术或去中心架构来阐述、分析和扩展相关理论的更是凤毛麟角。绝大多数在人云亦云，说一些自己也不了了的高大上概念，甚至把简单问题复杂化，云山雾罩。 再搜索国内作者的书籍，看看目录就知道不可买。浪费了半天时间品尝别人的口水，还是臭的，我呸呸呸。。最终让我对比特币和区块链拨云见雾的是比特币白皮书和一个github项目。读完它们各花了1小时，其实很简单很简单，因为中本聪并没有发明任何新技术，但巧妙的把很多老技术组合在了一起。
>- 理论。比特币白皮书：一种点对点的电子现金系统 注意别看这个中文版的，翻译错漏太多，比如其中第2节的交易图把“签名”和“公钥”都弄混了，不能忍！请对照看原文https://bitcoin.org/bitcoin.pdf
>- 实现。GitHub - izqui/blockchain: A blockchain implementation 这是一个golang实现。把源码读一遍,一切都如在掌中。看下面关于交易的代码定义，简洁明了。

在阅读这些东西之前，你也只需要具备一些知识或技术经验：

- 不对称加密算法的基本原理及其应用如签名、验证
- Hash算法如SHA的特性，如离散、不可逆等
- Merkle Tree的基本原理，其实就是二叉树Hash
- 懂一门编程语言和计算机常识，如随机数、二进制、Timestamp
- 懂一些P2P网络的常识如BitTorrent更有助于理解

以上看懂就入门了。个人觉得，**比特币其实较难理解的是几个层次**：

1，他的静态结构设计怎么样？为什么这样？如target的难度设计，加密算法的作用。
2，他是如何活生生的运行呢？如交易过程，生成新的区块，分叉的竞争，如何篡改，矿工的激励。
3，他有哪些未解决的难题？如区块扩容，交易并发能力，安全风险等。
4，比特币的扩展生态，如闪电网络，交易所，矿池，钱包。
5，抛开数字货币，区块链在其他场景的应用应该如何设计？如pow的替代机制、联盟链、智能合约。

## A developer-oriented series about Bitcoin

> from http://davidederosa.com/basic-blockchain-programming/ Davide De Rosa

Best Tutorials to Learn Bitcoin Coding I've Found.
