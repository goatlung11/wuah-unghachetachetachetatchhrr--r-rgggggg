# Wuah

A minimalist, text-only blog for creative writing, hosted on GitHub Pages.

## Folder structure

```

blog/
├── index.html                          homepage (lists all stories)
├── style.css                           the only stylesheet
└── stories/
└── the-fisherman/
├── index.html                  table of contents for this story
├── 01-the-hook.html            chapter 1
├── 02-the-river.html           chapter 2
└── 03-the-catch.html           chapter 3

```

## How to add a new chapter

1. Duplicate an existing chapter file, e.g. `01-the-hook.html`.
2. Rename it with the next number, e.g. `04-the-ending.html`.
3. Open it and change:
   - `<title>` in the head
   - `<h1>` in the main
   - the chapter body paragraphs
   - the Previous and Next links in the nav
4. Open the previous chapter and change its Next link to point at the new file.
5. Open `stories/the-fisherman/index.html` and add a new `<li>` for the chapter.

## How to add a new story

1. Duplicate the whole `stories/the-fisherman/` folder and rename it, e.g. `stories/new-story/`.
2. Edit that folder's `index.html` title and chapter list.
3. Edit the chapter files inside it.
4. Open the root `index.html` and add a new `<li>` pointing to `/stories/new-story/`.

## How to add a new chapter to a chapter nav

First chapter has no Previous link.
Last chapter has no Next link.
Middle chapters have both.
Every chapter links back to its table of contents with `./`.

## Rules

- Text only. No images.
- Dark mode only. No theme switching.
- No JavaScript.
- No webfonts, no external assets.
- One stylesheet at the repo root, linked with `/style.css`.
- Story links end with a trailing slash, e.g. `/stories/the-fisherman/`.

## Deploying to GitHub Pages

The site is served from the repository root on the `master` branch.
The `CNAME` file points at the custom domain.
Push the files, and GitHub Pages rebuilds automatically within about a minute.
