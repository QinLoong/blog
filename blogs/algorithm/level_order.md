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

  while (queue.length) {
    // 记录当前层级节点数
    let length = queue.length;
    //存放每一层的节点
    const curLevel = [];
    for(let i = 0; i < length; i++){
      const node = queue.shift()
      curLevel.push(node.val)
      // 存放下一层的节点
      node.left && queue.push(node.left)
      node.right && queue.push(node.right)
    }
    // 把每一层的结果放到数组
    result.push(curLevel)
  }