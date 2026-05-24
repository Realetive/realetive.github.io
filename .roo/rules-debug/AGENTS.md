# Project Debug Rules (Non-Obvious Only)

- Use `npm run debugstart` to run development server with full Eleventy debug output
- Draft posts are silently excluded during production builds via preprocessor in `eleventy.config.js`
- Content validation errors from Zod schemas will cause build failures with detailed messages
- CSS/JS bundles output to `_site/dist/` directory - check here for bundled output issues
- Image pipeline failures may not show clear errors - check processed file formats
- RSS feed generation issues might not surface until deployment
- Eleventy watch targets include CSS files and images automatically via configuration
