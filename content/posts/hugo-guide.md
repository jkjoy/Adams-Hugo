---
title: "Hugo 博客搭建完全指南"
date: 2024-01-15T10:30:00+08:00
draft: false
tags: ["Hugo", "教程", "建站"]
categories: ["技术"]
thumbnail: "https://picsum.photos/seed/hugo/400/300"
---

Hugo 是世界上最快的静态网站生成器之一，本文将带你了解如何快速搭建一个 Hugo 博客。

## 为什么选择 Hugo

1. **极快的构建速度** - 毫秒级生成网站
2. **简单易用** - 无需数据库，纯静态
3. **主题丰富** - 社区提供大量精美主题
4. **部署方便** - 支持 GitHub Pages、Netlify 等

<!--more-->

## 安装 Hugo

### Windows
```bash
choco install hugo-extended
```

### macOS
```bash
brew install hugo
```

### Linux
```bash
sudo apt-get install hugo
```

## 创建站点

```bash
hugo new site my-blog
cd my-blog
```

## 选择主题

推荐使用 Adams 主题，简洁优雅：

```bash
git clone https://github.com/yourusername/adams-hugo themes/adams
```

## 配置站点

编辑 `hugo.toml` 文件，设置网站基本信息和主题。

## 开始写作

```bash
hugo new posts/my-first-post.md
hugo server -D
```

就这么简单！开始你的博客之旅吧。
