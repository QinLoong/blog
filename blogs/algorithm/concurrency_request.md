---
title: 控制并发请求数列，结果按原顺序输出
date: 2023/8/25
tags:
 - request
categories:
 - 算法
---

``` javascript
// 模拟接口

/**
 * 并发maxNum个请求，请求结果顺序与urls保持一致
 * @param {*} urls
 * @param {*} maxNum
 */

function concurrencyRequest(urls, maxNum) {
  return new Promise((reslove) => {
    if (urls.length === 0) {
      reslove([]);
      return;
    }

    const result = [];
    let index = 0;  // 按照顺序发送请求
    let count = 0;  //请求的次数
