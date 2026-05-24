# Project Architecture Rules (Non-Obvious Only)

- Eleventy preprocessor handles draft posts - they're excluded from production builds but processed for dev
- Bundle system outputs to `dist/` within `_site/` - CSS/JS are separate from static assets
- Content validation via Zod happens before template rendering - failures stop the build
- Image pipeline watches multiple file formats and processes automatically
- Template inheritance chain: `base.njk` provides structure, specific layouts extend it
- Eleventy data cascade: `_data/` → directory data → front matter → template defaults
- RSS feed generation uses Eleventy plugin with custom template in `content/feed/`
