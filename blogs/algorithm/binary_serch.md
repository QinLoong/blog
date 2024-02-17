---
title: 二分查找
date: 2023/8/3
tags:
 - Binary Search
categories:
 - 算法
---

```typescript
/**
 *  循环(比递归效率更高)
 * @param arr
 * @param target
 * @returns
 */

export function search1(arr: number[], target: number): number {
  if (arr.length === 0) return -1;
  let startIndex = 0;
  let endIndex = arr.length - 1;
  let midIndex: number;
  let midVal: number;