---
title: 求连续最长的字符及长度
date: 2023/7/2
tags:
 - Continous Char
categories:
 - 算法
---

```typescript
// 求连续最长的字符及长度

  interface Ichar {
    char: string;
    length: number;
  }

    function getChar(str: string): Ichar {
    const res = {
      char: "",
      length: 0,
    };

    if (str.length === 0) return res;
    let temLength = 0; //记录当前字符连续最长的长度