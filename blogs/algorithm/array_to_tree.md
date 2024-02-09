---
title: 将一维数组转为树状结构
date: 2023/8/22
tags:
 - arrToTree
categories:
 - 算法
---

```js
const data = [
  {
    id:1,
    label:'l-1',
    parentId:0
  },
  {
    id:2,
    label:'l-2',
    parentId:0
  },
  {
    id:3,
    label:'l-1-1',
    parentId:1
  },
    {
    id:4,
    label:'l-1-2',
    parentId:2
  },
  {
    id:5,
    label:'l-1-2-1',
    parentId:4
  },
  {
    id:6,
    label:'l-1-2-1-1',
    parentId:5
  }
]