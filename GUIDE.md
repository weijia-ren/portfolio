# Site Maintenance Guide

## Quick Reference — File Locations

```
~/portfolio-site/
├── hugo.toml                        # Site config (title, nav, social links)
├── static/css/style.css             # All styling
├── static/images/                   # Logo, images
├── layouts/                         # Page templates (HTML structure)
│   ├── index.html                   # Homepage
│   ├── _default/baseof.html         # Base wrapper (head, header, footer)
│   ├── _default/single.html         # Individual page layout
│   ├── _default/list.html           # Default list layout
│   ├── case-studies/list.html       # Case Studies page layout
│   ├── knowledge/list.html          # Knowledge Base page layout
│   ├── page/single.html             # About/Competencies layout
│   ├── partials/header.html         # Navigation bar
│   ├── partials/footer.html         # Footer
│   └── shortcodes/callout.html      # Callout boxes
└── content/                         # All your content (Markdown)
    ├── about/index.md
    ├── case-studies/
    ├── competencies/index.md
    ├── blog/
    └── knowledge/
        ├── statistics/
        ├── uxr-methods/
        ├── ai-innovation/
        ├── frameworks/
        ├── methods/
        ├── tools/
        ├── interview-prep/
        └── communication/
```

---

## 1. Adding Content

### Add a new case study

Create a file in `content/case-studies/`:

```bash
touch ~/portfolio-site/content/case-studies/my-new-project.md
```

Use this template:

```yaml
---
title: "Your Project Title"
date: 2026-03-01
draft: false
tags: ["tag1", "tag2", "tag3"]
categories: ["Category Name"]
icon: "📊"
weight: 7
---

## Context
What was the situation?

## Question
What were you trying to answer?

## Approach
What did you do? (bullet points work well)

## Key Findings
1. Finding one
2. Finding two
3. Finding three

## Impact
What changed because of this work?

## Methods & Tools
`Method 1` · `Method 2` · `Tool 1`

## What This Demonstrates
Why does this matter for your career?
```

**Note:** The `weight` field controls the order (1 = first). Update other case studies' weights if you want to reorder.

### Add a new blog post

```bash
touch ~/portfolio-site/content/blog/my-post.md
```

Template:

```yaml
---
title: "Post Title"
date: 2026-03-01
draft: false
tags: ["topic1", "topic2"]
categories: ["Category"]
---

Your content here. Use `<!--more-->` to set where the summary cuts off.

<!--more-->

Rest of the post...
```

### Add a new knowledge base article

Create in the appropriate subfolder:

```bash
# Example: new statistics article
touch ~/portfolio-site/content/knowledge/statistics/my-topic.md
```

Template:

```yaml
---
title: "Topic Name"
date: 2026-03-01
draft: false
tags: ["tag1", "tag2"]
---

Content here...
```

### Add a new knowledge base section

1. Create the folder:
```bash
mkdir ~/portfolio-site/content/knowledge/new-section
```

2. Create `_index.md` inside it:
```yaml
---
title: "Section Name"
subtitle: "Brief description of this section."
icon: "🆕"
---
```

3. Add articles inside the folder.

### Hide content (drafts)

Set `draft: true` in any file's front matter. It won't appear on the live site but will show locally with `hugo server -D`.

---

## 2. Preview → Push Workflow

Every time you make changes:

```bash
# 1. Preview locally
cd ~/portfolio-site && hugo server -D

# 2. Open http://localhost:1313/portfolio/ in browser

# 3. When happy, stop server (Ctrl+C) and push
git add .
git commit -m "Description of what you changed"
git push
```

Site auto-deploys in ~1 minute after push.

---

## 3. Design Changes

### Colors
Edit the CSS custom properties at the top of `static/css/style.css`:

```css
:root {
  --color-bg: #ffffff;          /* Page background */
  --color-bg-alt: #f8f9fa;      /* Alternate section background */
  --color-text: #1a1a2e;        /* Main text */
  --color-text-light: #555;     /* Secondary text */
  --color-accent: #2563eb;      /* Links, buttons */
  --color-accent-hover: #1d4ed8;
  --color-border: #e5e7eb;      /* Borders */
  --color-tag-bg: #eef2ff;      /* Tag background */
  --color-tag-text: #3730a3;    /* Tag text */
}
```

### Fonts
Change the Google Fonts import in `layouts/_default/baseof.html` and update `--font-sans` / `--font-serif` in the CSS.

### Navigation
Edit `[menu]` in `hugo.toml` to add/remove/reorder nav items.

### Logo
Replace `static/images/logo.svg` and `static/favicon.svg`.

---

## 4. Working with AI Assistants

When asking an AI (Claude, ChatGPT, etc.) to help with your site, give them this context:

### For content changes:
```
I have a Hugo static site. The content is in Markdown files at:
~/portfolio-site/content/

I want to [add/edit/remove] [what].
The file is at [path] (or should be created at [path]).
```

### For design changes:
```
I have a Hugo static site with a custom theme (no external theme).
- All CSS is in: static/css/style.css
- HTML templates are in: layouts/
- The site is deployed at: https://weijia-ren.github.io/portfolio/

I want to change [describe what you want].
```

### For troubleshooting:
```
My Hugo site at ~/portfolio-site is showing [problem].
- Hugo version: [run `hugo version`]
- Error message: [paste it]
- Config: hugo.toml at the root
```

### Useful commands to share with AI:
```bash
# Show full file tree
find ~/portfolio-site -name "*.md" -o -name "*.html" -o -name "*.css" -o -name "*.toml" | sort

# Show current config
cat ~/portfolio-site/hugo.toml

# Build and show errors
cd ~/portfolio-site && hugo

# Check deploy status
gh run list --repo weijia-ren/portfolio --limit 3
```

---

## 5. Common Tasks Cheat Sheet

| Task | Command |
|------|---------|
| Preview locally | `cd ~/portfolio-site && hugo server -D` |
| Build (check errors) | `cd ~/portfolio-site && hugo` |
| Push to live | `git add . && git commit -m "msg" && git push` |
| Check deploy status | `gh run list --repo weijia-ren/portfolio --limit 3` |
| Create new content | Create `.md` file in the right `content/` subfolder |
| Change nav menu | Edit `[menu]` in `hugo.toml` |
| Change colors | Edit `:root` variables in `static/css/style.css` |
| Change page title | Edit `title` in `hugo.toml` |
| Add social links | Fill in `linkedin`, `github`, `email` in `hugo.toml` |
