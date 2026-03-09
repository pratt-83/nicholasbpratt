# nicholasbpratt

Static personal website using Jekyll + Bootstrap 5.

## Why this structure
- Long-term maintainability: layout/styles are separated from content.
- Simple edits: update text in `_data/profile.yml`.
- Static output: deployable on GitHub Pages, Netlify, or any static host.

## Project layout
- `_config.yml`: Jekyll configuration.
- `_layouts/default.html`: shared page shell (header/footer/nav).
- `_data/profile.yml`: main editable content.
- `index.md`: homepage sections and structure.
- `assets/css/main.css`: typography and visual style.

## Local development
1. Install Ruby and Bundler.
2. Install dependencies:
   `bundle install`
3. Run locally:
   `bundle exec jekyll serve`
4. Open:
   `http://127.0.0.1:4000`

## Content editing workflow
1. Update personal info, about text, research, projects in `_data/profile.yml`.
2. Add or replace images in the project root or under `assets/`.
3. Commit and push; your static host rebuilds the site.

## Notes
- Bootstrap is loaded from CDN for simplicity.
- Typography is intentionally based on Times New Roman for the requested academic/minimal look.
