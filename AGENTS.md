# Repository Guidelines

## Project Structure & Module Organization
This repository is a single-page static site. Keep primary markup, inline CSS, and JavaScript in `index.html`. Store images in `assets/` using descriptive kebab-case names such as `service-deep-tissue.png`. Keep crawler-facing files at the root: `robots.txt` and `sitemap.xml`. When updating business info, keep phone numbers, URLs, opening hours, and image paths consistent across HTML metadata, JSON-LD, and sitemap entries.

## Build, Test, and Development Commands
There is no build pipeline for this project; files are served as-is.

- `python3 -m http.server 8000`
  Run a local preview from the repository root.
- `git diff`
  Review content, SEO, and layout changes before committing.
- `rg -n 'jdx-pro.com|902-189-391|kine_life_tw' index.html sitemap.xml robots.txt`
  Recheck critical domain, phone, and profile references after content updates.

## Coding Style & Naming Conventions
Use 2-space indentation in HTML, CSS, and inline JavaScript to match the existing file. Prefer semantic HTML sections and clear `id` values such as `#about`, `#services`, and `#contact` for anchor navigation. Keep CSS custom properties centralized in `:root` and reuse existing class patterns before adding new ones. Name asset files in lowercase kebab-case and keep external links secure with `target="_blank"` plus `rel="noopener noreferrer"`.

## Testing Guidelines
This repository currently has no automated test suite. Validate changes manually in desktop and mobile widths using a local server. Check anchor navigation, contact links, image loading, form behavior, and browser console output. After SEO edits, verify `title`, meta description, Open Graph data, JSON-LD, `robots.txt`, and `sitemap.xml` remain aligned.

## Commit & Pull Request Guidelines
Current git history uses very short lowercase subjects such as `init`. Keep commit subjects short and imperative, but make them more descriptive for new work, for example `update booking section copy` or `refresh service images`. PRs should include a brief summary, before/after screenshots for visual changes, and notes for any metadata or contact-information updates.
