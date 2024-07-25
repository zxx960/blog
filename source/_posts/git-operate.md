---
title: git常用操作
date: 2024-07-25 12:00:00
categories:
  - git
tags:
  - git
---

### 强推
```bash
git push origin <your-branch-name> --force
```

### 取消合并
```javascript
git merge --abort
```

### 合并指定commit
```javascript
git log  //查看提交的日志，复制要合并的那个分支的commit id(简略ID-前8位数)
git checkout 要合并的分支  // 切换到要合并的分支上
git cherry-pick 上面复制的那个要合并的commit id  // 提交该commit到当前分支
git push // 推送到B分支远程仓库
```

### vscode不显示远程分支
```javascript
git remote update origin --prune
```

### 强制拉取远程tag覆盖本地
```javascript
git fetch --tags -f
```




 