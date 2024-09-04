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

### 取消合并(遇到冲突)
```bash
git merge --abort
```

### vscode不显示远程分支
```bash
git remote update origin --prune
```

### 强制拉取远程tag覆盖本地
```bash
git fetch --tags -f
```

### 合并指定commit
```bash
查看提交的日志，复制要合并的那个分支的commit id(SHA)

切换到要合并的分支上

git cherry-pick commitId  #提交该commit到当前分支

```




 
