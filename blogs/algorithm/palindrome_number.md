---
title: 求输入数字以内的回文数
date: 2023/7/10
tags:
 - Palindrome Number
categories:
 - 算法
---

```typescript
// 求输入数字以内的回文数

/**
 * 方法1：通过反转比较
 * @param num
 */
function getNumbers(num: number): number[] {
  const res: number[] = [];
  if (num < 0) return res;

  for (let i = 0; i < num; i++) {
    const s = i.toString();
    if (s.split("").reverse().join("") === s) {
      res.push(i);
    }
  }

  return res;
}