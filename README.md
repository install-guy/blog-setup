# Blog Setup

Content repo for Hobby Etc's Gearhead's Gazette articles, collection-page SEO blocks, and homepage content modules.

## What Lives Here
- `content/` = Gearhead's Gazette article markdown
- `collections/` = SEO content blocks for collection/category pages
- `components/homepage/` = homepage modules, including Gearhead's Gazette
- `docs/` = strategy, workflow, and system rules
- `templates/` = reusable future templates if the repo grows into that structure

## Current Repo Shape
Current top-level folders in the repo are:
- `content/`
- `collections/`
- `components/`
- `docs/`

If `data/`, `scripts/`, `src/`, or `output/` are added later, keep their existing documented purpose rather than redefining them casually.

## URL Conventions
- Gazette articles: `/gearheads-gazette/[slug]`
- Collection/category pages: `/collections/[slug]`
- Fitment tool: `/vehicles`

## Content Rules
- Blog posts should follow `content/blog-post-template.md`
- Articles should use natural internal links, not forced link stuffing
- CTAs should use the `Keep Your Rig Dialed` pattern
- Keep links helpful and avoid over-linking

## Quick Workflow
- Add or update Gazette articles in `content/`
- Add or update collection SEO blocks in `collections/`
- Add or update homepage modules in `components/homepage/`
- Check article links, collection links, and `/vehicles` fitment references before wrapping up

## Who This Is For
This repo should be easy for Dan, Loren, and future Codex sessions to pick up quickly without reverse-engineering the content system first.
