---
title: 实现翻转链表及测试用例
date: 2023/9/07
tags:
 - List
categories:
 - 算法
---

首先，我们定义一个简单的链表节点类：
```js
class ListNode {
  constructor(val, next = null) {
    this.val = val;
    this.next = next;
  }
}
```
然后，编写翻转链表的函数 `reverseList`：

```js
function reverseList(head) {
  let prev = null;
  let curr = head;

  while (curr !== null) {
    const nextTemp = curr.next;
    curr.next = prev;
    prev = curr;
    curr = nextTemp;
  }

  return prev;
}
```