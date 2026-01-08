# 快速开始 / Quick Start Guide

5 分钟内让你的个人网站上线！

## 📋 准备工作

1. 一个 GitHub 账号
2. Git 已安装
3. 一个文本编辑器（VSCode、Sublime 等）

---

## 🚀 五步上手

### 第一步：Fork 本仓库

1. 访问 [personal-website-template](https://github.com/yourusername/personal-website-template)
2. 点击右上角 **Fork** 按钮
3. 将仓库重命名为 `<你的用户名>.github.io`
   - 例如：你的用户名是 `john`，则命名为 `john.github.io`
   - 这样你的网站地址就是 `https://john.github.io/`

### 第二步：克隆到本地

```bash
# 替换为你自己的仓库地址
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

### 第三步：修改基本配置

编辑 `contents/config.yml`：

```yaml
title: 你的名字 - 个人主页
page-top-title: 你的名字
home-subtitle: 你的职位 | 你的学校/公司
copyright-text: '&copy; 你的名字 2023-2026. All Rights Reserved.'
```

### 第四步：修改首页内容

编辑 `contents/home.md`，替换为你的个人信息：

```markdown
[![GitHub](https://img.shields.io/badge/GitHub-你的用户名-blue?logo=github)](https://github.com/你的用户名)

我是 XXX，目前在 XXX 攻读硕士学位。

#### 联系方式
<code>your@email.com</code>

#### 教育背景
**XXX 大学**，XXX 学位（20XX - 20XX）
```

### 第五步：推送部署

```bash
# 添加所有更改
git add .

# 提交（用英文描述）
git commit -m "Initial: update my info"

# 推送到 GitHub
git push
```

### 第六步：等待部署

1. 访问 `https://<你的用户名>.github.io/`（可能需要几分钟）
2. 如果没更新，清除浏览器缓存或尝试硬刷新 `Ctrl+Shift+R`

---

## 📁 目录结构速览

```
├── contents/              # 内容文件
│   ├── config.yml        # 网站配置
│   ├── home.md           # 首页个人简介
│   ├── news.md           # 新闻动态
│   ├── awards.md         # 奖项荣誉
│   ├── experience.md     # 工作经历
│   ├── publications.md   #  publications
│   └── blog/             # 博客系统
│       ├── articles.yml  # 文章索引
│       └── *.md          # 文章文件
├── static/               # 静态资源
│   ├── css/              # 样式文件
│   ├── js/               # JavaScript 文件
│   └── assets/img/       # 图片（头像、背景）
├── index.html            # 首页
└── blog.html             # 博客页面
```

---

## ❓ 常见问题

### Q: 怎么修改头像？
A: 替换 `static/assets/img/photo.png` 为你的照片（建议正方形，400x400 以上）

### Q: 怎么修改背景图？
A: 替换 `static/assets/img/background.jpeg` 为你的背景图

### Q: 怎么添加新板块？
A: 参考 [FEATURE_GUIDE.md](FEATURE_GUIDE.md) 中的"添加自定义板块"部分

### Q: 本地怎么预览？
A:
```bash
# Python 3
python -m http.server 8000

# 访问 http://localhost:8000
```

---

## ➡️ 下一步

- [功能使用详解](FEATURE_GUIDE.md) - 了解所有功能
- [进阶自定义](ADVANCED.md) - 深度定制你的网站
