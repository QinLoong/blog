---
title: 二叉树层序遍历
date: 2023/10/12
tags:
 - levelOrder
categories:
 - 算法
---

talk is cheap, show you my code!
```js
function levelOrder(root) {
  if (!root) return [];
  // result存储结果  queue队列里面存储每层节点
  const queue = [root];
  const result = [];