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
    //注释节点
    console.log("Comment--", node.textContent);
  } else if (node instanceof Text) {
    //文本节点
    let t = node.textContent?.trim();
    if (t) {
      console.log("Text--", t);
    }
  } else if (node instanceof HTMLElement) {
     // element
    console.log("Element--", `<${node.tagName.toLocaleLowerCase()}>`);
  }
}