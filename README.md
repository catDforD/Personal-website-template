# Personal Website with Blog / 个人主页 + 博客模板

[![GitHub stars](https://img.shields.io/github/stars/yourusername/personal-website-template?style=flat)](https://github.com/yourusername/personal-website-template)
[![GitHub forks](https://img.shields.io/github/forks/yourusername/personal-website-template?style=flat)](https://github.com/yourusername/personal-website-template)
[![License](https://img.shields.io/github/license/yourusername/personal-website-template?style=flat)](LICENSE)

A personal homepage + blog template built with pure HTML/CSS/JS, deployable on GitHub Pages. Features include responsive design, Markdown support, math formulas, and a complete blog system.

一个基于纯 HTML/CSS/JS 的个人主页 + 博客模板，可部署在 GitHub Pages 上。特点包括响应式设计、Markdown 支持、数学公式，以及完整的博客系统。

![Screenshot](screenshot.png)

## ✨ Features / 功能特点

- **🏠 Personal Homepage / 个人主页**
  - Home section with bio / 首页个人简介
  - News updates / 新闻动态
  - Awards and achievements / 奖项荣誉
  - Work experience / 工作经历
  - Publications list /  publications 列表

- **📝 Blog System / 博客系统**
  - Article list with filtering / 文章列表（支持筛选）
  - Category and tag support / 分类和标签
  - Search functionality / 搜索功能
  - Full-page article view / 全页面文章阅读

- **🎨 Rich Content Support / 丰富内容支持**
  - Markdown syntax / Markdown 语法
  - MathJax formulas / MathJax 数学公式
  - Code highlighting / 代码高亮
  - Responsive design / 响应式设计

- **⚡ Easy Deployment / 轻松部署**
  - Pure static files / 纯静态文件
  - No build process needed / 无需构建
  - GitHub Pages ready / 支持 GitHub Pages

## 🚀 Quick Start / 快速开始

### Step 1: Fork this repository / Fork 本仓库

1. Click the **Fork** button on the top right
2. Rename the repository to `<username>.github.io`
   - Your site will be at `https://<username>.github.io/`

### Step 2: Clone locally / 克隆到本地

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

### Step 3: Configure your info / 配置你的信息

Edit `contents/config.yml`:

```yaml
title: Your Name's Homepage
page-top-title: Your Name
home-subtitle: Your Title | Your Department, University
copyright-text: '&copy; Your Name 2023-2026. All Rights Reserved.'
```

### Step 4: Customize content / 自定义内容

Edit files in `contents/`:
- `home.md` - Your bio / 个人简介
- `news.md` - News updates / 新闻动态
- `awards.md` - Awards / 奖项
- `experience.md` - Experience / 经历
- `publications.md` - Publications / publications

### Step 5: Add your photo / 添加头像

Replace `static/assets/img/photo.png` with your photo.

### Step 6: Update background / 更新背景图

Replace `static/assets/img/background.jpeg` with your background image.

### Step 7: Deploy / 部署

```bash
git add .
git commit -m "Update my website"
git push
```

### Step 8: Github Pages
- Under your repository name, click Settings.
- In the "Code and automation" section of the sidebar, click Pages.
- Under "Build and deployment", under "Source", select Deploy from a branch. Then, use the branch dropdown menu and select a publishing source.


Your site will be live at `https://<username>.github.io/` in a few minutes.

## 📖 Documentation / 文档

- [Quick Start Guide](QUICKSTART.md) - 5 分钟上手
- [Feature Guide](FEATURE_GUIDE.md) - 功能使用详解
- [Advanced Customization](ADVANCED.md) - 进阶自定义

## 📝 Blog Management / 博客管理

### Add a new article / 添加新文章

1. Create a new `.md` file in `contents/blog/`:
   ```markdown
   # Your Article Title
   
   Your article content here...
   ```

2. Add article entry to `contents/blog/articles.yml`:
   ```yaml
   - id: "your-article-id"
     title: "Your Article Title"
     date: "2025-01-25"
     category: "Your Category"
     tags: ["Tag1", "Tag2"]
     summary: "Article summary..."
     file: "2025-01-25-your-article.md"
   ```

### Supported Markdown / 支持的 Markdown

- Headers, lists, links, images
- Code blocks with syntax highlighting
- Blockquotes, tables
- **Math formulas** with `$...$` and `$$...$$`

## 🙏 Credits / 致谢

- Original template by [Sen Li](https://github.com/senli1073)
- Bootstrap 5 for styling
- Marked.js for Markdown parsing
- MathJax for math formulas
- js-yaml for YAML parsing

## 📄 License / 许可证

MIT License - feel free to use and modify.

---

Made with ❤️ for the community
