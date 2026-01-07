# System Architecture

## Overview

```
┌─────────────────────────────────────────────────────────┐
│                    Cloudflare Pages                      │
│  ┌─────────────────────────────────────────────────────┐│
│  │                  Static Assets                       ││
│  │  (HTML, CSS, JS, Images, RSS Feed)                  ││
│  └─────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────┘
                           ▲
                           │ Deploy
                           │
┌─────────────────────────────────────────────────────────┐
│                    GitHub Repository                     │
│                      (main branch)                       │
└─────────────────────────────────────────────────────────┘
                           ▲
                           │ Push
                           │
┌─────────────────────────────────────────────────────────┐
│                   Local Development                      │
│  ┌─────────────────────────────────────────────────────┐│
│  │  Jekyll Build Process                                ││
│  │  ┌─────────┐  ┌─────────┐  ┌─────────┐             ││
│  │  │Markdown │→ │ Liquid  │→ │  HTML   │             ││
│  │  │ + YAML  │  │Templates│  │ Output  │             ││
│  │  └─────────┘  └─────────┘  └─────────┘             ││
│  │                    ↓                                 ││
│  │  ┌─────────┐  ┌─────────┐                           ││
│  │  │  SCSS   │→ │   CSS   │                           ││
│  │  └─────────┘  └─────────┘                           ││
│  └─────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────┘
```

## Build Pipeline

1. **Source Files**: Markdown content + YAML front matter
2. **Liquid Processing**: Templates render with site data
3. **SCSS Compilation**: Compressed CSS output
4. **Static Output**: `_site/` directory with all assets

## Deployment Flow

1. Push to `main` branch on GitHub
2. Cloudflare Pages auto-detects push
3. Runs `jekyll build` command
4. Deploys `_site/` to edge network
5. Available at kenlaam-blog.pages.dev

## Content Types

| Type | Source | Output |
|------|--------|--------|
| Pages | `*.md` | `/*.html` |
| Posts | `_posts/*.md` | `/blog/YYYY/MM/DD/title/` |
| Feed | Auto-generated | `/feed.xml` |

## External Dependencies

- **Google Fonts**: Inter, JetBrains Mono (preconnect optimized)
- **No JavaScript frameworks**: Pure static HTML/CSS
- **No build tools**: Jekyll handles everything
