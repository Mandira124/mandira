# Mandira Sharma — Portfolio

A single-page editorial portfolio built with Hugo, plain HTML/CSS/JS
(no framework, no theme).

## Run it locally

1. Install Hugo (extended version): https://gohugo.io/installation/
2. From this folder: `hugo server -D`
3. Open http://localhost:1313

## Build for deployment

`hugo --minify` — outputs the static site to `public/`, which you can
deploy anywhere (Netlify, Vercel, GitHub Pages, any static host).

## What to edit, and where

| What you want to change            | Where                              |
|-------------------------------------|-------------------------------------|
| Hero name / tagline                 | `content/_index.md` → `hero:`       |
| About text                          | `content/_index.md` → `about:`      |
| Contact links                       | `content/_index.md` → `contact:`    |
| Hero portrait image                 | replace `static/images/mandira-handdrawn.png` (keep the filename, or update the path in `content/_index.md`) |
| Life / scrapbook photos + captions  | `data/life.yaml` — add/remove entries, drop matching photos into `static/images/life/` |
| Projects (name, description, GitHub link) | `data/projects.yaml` — replace every `REPLACE_WITH_...` URL with the real repo link |
| Colors, type, spacing               | `static/css/main.css` (tokens are at the top, under `:root`) |
| Section templates                   | `layouts/partials/*.html` (one file per section: hero,about, life, projects, contact, nav) |

## Notes

- The hero portrait placeholder is a plain box — replace it with your
  actual hand-drawn image at the same path (or point to a new path in
  `content/_index.md`). It should be a fairly tall image (roughly
  4:5, like the 640×800 placeholder) for the layering to look right.
- Life photos are placeholders too — drop your real JPGs into
  `static/images/life/`, matching the filenames used in
  `data/life.yaml` (or update the paths).
- No JavaScript framework, no build step beyond Hugo itself, no
  external dependencies besides Google Fonts (Fraunces, IBM Plex Sans,
  Caveat).
