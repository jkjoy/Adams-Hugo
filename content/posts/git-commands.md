---
title: "Git 常用命令速查"
date: 2023-11-15T14:30:00+08:00
draft: false
tags: ["Git", "版本控制", "命令"]
categories: ["技术"]
thumbnail: "https://picsum.photos/seed/git/400/300"
---

Git 是最流行的版本控制系统，这里整理了常用的 Git 命令。

## 配置

```bash
# 设置用户名和邮箱
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# 查看配置
git config --list
```

<!--more-->

## 基本操作

```bash
# 初始化仓库
git init

# 克隆仓库
git clone <url>

# 查看状态
git status

# 添加文件
git add <file>
git add .

# 提交
git commit -m "commit message"

# 推送
git push origin main

# 拉取
git pull origin main
```

## 分支操作

```bash
# 查看分支
git branch

# 创建分支
git branch <branch-name>

# 切换分支
git checkout <branch-name>

# 创建并切换分支
git checkout -b <branch-name>

# 合并分支
git merge <branch-name>

# 删除分支
git branch -d <branch-name>
```

## 撤销操作

```bash
# 撤销工作区修改
git checkout -- <file>

# 撤销暂存区修改
git reset HEAD <file>

# 撤销提交
git reset --soft HEAD^

# 查看提交历史
git log
git log --oneline
```

## 远程仓库

```bash
# 查看远程仓库
git remote -v

# 添加远程仓库
git remote add origin <url>

# 删除远程仓库
git remote remove origin
```

## 标签

```bash
# 创建标签
git tag v1.0.0

# 查看标签
git tag

# 推送标签
git push origin v1.0.0
```

## 实用技巧

```bash
# 暂存当前修改
git stash

# 恢复暂存
git stash pop

# 查看差异
git diff

# 美化日志
git log --graph --oneline --all
```

掌握这些命令，日常使用 Git 就没问题了！
