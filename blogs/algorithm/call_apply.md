---
title: 手写Call & Apply
date: 2023/8/21
tags:
 - Call & Apply
categories:
 - 算法
---

bind 返回一个新函数（不执行），call 和 apply 会立即执行函数

分析：如何在函数执行时绑定this

const obj = { x:11, fun(){ this.x } }，执行obj.fun()，此时fun内部的this就指向obj，可借此实现函数绑定this