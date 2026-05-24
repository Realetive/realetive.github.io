# AGENTS.md

This file provides guidance to agents when working with code in this repository.

## Project Overview
This is an Eleventy static site generator blog project with ES modules and modern JavaScript tooling.

## Essential Commands
- `npm start` - Run development server with live reload
- `npm run build` - Build static site to `_site/` directory
- `npm run debug` - Run build with Eleventy debug output
- `npm run debugstart` - Run development server with debug output

## Code Style Requirements
- Use tabs for indentation (2 spaces width) - enforced by .editorconfig
- Use ES6 module syntax (import/export) - project uses `"type": "module"`
- Trim trailing whitespace and insert final newlines - enforced by .editorconfig
- Use LF line endings - enforced by .editorconfig

## Critical Project Structure
- `content/` - Source content files (Markdown, Nunjucks)
- `_includes/layouts/` - Template layouts (base.njk, post.njk, home.njk)
- `_data/` - Global data files and schema validation
- `_config/filters.js` - Custom Eleventy filters (date formatting, array operations)
- `public/` - Static assets copied to output
- `css/` - Stylesheets bundled by Eleventy
- `_site/` - Generated static site (output directory)

## Front Matter Requirements
- Blog posts must have `title`, `date`, and `description` in front matter
- Optional `draft: true` flag excludes posts from production builds
- Posts in `content/blog/` automatically get `tags: ["posts"]` and use `layouts/post.njk`
- Content validation uses Zod schemas in `_data/eleventyDataSchema.js`

## Bundle System
- CSS bundled via `{% css %}{% endcss %}` shortcodes
- JavaScript bundled via `{% js %}{% endjs %}` shortcodes
- Bundles output to `dist/` directory
- Use `eleventy:ignore` attribute to opt-out specific elements

## Deployment Configuration
- Netlify: builds to `_site/`, uses `npm run build`
- Vercel: requires trailing slashes (`{ "trailingSlash": true }`)
- RSS feed available at `/feed/feed.xml`

## Unique Patterns
- Date formatting uses Luxon library, not native Date
- Custom `filterTagList` filter removes "all" and "posts" tags
- Draft posts handled by preprocessor in `eleventy.config.js`
- Image pipeline watches for `{svg,webp,png,jpg,jpeg,gif}` files
- CSS files watched for live reload during development
