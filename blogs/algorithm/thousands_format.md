---
title: 数字千分位添加“，”转为字符串
date: 2023/7/14
tags:
 - Thousands Format
categories:
 - 算法
---

```typescript
// 方法一：数组反转+reduce
  function format1(n: number): string {
    // 只考虑整数
    const str = Math.floor(n).toString();
    let arr = str.split("").reverse();

    return arr.reduce((prev, cur, index) => {
      if (index % 3 === 0 && index !== 0) {
        return cur + "," + prev;
      } else {
        return cur + prev;
      }
    }, "");
  }