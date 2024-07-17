---
title: 设置npm源
date: 2024-07-17 12:00:00
categories:
  - 编程
tags:
  - 编程
---

### 设置npm源
```bash
npm config get registry   #查看npm源

npm config set registry https://registry.npmmirror.com/   #设置成淘宝镜像

npm config set registry https://registry.npmjs.org/   #恢复成npm官方镜像
```

### .npmrc模板

<!-- <a download href='../assets/html2canvas.js'>下载 html2canvas</a> -->
在项目根目录下创建.npmrc文件，内容如下：

```bash
shamefully-hoist=true
strict-peer-dependencies=false
sentrycli_cdnurl=https://cdn.npmmirror.com/binaries/sentry-cli
#ELECTRON 相关镜像
chromedriver_cdnurl=https://npmmirror.com/mirrors/chromedriver
phantomjs_cdnurl=http://npmmirror.com/mirrors/phantomjs
operadriver_cdnurl=http://npmmirror.com/mirrors/operadriver
ELECTRON_MIRROR=https://npmmirror.com/mirrors/electron/
ELECTRON_BUILDER_BINARIES_MIRROR=http://npmmirror.com/mirrors/electron-builder-binaries/
# SASS 淘宝镜像
SASS_BINARY_SITE=http://npmmirror.com/mirrors/node-sass
engine-strict = true
registry=https://registry.npmmirror.com/
resolution-mode=highest
```
