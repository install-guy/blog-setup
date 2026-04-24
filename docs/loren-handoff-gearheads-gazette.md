# Loren Handoff: Gearhead's Gazette

## System Overview
- Gazette articles live in `content/` as Markdown
- Each article should include frontmatter:
  `title`, `image`, `image_alt`, `excerpt`
- Images live in `assets/gazette/posts/`
- Image filenames should match the article slug
- Gazette URLs use:
  `/gearheads-gazette/[slug]`

## Repo Structure
- `content/` = Gazette article markdown
- `assets/gazette/posts/` = Gazette post images
- `components/homepage/` = homepage modules
- `components/gazette/` = Gazette article template
- `collections/` = collection/category SEO blocks
- `data/` = reference/example data structures

## Rendering System
There are two Gazette render targets:

### A. Homepage Module
- File:
  `components/homepage/gearheads-gazette-section.html`
- Purpose:
  Displays 2 latest or featured posts
- Expected fields:
  `title`, `image`, `excerpt`, `url`

### B. Article Page Template
- File:
  `components/gazette/gazette-article-template.html`
- Purpose:
  Renders the full article page
- Uses:
  `article.title`
  `article.image`
  `article.image_alt`
  `article.content`

## Data Flow
Markdown in `content/`
-> frontmatter extracted
-> converted to post objects
-> optionally output as JSON
-> rendered into the homepage module and article template

Example data file:
- `data/gazette-posts-example.json`

## What Loren Needs To Do
1. Parse markdown frontmatter from `content/*.md`
2. Generate slugs from filenames
3. Build post URLs using `/gearheads-gazette/[slug]`
4. Render the first 2 latest or featured posts into the homepage module
5. Default CTA text to `Read the Guide` if missing
6. Render individual article pages
7. Inject collection SEO blocks where appropriate

## Developer Notes
- `article.content` must be rendered as HTML from markdown
- Do not escape HTML content
- Do not hardcode article content inside components
- Use frontmatter as the source of truth
