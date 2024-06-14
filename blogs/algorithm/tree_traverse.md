---
title: 前中后序遍历二叉树
date: 2023/8/14
tags:
 - Tree Traverse
categories:
 - 算法
---

```typescript
// 二叉树的遍历

interface ITreeNode {
  value: number;
  left: ITreeNode | null;
  right: ITreeNode | null;
}
const resArr: number[] = [];

/**
 * @param node 前序遍历
 */
function preOrderTraverse(node: ITreeNode | null) {
  if (node == null) return;
  // 根 左 右
  resArr.push(node.value);
  preOrderTraverse(node.left);
  preOrderTraverse(node.right);
}
