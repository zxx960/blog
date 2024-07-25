---
title: decimal-eval解决精度问题
date: 2024-07-16 13:29:45
categories:
  - 编程
tags:
  - 编程
---
一个小巧、安全、快速的 JavaScript 库，用于计算算术表达式。

### 安装
```bash
pnpm install decimal-eval
```
### 引用
```javascript
import {evaluate} from 'decimal-eval';
```
### 常用例子
```javascript
evaluate('0.1 + 0.2') // '0.3'
evaluate('100 * (0.08 - 0.01)'); // '7'
evaluate('9007199254740992 + 1'); // '9007199254740993'
evaluate('1 + abc', { abc: 2 }); // '3'
```
### gitbub地址
```javascript
https://github.com/peakchen90/decimal-eval/blob/master/README.ZH-CN.md
```