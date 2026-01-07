# Ken Laam Blog

Personal blog and portfolio site built with Jekyll. Deployed on Cloudflare Pages.

**Live**: [kenlaam-blog.pages.dev](https://kenlaam-blog.pages.dev)

## Quick Start

### Prerequisites

- Ruby 3.2.2 (check `.ruby-version`)
- Bundler

```bash
# Install Ruby (if needed)
rvm install ruby-3.2.2
# or: rbenv install 3.2.2

# Install dependencies
bundle install
```

### Local Development

```bash
# Start dev server with live reload
bundle exec jekyll serve --livereload

# Site available at http://localhost:4000
```

### Build for Production

```bash
bundle exec jekyll build

# Output in _site/ directory
```

## Deploy to Cloudflare Pages

Automatic deployment on push to `main` branch.

### Manual Deploy (CLI)

```bash
# Install Wrangler CLI
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Deploy
wrangler pages deploy _site --project-name=kenlaam-blog
```

### Cloudflare Pages Settings

| Setting | Value |
|---------|-------|
| Build command | `bundle exec jekyll build` |
| Build output | `_site` |
| Root directory | `/` |

## Project Structure

```
├── _posts/          # Blog posts
├── _layouts/        # Page templates
├── _includes/       # Reusable partials
├── _sass/           # SCSS styles
├── assets/          # Static files
├── docs/            # Project documentation
└── _config.yml      # Jekyll config
```

## Adding Content

### New Blog Post

Create `_posts/YYYY-MM-DD-title-slug.md`:

```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
categories: [swift, ios]
---

Your content here...
```

### New Page

Create `page-name.md` in root:

```yaml
---
layout: page
title: "Page Title"
permalink: /url-path/
---

Your content here...
```

## Documentation

See `docs/` for detailed documentation:

- [Project Overview](docs/project-overview-pdr.md)
- [Codebase Summary](docs/codebase-summary.md)
- [Code Standards](docs/code-standards.md)
- [System Architecture](docs/system-architecture.md)

## Tech Stack

- **Generator**: Jekyll 4.3
- **Styling**: SCSS (dark theme)
- **Fonts**: Inter, JetBrains Mono
- **Hosting**: Cloudflare Pages
- **Plugins**: jekyll-feed, jekyll-seo-tag
