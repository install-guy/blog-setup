# Loren Handoff: Gearhead's Gazette

## What Is Ready
- `content/` holds Gearhead's Gazette article markdown
- `collections/` holds SEO content blocks for collection/category pages
- `components/homepage/gearheads-gazette-section.html` is the homepage module placeholder wired for Gazette post data
- `data/gazette-posts-example.json` shows the expected data shape for homepage rendering
- Gazette image standards are documented and frontmatter has been added across active article files

## Repo Structure
- `content/` = Gazette article markdown
- `assets/gazette/posts/` = Gazette post images
- `components/homepage/` = homepage modules
- `collections/` = collection/category SEO blocks
- `data/` = reference/example data structures

## URL Convention
- Gazette articles should resolve to:
  `/gearheads-gazette/[slug]`

## Required Article Frontmatter
Each Gazette article should include:
- `title`
- `image`
- `image_alt`
- `excerpt`

## Image Convention
- Path:
  `/assets/gazette/posts/[slug].jpg`
- Standard size:
  `1200 x 675`
- Ratio:
  `16:9`

## Homepage Module
- Path:
  `components/homepage/gearheads-gazette-section.html`
- Current state:
  Uses placeholder/pseudo-loop markup and comments to show how Gazette post data should map into the module

## Example Data
- Path:
  `data/gazette-posts-example.json`
- Purpose:
  Shows the expected post data structure for homepage rendering

## What Loren Needs To Do
1. Parse markdown frontmatter from `content/*.md`
2. Generate slugs from filenames
3. Build post URLs using `/gearheads-gazette/[slug]`
4. Render the first 2 latest or featured posts into the homepage module
5. Default CTA text to `Read the Guide` if missing
6. Render individual article pages
7. Inject collection SEO blocks where appropriate

## Practical Notes
- Use the filename slug as the source of truth unless there is a later routing override
- Keep homepage/article image usage tied to the `image` frontmatter field
- Treat `excerpt` as the preview copy for homepage cards and future featured modules
