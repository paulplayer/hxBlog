---
title: sleep and wake classification
tags: 
	- Writing
	- Project
	- Open Source Software
	- OSAHS
categories:
	- Origin
date: 2015-10-23 12:08:47
---

{% blockquote -- sleep and wake classification %}
A Bayesian approach for sleep and wake classification based on dynamic time warping method.
{% endblockquote %}

<!-- more -->

## 插图
{% img /gallery/origin/0001-DHR-OSAHS-998.png 500 DHR-OSAHS-998 %}
<p align="center"><b>DHR-OSAHS-998</b></p>

***
## 目录
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [sleep and wake classification study](#sleep-and-wake-classification-case-study)
	- [插图](#插图)
	- [目录](#目录)
	- [正文](#正文)
	- [1. Introduction](#1-introduction)
	- [2. Methods](#2-methods)
	- [3. Results](#3-results)

<!-- /TOC -->

***

# sleep and wake classification case study

> sleep and wake classification study is a signal data mining study from wrist-worn multi-sensor devices.

## 1. Introduction

Sleep plays a significant role in human’ smental and physical health. Recently, the associations between lack of sleep and weight gain, development of cancer and many other health problems have been recognized. Then monitoring the sleep and wake state all night is becoming a hotspot issue. Traditionally it classified by a PSG recording which is very costly and uncomfortable. Nowadays, with the advance of internet of things, many convenient wearable devices are being used for medical use, like measuring the heart rate (HR), blood pressure and other signals. With the sleep quality monitor problem, the key question is how to discriminate the sleep and weak stage from these signals. This paper proposed a Bayesian approach based on dynamic time warping (DTW) method for sleep and wake classification. It used HR and surplus pulse O2 (SPO2) signals to analyze the sleep states and the occurrence of some sleep-related problems. DTW is an algorithm that searches an optimal alignment between time series with scaling and shifting and Bayesian methods have been successfully used for object classification in many study. In this paper, a three-step process is used for sleep and wake classification. In the first step, the DTW is used to extract features of the original HR and SPO2 signals. Then a probabilistic model is introduced for using the Bayesian classification for uncertain data. And in the classification step, the DTW features are used as the training dataset in the Bayesian approach for sleep and wake classification. Finally, a case study form a realword applications, collected from the website of the Sleep Heart Health Study, is presented to shown the feasibility and advantages of the DTW-based Bayesian approach.

## 2. Methods

{% img /gallery/origin/0001-dtw-based.png 500 DTW-BASED METHOD MODEL %}
<p align="center"><b>DTW-BASED METHOD MODEL</b></p>

{% img /gallery/origin/0001-features.png 500 Features %}
<p align="center"><b>Features</b></p>

## 3. Results

{% img /gallery/origin/0001-result.png 500 Results %}
<p align="center"><b>Results</b></p>
