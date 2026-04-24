# Blog Setup

Content repo for Hobby Etc's Gearhead's Gazette articles, collection-page SEO blocks, and homepage content modules.

## System Overview
- Gazette articles live in `content/` as Markdown
- Gazette article frontmatter should include:
  `title`, `image`, `image_alt`, `excerpt`
- Gazette post images live in `assets/gazette/posts/`
- Image filenames should match the article slug
- Gazette article URLs use `/gearheads-gazette/[slug]`

## What Lives Here
- `content/` = Gearhead's Gazette article markdown
- `collections/` = SEO content blocks for collection/category pages
- `components/homepage/` = homepage modules, including Gearhead's Gazette
- `components/gazette/` = Gazette article page template(s)
- `data/` = reference/example data structures for module wiring
- `docs/` = strategy, workflow, and system rules
- `templates/` = reusable future templates if the repo grows into that structure

## Rendering System
There are two main Gazette render targets:

- Homepage module:
  `components/homepage/gearheads-gazette-section.html`
  Renders 2 latest or featured posts from post data

- Article page template:
  `components/gazette/gazette-article-template.html`
  Renders a full Gazette article using:
  `article.title`, `article.image`, `article.image_alt`, `article.content`

## Data Flow
Markdown in `content/`
-> frontmatter extracted
-> converted to post objects
-> optionally output as JSON
-> rendered into the homepage module and article template

Example data shape:
- `data/gazette-posts-example.json`

## Content Rules
- Blog posts should follow `content/blog-post-template.md`
- Articles should use natural internal links, not forced link stuffing
- CTAs should use the `Keep Your Rig Dialed` pattern
- Keep links helpful and avoid over-linking
- Gazette image standards live in `docs/gazette-image-standards.md`

## Developer Notes
- `article.content` must be rendered as HTML converted from markdown
- Do not escape article HTML as plain text
- Default homepage CTA text to `Read the Guide` if `post.cta_text` is missing
- Use frontmatter as the source of truth for Gazette post metadata

## Who This Is For
This repo should be easy for Dan, Loren, and future Codex sessions to pick up quickly without reverse-engineering the content system first.
