---
title: 用对象和链表模拟队列
date: 2023/8/1
tags:
 - Queue
categories:
 - 算法
---

```typescript
interface Item {
  [prop: number]: number;
}

// 用对象实现队列
export class Queue1 {
  private count: number; //记录数量，计算长度
  private lowestCount: number; //记录第一个元素位置
  private items: Item; //存储

  constructor() {
    this.count = 0;
    this.lowestCount = 0;
    this.items = {};
  }

  // 尾部进
  enquene(n: number) {
    this.items[this.count] = n;
    this.count++;
  }

  // 头部出
  dequene() {
    if (this.getlen() === 0) return undefined;

    const res = this.items[this.lowestCount];
    delete this.items[this.lowestCount];
    this.lowestCount++;
    return res;
  }

   getlen() {
    return this.count - this.lowestCount;
  }

  // 查看队头
  peek() {
    return this.items[this.lowestCount];
  }
}
