# Project Documentation Rules (Non-Obvious Only)

- Blog posts automatically inherit `tags: ["posts"]` from `content/blog/blog.11tydata.js`
- Front matter validation happens via Zod schemas - required fields: `title`, `date`, `description`
- Custom filters are in `_config/filters.js` - includes date formatting with Luxon
- Template hierarchy: `base.njk` → `post.njk`/`home.njk` (extends)
- Content directories have different behaviors: `content/blog/` vs root `content/`
- Eleventy data files in `_data/` provide global variables and validation
- Bundle system uses different syntax than standard Eleventy (shortcodes `{% css %}`)
