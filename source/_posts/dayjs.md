---
title: dayjs常用操作
date: 2024-07-16 12:29:45
categories:
  - 编程
tags:
  - 编程
---
dayjs 是一个轻量级的 JavaScript 日期库，可以用来解析、验证、操作和显示日期和时间。以下是安装、引用以及一些常用操作的介绍：

### 安装
```bash
pnpm install dayjs
```
### 引用
```javascript
import dayjs from 'dayjs'
```
### 常用操作
获取当前日期和时间
```javascript
const now = dayjs();
console.log(now.format());  // 输出当前日期和时间，格式为 "YYYY-MM-DDTHH:mm:ssZ"
```

格式化日期
```javascript
const formattedDate = dayjs().format('YYYY-MM-DD');
console.log(formattedDate);  // 输出当前日期，格式为 "YYYY-MM-DD"
```

解析日期
```javascript
const date = dayjs('2024-07-16');
console.log(date.format());  // 输出 "2024-07-16T00:00:00Z"
```

日期加减
```javascript
const tomorrow = dayjs().add(1, 'day');
console.log(tomorrow.format('YYYY-MM-DD'));  // 输出明天的日期

const lastMonth = dayjs().subtract(1, 'month');
console.log(lastMonth.format('YYYY-MM-DD'));  // 输出上个月的日期
```

获取日期信息
```javascript
const year = dayjs().year();
const month = dayjs().month();  // 月份从0开始，0表示一月
const day = dayjs().date();
console.log(`Year: ${year}, Month: ${month + 1}, Day: ${day}`);  // 输出当前的年、月、日
```

日期比较
```javascript
const date1 = dayjs('2024-07-16');
const date2 = dayjs('2024-08-16');

const isBefore = date1.isBefore(date2);  // true
const isAfter = date1.isAfter(date2);    // false
const isSame = date1.isSame(date2);      // false

console.log(`Is before: ${isBefore}, Is after: ${isAfter}, Is same: ${isSame}`);
```
### 插件
dayjs 支持多种插件，可以通过插件扩展其功能。比如，如果你需要处理相对时间，可以安装和使用 relativeTime 插件：
```javascript
// 安装插件
npm install dayjs-plugin-relativeTime

// 引入并使用插件
import relativeTime from 'dayjs/plugin/relativeTime';
dayjs.extend(relativeTime);

const relative = dayjs().from(dayjs('2024-07-16'));  // 例如 "in 2 months"
console.log(relative);
```







