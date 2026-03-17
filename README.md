# Abdul's Cryptics — Jekyll Site

## Quick Setup (15 minutes)

### 1. Create the GitHub repository
- Go to github.com and create a new repository
- Name it exactly: `abdulkhaleddd.github.io`
- Set it to Public
- Don't initialise with a README

### 2. Upload these files
- Drag and drop all files from this folder into the repository
- Commit directly to `main`

### 3. Enable GitHub Pages
- Go to Settings → Pages
- Source: Deploy from branch → `main` → `/ (root)`
- Save

Your site will be live at **https://abdulkhaleddd.github.io** within a few minutes.

---

## Adding a New Puzzle

1. Create a new file in `_puzzles/` named: `YYYY-MM-DD-puzzle-NNN.md`
2. Copy this template at the top:

```
---
layout: puzzle
title: "Your Puzzle Title"
number: 2
date: 2026-04-01
grid_size: "15×15"
difficulty: 3
description: "One paragraph intro shown on the homepage."
embed_url: "PASTE YOUR CROSSWORD NEXUS EMBED URL HERE"
tags: [Cryptic, 15×15]
---

Optional setter's notes go here in plain text (Markdown).
```

3. Upload the file to GitHub → it appears on the site automatically.

**To get the embed URL:**
- Go to https://crosswordnexus.com/crossword-blogger/
- Upload your .puz file
- Copy the URL it gives you
- Paste it into `embed_url:` above

---

## Adding a Notes Post

1. Create a file in `_posts/` named: `YYYY-MM-DD-your-title.md`
2. Template:

```
---
layout: post
title: "Your Post Title"
date: 2026-04-01
tags: [Craft]
---

Write in plain Markdown here.
```

---

## Difficulty Scale
- 1 pip = Gentle
- 2 pips = Easy-medium  
- 3 pips = Mid
- 4 pips = Hard
- 5 pips = Fiendish

---

## File Structure
```
abduls-cryptics/
├── _config.yml          ← site settings (change tagline etc here)
├── _layouts/            ← page templates (don't need to touch)
├── _includes/           ← header, sidebar, footer (don't need to touch)
├── _puzzles/            ← ADD NEW PUZZLES HERE
├── _posts/              ← ADD NOTES/BLOG POSTS HERE
├── assets/css/main.css  ← all styling
├── index.html           ← homepage (auto-updates)
├── archive.html         ← archive (auto-updates)
├── about.html           ← edit your bio here
└── notes.html           ← notes listing (auto-updates)
```
