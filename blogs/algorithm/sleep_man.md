---
title: Sleep Man支持sleep和eat两个方法；支持链式调用
date: 2023/8/22
tags:
 - Sleep Man
categories:
 - 算法
---

<img src="/image-20230405162948770.png" alt="image-20230405162948770"  />

代码设计：由于有sleep功能，函数不能直接在调用时触发；需要初始化一个列表，把函数注册进去；由每个item触发next执行（sleep则异步触发）

![image-20230405163207942](/image-20230405163207942.png)

talk is cheap, show you my code.
