---
title: 数组反转
date: 2023/8/1
tags:
 - Array Rotate
categories:
 - 算法
---

```typescript
function rotate1(arr: number[], k: number): number[] {
  if (!k || arr.length === 0) return arr;
  const step = Math.abs(k % arr.length);

  for (let i = 0; i < step; i++) {
    const tem = arr.pop();
    if (tem) {
      arr.unshift(tem);
    }
  }

  return arr;
}