# 进阶自定义 / Advanced Customization

高级用户指南，教你如何深度定制网站。

## 📋 目录

- [添加新板块](#添加新板块)
- [修改导航栏](#修改导航栏)
- [添加统计分析](#添加统计分析)
- [SEO 优化](#seo-优化)
- [多语言支持](#多语言支持)

---

## ➕ 添加新板块

### 1. 修改 index.html

在 `<body>` 中添加新板块：

```html
<!-- 新板块名称 -->
<section id="your-section-id" class="bg-gradient-primary-to-secondary-light mt-5">
    <div class="container px-5">
        <header>
            <h2><i class="bi bi-star-fill"></i> 新板块名称</h2>
        </header>
        <div class="main-body" id="your-section-md"></div>
    </div>
</section>
```

### 2. 修改导航栏

在导航栏 `<ul>` 中添加链接：

```html
<li class="nav-item">
    <a class="nav-link me-lg-3" href="#your-section-id">板块名</a>
</li>
```

### 3. 修改 JavaScript

编辑 `static/js/scripts.js`，在 `section_names` 数组中添加：

```javascript
const section_names = ['home', 'news', 'awards', 'experience', 'publications', 'your-section-id'];
```

### 4. 创建内容文件

创建 `contents/your-section.md`，写入内容。

---

## 🔗 修改导航栏

### 隐藏不需要的链接

删除 `<ul>` 中对应的 `<li>` 元素。

### 修改导航栏样式

在 `static/css/main.css` 中：

```css
/* 导航栏背景 */
.header {
    background-color: #fff;
}

/* 导航链接颜色 */
.nav-link {
    color: #333;
}
```

### 添加下拉菜单

```html
<li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">
        更多
    </a>
    <ul class="dropdown-menu">
        <li><a class="dropdown-item" href="#">项目 1</a></li>
        <li><a class="dropdown-item" href="#">项目 2</a></li>
    </ul>
</li>
```

---

## 📊 添加统计分析

### Google Analytics

在 `index.html` 的 `<head>` 中添加：

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Cloudflare Analytics

在 `index.html` 的 `<body>` 末尾添加：

```html
<script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "YOUR_TOKEN"}'></script>
```

---

## 🔍 SEO 优化

### Meta 标签

修改 `index.html` 中的 description：

```html
<meta name="description" content="你的网站描述，简洁说明你的身份和研究方向。">
```

### Open Graph 标签（社交分享预览）

```html
<meta property="og:title" content="你的名字 - 个人主页">
<meta property="og:description" content="你的网站描述">
<meta property="og:image" content="https://yourdomain.com/static/assets/img/photo.png">
<meta property="og:url" content="https://yourdomain.com/">
```

### Sitemap

创建 `sitemap.xml`：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://yourdomain.com/</loc>
        <changefreq>monthly</changefreq>
        <priority>1.0</priority>
    </url>
    <url>
        <loc>https://yourdomain.com/blog.html</loc>
        <changefreq>weekly</changefreq>
        <priority>0.8</priority>
    </url>
</urlset>
```

---

## 🌐 多语言支持

### 方案一：中英文双版本

创建两个版本的文件：
- `contents/home.md`（中文）
- `contents/home-en.md`（英文）

在导航栏添加语言切换：

```html
<li class="nav-item">
    <a class="nav-link" href="?lang=zh">中文</a>
</li>
<li class="nav-item">
    <a class="nav-link" href="?lang=en">EN</a>
</li>
```

### 方案二：纯英文模板

如果需要纯英文版本：
1. 将 `config.yml` 中的中文改为英文
2. 将各 `.md` 文件内容改为英文
3. 修改 `index.html` 语言：`lang="en"`

---

## 🚀 性能优化

### 图片优化

- 使用 WebP 格式（比 JPEG/PNG 小 30-50%）
- 压缩图片：https://squoosh.app
- 适当尺寸：不要上传过大的图片

### 缓存配置

在仓库根目录创建 `.nojekyll` 文件（GitHub Pages 缓存控制）。

### 懒加载图片

```html
<img src="placeholder.jpg" data-src="real-image.jpg" class="lazy" alt="描述">
<script>
document.addEventListener('DOMContentLoaded', function() {
    const lazyImages = document.querySelectorAll('.lazy');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.src = entry.target.dataset.src;
                observer.unobserve(entry.target);
            }
        });
    });
    lazyImages.forEach(img => observer.observe(img));
});
</script>
```

---

## 🔧 故障排除

### 问题：修改后页面没更新

**解决**：
1. 清除浏览器缓存 `Ctrl+Shift+R`
2. 等待 GitHub Pages 部署完成（通常 1-2 分钟）
3. 强制刷新：`Ctrl+F5`

### 问题：图片不显示

**解决**：
1. 检查图片路径是否正确
2. 确认图片文件存在
3. 检查文件名大小写

### 问题：数学公式不渲染

**解决**：
1. 确保 MathJax 已加载
2. 检查公式语法：`$...$` 或 `$$...$$`
3. 等待页面完全加载后查看

---

## 📚 更多资源

- [Bootstrap 5 文档](https://getbootstrap.com/docs/5.3/)
- [Markdown 语法](https://www.markdownguide.org/)
- [MathJax 文档](https://docs.mathjax.org/)
- [GitHub Pages 文档](https://docs.github.com/en/pages)
