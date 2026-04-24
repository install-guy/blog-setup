# AGENTS

## Repo Purpose
This repo is the working content engine for Hobby Etc:
- Gearhead's Gazette article markdown in `content/`
- Collection SEO blocks in `collections/`
- Homepage modules in `components/homepage/`
- Gazette data examples in `data/`

## Core Rules
- Gazette article URLs must use `/gearheads-gazette/[slug]`
- Collection links must use `/collections/[slug]`
- Fitment references must use `/vehicles`
- Do not over-link articles or collection content
- Keep the tone practical, garage-style, and useful

## Blog Post Standard
- Use `content/blog-post-template.md` as the source of truth
- Gazette posts should include frontmatter for `title`, `image`, `image_alt`, and `excerpt`
- Include natural internal links only where they help
- Use the `Keep Your Rig Dialed` CTA format
- Avoid placeholders and instructional artifacts in finished content
- Follow `docs/gazette-image-standards.md` for Gazette post image sizing and naming

## Gazette Module Notes
- Homepage module path: `components/homepage/gearheads-gazette-section.html`
- Gazette post URLs must resolve to `/gearheads-gazette/[slug]`
- The module is designed to consume frontmatter-derived post data or a generated data file
- Example data shape lives in `data/gazette-posts-example.json`
- If `post.cta_text` is missing, renderer fallback should be `Read the Guide`

## Working Guidance
- Prefer direct file edits over abstract planning when the ask is clear
- Keep docs concise and practical
- Preserve mockup/reference files when asked, and separate them from production-ready components
