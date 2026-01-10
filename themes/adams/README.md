# Adams Hugo 主题

这是从 WordPress Adams 主题移植到 Hugo 的版本，保留了原主题的所有视觉效果。

## 特性

- ✅ 简洁优雅的设计
- ✅ 三种主题模式（默认/护眼/夜间）
- ✅ 完全响应式布局
- ✅ 代码高亮支持
- ✅ 三种评论系统可选（Twikoo/Artalk/Gitalk）
- ✅ PJAX 无刷新加载
- ✅ 图片查看器
- ✅ 时间相对显示

## 快速开始

### 1. 安装

```bash
cd your-hugo-site
git clone https://github.com/yourusername/adams-hugo themes/adams
```

### 2. 配置

编辑 `hugo.toml` 文件，设置主题：

```toml
theme = "adams"
```

### 3. 评论系统配置

在 `hugo.toml` 中选择并配置评论系统：

**使用 Twikoo：**

```toml
[params.comments]
  system = "twikoo"
  [params.comments.twikoo]
    envId = "https://your-twikoo-url"
    lang = "zh-CN"
```

**使用 Artalk：**

```toml
[params.comments]
  system = "artalk"
  [params.comments.artalk]
    server = "https://your-artalk-server"
    site = "我的站点"
```

**使用 Gitalk：**

```toml
[params.comments]
  system = "gitalk"
  [params.comments.gitalk]
    clientID = "your-github-client-id"
    clientSecret = "your-github-client-secret"
    repo = "your-repo"
    owner = "your-github-username"
    admin = ["your-github-username"]
```

### 4. 创建内容

```bash
hugo new posts/my-first-post.md
```

### 5. 本地预览

```bash
hugo server -D
```

访问 http://localhost:1313

## 配置说明

详细的配置选项请查看 `hugo.toml` 文件中的注释。

## 原版主题

本主题移植自 [Adams WordPress Theme](https://github.com/Tokinx/Adams)

## 许可证

MIT License
