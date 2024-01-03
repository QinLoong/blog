---
title: 数组扁平化
date: 2023/7/1
tags:
 - Array Flatten
categories:
 - 算法
---

```typescript
// 数组深度扁平化，使用 push
function flattenDeep1(arr: any[]): any[] {
    const res: any[] = []

    arr.forEach(item => {
        if (Array.isArray(item)) {
            const flatItem = flattenDeep1(item) // 递归
            flatItem.forEach(n => res.push(n))
        } else {
            res.push(item)
        }
    })

    return res
}