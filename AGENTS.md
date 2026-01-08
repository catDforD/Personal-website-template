# AGENTS.md - Agentic Coding Guidelines

This is a static personal website template using pure HTML/CSS/JS with Bootstrap 5, forked from [senli1073/academic-homepage-template](https://github.com/senli1073/academic-homepage-template). Deploy via GitHub Pages.

## Project Structure

```
├── contents/              # Content files (YAML + Markdown)
│   ├── config.yml         # Main site configuration
│   ├── home.md            # Homepage bio content
│   ├── news.md            # News updates
│   ├── awards.md          # Awards section
│   ├── experience.md      # Work experience
│   ├── publications.md    # Publications list
│   └── blog/
│       ├── articles.yml   # Blog article index
│       └── *.md           # Blog articles
├── static/                # Static assets
│   ├── css/
│   │   ├── styles.css     # Custom styles (Bootstrap-based)
│   │   └── main.css       # Additional styles
│   ├── js/
│   │   ├── scripts.js     # Main site logic (YAML loading, Markdown rendering)
│   │   ├── blog.js        # Blog system (articles list, filtering, routing)
│   │   ├── marked.min.js  # Markdown parser
│   │   ├── jsyaml.min.js  # YAML parser
│   │   ├── bootstrap.bundle.min.js
│   │   └── mathjax setup
│   └── assets/
│       ├── img/photo.png  # Profile photo
│       └── img/background.jpeg
├── index.html             # Main homepage
└── blog.html              # Blog page
```

## Build/Lint/Test Commands

**No build process required.** This is a pure static site.

- **Preview locally**: Open `index.html` directly in browser, or serve via any static server:
  ```bash
  # Python
  python -m http.server 8000
  # Node.js (npx)
  npx serve .
  # PHP
  php -S localhost:8000
  ```

- **GitHub Pages URL format**:
  - User site: `https://<username>.github.io/`
  - Project site: `https://<username>.github.io/<repo-name>/`

## GitHub Pages Setup Guide

### Option 1: User Site (Recommended)

1. Fork this repository to your GitHub account
2. Rename to `<username>.github.io` (replace `<username>` with your GitHub username)
3. Site available at `https://<username>.github.io/`

### Option 2: Project Site

1. Fork repository (keep original name)
2. Rename to your preferred project name (e.g., `my-website`)
3. Site URL: `https://<username>.github.io/<project-name>/`

### Configure GitHub Pages

1. Go to repository **Settings** → **Pages**
2. Under "Build and deployment" → "Source": Select **Deploy from a branch**
3. Under "Branch": Select **main** and folder **/(root)**
4. Click **Save** (can take up to 10 minutes to deploy)

### Verify Deployment

- Check **Actions** tab for deployment status
- Settings → Pages shows "Your site is live at https://..."

## Code Style Guidelines

### JavaScript (ES6+)

- **Use `const` by default**, `let` only when reassignment needed
- **Prefer `const` configuration objects** at module top (see `BLOG_CONFIG` in `blog.js`)
- **Use arrow functions** for callbacks and short functions
- **Use `async/await` for async operations** (see `blog.js` patterns)
- **Use `document.addEventListener('DOMContentLoaded', ...)`** for initialization
- **CamelCase for variables/functions**: `loadArticlesIndex`, `filteredArticles`
- **PascalCase for constants/config objects**: `BLOG_CONFIG`
- **Handle errors gracefully**: Always wrap async operations in try/catch, log meaningful messages
- **DOM manipulation**: Use `classList.add/remove` for visibility toggling (e.g., `d-none` Bootstrap class)

### CSS

- **Bootstrap classes preferred**: `col-12`, `d-none`, `shadow-sm`, `text-primary`
- **Custom CSS in `styles.css`**: Extend Bootstrap, override theme variables in `:root`
- **Bootstrap CSS variables** follow `--bs-{color}` pattern
- **Custom classes use BEM-lite**: `article-card-*`, `blog-tag`, `display-top`

### HTML

- **Bootstrap 5 components** for layout: grid (`row`, `col-*`), cards, alerts, navbar
- **Data attributes for JS hooks**: Use `id` attributes for DOM selection
- **Semantic HTML**: `<header>`, `<main>`, `<section>`, `<footer>`
- **Bootstrap icons**: `<i class="bi bi-folder"></i>` format

### YAML

- **Use dashes for lists**: `- item` (not `* item`)
- **String values quoted** only if containing special chars: `copyright-text: '&copy; ...'`
- **Consistent indentation**: 2 spaces per level

### Markdown (Content Files)

- **Standard GitHub Flavored Markdown**: Headers, lists, links, images, code blocks
- **Math formulas**: `$...$` for inline, `$$...$$` for block (MathJax)
- **Front matter**: None required - metadata in `articles.yml`

## Naming Conventions

| Type | Convention | Examples |
|------|------------|----------|
| Variables | camelCase | `allArticles`, `tagSearch` |
| Functions | camelCase | `loadArticlesIndex`, `formatDate` |
| Config objects | PascalCase | `BLOG_CONFIG` |
| CSS classes | kebab-case | `article-card-meta`, `blog-tag` |
| File names | kebab-case | `blog.js`, `styles.css`, `home.md` |
| Article IDs | kebab-case | `my-first-post`, `2025-01-25-article` |

## Error Handling

- **Always wrap async operations** in try/catch
- **Log meaningful error messages**: `console.error('博客加载失败:', error)`
- **Show user-friendly messages** in UI for critical failures
- **Graceful degradation**: Hide failed sections, show fallback content

## Key External Libraries

- **Bootstrap 5.2.3**: CSS framework (grid, components, utilities)
- **Marked.js**: Markdown → HTML parsing
- **js-yaml**: YAML parsing in browser
- **MathJax**: Math formula rendering (`$...$`, `$$...$$`)

## Adding New Features

1. **New JS functionality**: Add to `static/js/scripts.js` or create new file
2. **New pages**: Create HTML file in root, include Bootstrap + common header/footer
3. **New blog categories**: Update `blog.js` filter logic if needed
4. **Styling changes**: Edit `static/css/styles.css`, use Bootstrap utilities first

## Content Editing Workflow

1. Edit `contents/config.yml` for site configuration
2. Edit `contents/*.md` for main page content
3. Add blog articles: create `.md` file in `contents/blog/`, add entry to `articles.yml`
4. Commit and push to auto-deploy

## Deployment Troubleshooting

| Issue | Solution |
|-------|----------|
| Site not updating | Wait up to 10 minutes after push |
| 404 error | Check repository name matches pattern |
| CSS/JS not loading | Ensure files in root directory, not `/docs` |
| Custom domain | Configure in Settings → Pages → Custom domain |
| SSL not working | Enable "Enforce HTTPS" in Pages settings |


## Github 推送注意事项
- 请使用中文规范编写commit message