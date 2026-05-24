# Project Coding Rules (Non-Obvious Only)

- Always use tabs for indentation (2 spaces width) - enforced by .editorconfig, not standard spaces
- ES6 module syntax required throughout - project uses `"type": "module"` in package.json
- Use Luxon DateTime for date operations instead of native Date (see _config/filters.js)
- Bundle CSS with `{% css %}{% endcss %}` shortcodes, not individual style tags
- Bundle JavaScript with `{% js %}{% endjs %}` shortcodes
- Content validation uses Zod schemas in `_data/eleventyDataSchema.js` - front matter must conform
- Draft posts use `draft: true` flag but are processed by preprocessor in `eleventy.config.js`
- Custom filters from `_config/filters.js` override standard methods (filterTagList removes "all" and "posts")
- Nunjucks templates in `_includes/layouts/` follow specific hierarchy (base.njk → post.njk/home.njk)
