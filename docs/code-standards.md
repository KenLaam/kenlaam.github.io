# Code Standards

## File Naming

- **Posts**: `YYYY-MM-DD-title-slug.md` in `_posts/`
- **Pages**: `page-name.md` in root
- **SCSS**: `_partial-name.scss` in `_sass/`
- **Layouts**: `layout-name.html` in `_layouts/`

## Front Matter

### Required for Pages
```yaml
---
layout: page|home|post
title: "Page Title"
permalink: /url-path/
---
```

### Required for Posts
```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD
categories: [category1, category2]
---
```

## SCSS Organization

1. **_variables.scss**: Design tokens only
2. **_base.scss**: Reset, body, typography defaults
3. **_layout.scss**: Header, footer, page structure
4. **_components.scss**: Buttons, cards, UI elements
5. **_syntax.scss**: Code block styling

## Design Tokens

### Colors (Dark Theme)
- Background: `$bg-primary` (#0D1117)
- Text: `$text-primary` (#F0F6FC)
- Accent: `$accent` (#58A6FF)

### Typography
- Sans: Inter
- Mono: JetBrains Mono

### Breakpoints
- Small: 640px
- Medium: 768px
- Large: 1024px

## Liquid Templates

- Use `relative_url` filter for all internal links
- Escape user content with `| escape`
- Limit loops where possible (e.g., `limit:5`)

## Jekyll Plugins

| Plugin | Purpose |
|--------|---------|
| jekyll-feed | RSS feed generation |
| jekyll-seo-tag | Meta tags for SEO |
