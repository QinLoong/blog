---
title: 遍历DOM树
date: 2023/7/5
tags:
 - Dom Traverse
categories:
 - 算法
---

```typescript
//遍历单个节点
function visitNode(node: Node) {
  if (node instanceof Comment) {