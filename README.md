# Case Studies & Knowledge Base

Personal website built with Hugo. Showcases research expertise (Layer A) and serves as a structured knowledge base (Layer B).

## Quick Start

### 1. Install Hugo

```bash
# macOS
brew install hugo

# Or download directly from https://github.com/gohugoio/hugo/releases
```

You need Hugo **extended** edition (v0.120+).

### 2. Preview locally

```bash
cd portfolio-site
hugo server -D
```

Open http://localhost:1313 in your browser. The `-D` flag shows draft content.

### 3. Deploy to GitHub Pages (free)

1. Create a GitHub repo named `yourusername.github.io` (or any name)
2. Push this project:

```bash
cd portfolio-site
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

3. In GitHub: **Settings → Pages → Source** → select "GitHub Actions"
4. The included `.github/workflows/hugo.yml` will auto-build and deploy on every push

### 4. Custom domain (optional, ~$12/year)

1. Buy a domain (Namecheap, Cloudflare, Google Domains)
2. In GitHub: **Settings → Pages → Custom domain** → enter `yourname.com`
3. Add DNS records per [GitHub's instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
4. Update `baseURL` in `hugo.toml` to `https://yourname.com/`

## Site Structure

```
content/
├── about/              # Layer A: Who you are
├── case-studies/       # Layer A: Case studies
├── competencies/       # Layer A: Skills grid
├── blog/               # Layer A: Public writing (2 starter posts)
└── knowledge/          # Layer B: Personal second brain
    ├── frameworks/     #   Mental models & approaches
    ├── methods/        #   Statistical & research methods notes
    ├── tools/          #   Tool/tech reference notes
    └── interview-prep/ #   STAR stories for interviews
```

## Adding Content

### New blog post

```bash
hugo new blog/my-post-title.md
```

Or just create a markdown file in `content/blog/` with frontmatter:

```yaml
---
title: "My Post Title"
date: 2025-10-01
draft: false
tags: ["topic1", "topic2"]
---
```

### New case study

Create a file in `content/case-studies/`:

```yaml
---
title: "Project Title"
date: 2025-10-01
tags: ["method1", "method2"]
categories: ["Quantitative UXR"]
icon: "📊"
weight: 4
---

## Context
## Question
## Method
## Key Findings
## Impact
## Methods Used
```

### New knowledge base note

Create a file in the appropriate `content/knowledge/` subfolder. Same markdown format.

### Callout shortcode

Use in any markdown file:

```markdown
{{< callout type="insight" title="Key Insight" >}}
Your insight text here.
{{< /callout >}}
```

Types: `insight` (blue), `method` (green), `warning` (yellow), `note` (gray).

## Customization

- **Colors/fonts**: Edit `static/css/style.css` — all values are in CSS custom properties at the top
- **Navigation**: Edit `[menu]` in `hugo.toml`
- **Site title/description**: Edit `[params]` in `hugo.toml`
- **Social links**: Fill in `linkedin`, `github`, `email` etc. in `hugo.toml`
- **Hide knowledge base from nav**: Set `showKnowledgeBase = false` in `hugo.toml` (pages still accessible by URL)

## Content Tips

- Mark posts as `draft: true` to hide them from the public site (still visible with `hugo server -D`)
- Use `weight` in case study items to control display order on the home page
- Tags create automatic tag pages at `/tags/topic-name/`
- All content is plain markdown — easy to edit in any text editor or IDE
