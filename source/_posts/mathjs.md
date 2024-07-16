---
title: mathjs解决精度问题
date: 2024-07-16 13:29:45
categories:
  - 编程
tags:
  - 编程
---
使用mathjs的表达式方法可以比较优雅的解决精度问题

### 安装
```bash
pnpm install mathjs
```
### 引用
```javascript
import { create, all } from 'mathjs';
```
### 创建mathjs实例
```javascript
const mathjs = create(all);

mathjs.config({
  number: "BigNumber",
});

const result1 = mathjs.evaluate("0.1 + 0.2");
console.log(result1.toString()); // 输出0.3
```