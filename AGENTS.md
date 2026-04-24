# AGENTS

## Repo Purpose
This repo is the working content engine for Hobby Etc:
- Gearhead's Gazette article markdown in `content/`
- Collection SEO blocks in `collections/`
- Homepage modules in `components/homepage/`
- Gazette article templates in `components/gazette/`
- Gazette data examples in `data/`

## Core Rules
- Gazette article URLs must use `/gearheads-gazette/[slug]`
- Collection links must use `/collections/[slug]`
- Fitment references must use `/vehicles`
- Do not over-link articles or collection content
- Keep the tone practical, garage-style, and useful

## Blog Post Standard
- Use `content/blog-post-template.md` as the source of truth
- Always include frontmatter in new articles:
  `title`, `image`, `image_alt`, `excerpt`
- Follow Gazette image naming conventions in `assets/gazette/posts/`
- Use `/gearheads-gazette/[slug]` for internal article links
- Limit links to 5 or fewer per article
- Include the `Keep Your Rig Dialed` section in articles
- Avoid placeholders and instructional artifacts in finished content

## Gazette Rendering Notes
- Homepage module path:
  `components/homepage/gearheads-gazette-section.html`
- Article template path:
  `components/gazette/gazette-article-template.html`
- Homepage module should render 2 latest or featured posts
- The module is designed to consume frontmatter-derived post data or a generated data file
- Example data shape lives in `data/gazette-posts-example.json`
- If `post.cta_text` is missing, renderer fallback should be `Read the Guide`
- `article.content` must render as HTML converted from markdown and should not be escaped

## Working Guidance
- Prefer direct file edits over abstract planning when the ask is clear
- Keep docs concise and practical
- Preserve mockup/reference files when asked, and separate them from production-ready components
