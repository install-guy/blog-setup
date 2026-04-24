# Publishing Workflow

## Drafting
- Create Gazette articles in `content/`
- Create collection SEO blocks in `collections/`
- Create homepage modules in `components/homepage/`
- Follow `content/blog-post-template.md` for article work
- Add Gazette frontmatter fields: `title`, `image`, `image_alt`, `excerpt`

## Review
- Check structure and formatting
- Confirm article links use `/gearheads-gazette/[slug]`
- Confirm collection links use `/collections/[slug]`
- Confirm fitment links use `/vehicles`
- Confirm Gazette image path matches the article slug in `assets/gazette/posts/`
- Confirm excerpt is usable for homepage/module previews
- Keep CTAs useful and avoid over-linking

## Publish-Ready Check
- Make sure the tone matches existing Hobby Etc content
- Remove placeholders or instructional language
- Verify layout behavior if the file is a homepage/component module
- If wiring the Gazette homepage module, use `components/homepage/gearheads-gazette-section.html`
- Reference `data/gazette-posts-example.json` for the expected post data shape
- Default missing CTA labels to `Read the Guide` in the renderer

The workflow should stay simple, repeatable, and fast.
