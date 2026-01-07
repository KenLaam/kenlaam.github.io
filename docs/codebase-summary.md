# Codebase Summary

## Directory Structure

```
kenlaam-blog/
├── _config.yml          # Jekyll configuration
├── _includes/           # Reusable HTML partials
│   ├── header.html      # Site header with navigation
│   └── footer.html      # Site footer
├── _layouts/            # Page templates
│   ├── default.html     # Base layout (head, body wrapper)
│   ├── home.html        # Homepage with hero + posts list
│   ├── page.html        # Standard page layout
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts (markdown)
│   └── 2025-12-21-welcome-to-my-blog.md
├── _sass/               # SCSS stylesheets
│   ├── _variables.scss  # Color, typography, spacing tokens
│   ├── _base.scss       # Reset and base styles
│   ├── _layout.scss     # Layout components
│   ├── _components.scss # UI components (buttons, cards)
│   └── _syntax.scss     # Code syntax highlighting
├── assets/
│   ├── css/main.scss    # SCSS entry point
│   └── apps/            # App screenshots/icons
├── index.md             # Homepage content
├── blog.md              # Blog listing page
├── apps.md              # Apps portfolio page
├── about.md             # About page
├── privacy.md           # Privacy policy
├── terms.md             # Terms of service
├── support.md           # App support page
├── Gemfile              # Ruby dependencies
└── README.md            # Project readme
```

## File Statistics

| Category | Files | Purpose |
|----------|-------|---------|
| Layouts | 4 | HTML templates |
| Includes | 2 | Reusable partials |
| SCSS | 5 | Styling |
| Content | 7 | Markdown pages |
| Posts | 1 | Blog articles |
| Config | 2 | Jekyll + Gemfile |

## Key Files

### _config.yml
Site configuration: title, URL, plugins, navigation, collections.

### _sass/_variables.scss
Design tokens: dark theme colors, fonts, breakpoints, spacing.

### _layouts/default.html
Base template: HTML head, Google Fonts, header/footer includes.

### _layouts/home.html
Homepage: hero section + latest posts list (limit 5).
