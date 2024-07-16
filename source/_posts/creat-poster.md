---
title: 使用html2canvas生成海报
date: 2024-07-16 15:29:45
categories:
  - 编程
tags:
  - 编程
---

使用 html2canvas 和 qrcode 生成带二维码的海报

### 安装

```bash
pnpm install qrcode
```

### 生成二维码

```javascript
import QRCode from "qrcode";

function generateQRCode() {
  let url = `www.baidu.com`;
  QRCode.toDataURL(url, { margin: 1 }).then((url) => {
    console.log(url);
  });
}
```

### 引入本地文件
<a download href='../assets/html2canvas.js'>下载 html2canvas</a>
```javascript
import html2canvas from '@/utils/html2canvas.js'

function downImg() {
  //posterBox一定要唯一，否则会生成失败
  html2canvas(document.querySelector('#poster'), { 
    dpi: 300, // 或适当更高的值以提升清晰度
    scale: devicePixelRatio, // 自动适应高DPI屏幕
    useCORS: true //配置允许跨域
  })
    .then(canvas => {
      var dataURL = canvas.toDataURL()
      this.$app.app.SavePhotosAlbum(dataURL)
    })
    .catch(err => {
      console.error(err)
    })
}
```
