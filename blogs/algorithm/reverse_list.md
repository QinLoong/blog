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

这个函数使用迭代的方式将链表进行翻转。我们使用两个指针 `prev` 和 `curr`，分别表示前一个节点和当前节点。通过不断修改节点的 `next` 指针，将链表逐个反转。

接下来，编写测试用例来验证翻转链表的正确性：

```js
// 创建一个链表: 1 -> 2 -> 3 -> 4 -> 5
const head = new ListNode(1);
head.next = new ListNode(2);
head.next.next = new ListNode(3);
head.next.next.next = new ListNode(4);
head.next.next.next.next = new ListNode(5);