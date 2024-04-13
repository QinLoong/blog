---
title: 斐波那契
date: 2023/7/6
tags:
 - Fabonacci
categories:
 - 算法
---

```typescript
/**
 * 特别慢 时间复杂度为2的n次方
 * @param n
 * @returns
 */

function fabonacci(n: number): number {
  if (n === 1 || n === 2) {
    return 1;
  }
  return fabonacci(n - 1) + fabonacci(n - 2);
}