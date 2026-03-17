# crypticsbyabdul.com — Jekyll Site

Live at: **https://crypticsbyabdul.com**
GitHub repo: **abdulkhaleddd.github.io**

---

## Adding a New Puzzle

1. Create a new file in `_puzzles/` named: `puzzle-NNN.md`
2. Use this template:
```
---
layout: puzzle
title: "Your Puzzle Title"
number: 2
date: 2026-04-01
grid_size: "15×15"
difficulty: 3
solution_slug: "solution-NNN"
embed: '<iframe height="700px" width="100%" allow="web-share; fullscreen" style="border:none; width: 100% !important; position: static;display: block !important; margin: 0 !important;" src="YOUR AMUSELABS URL HERE" aria-label="Puzzle Me Game"></iframe>'
tags: [Cryptic, 15×15]
---

Intro text shown above the puzzle goes here. You can include HTML links.

<!--notes-->

Setter's notes go here, shown below the puzzle under "Setter's Notes".
```

**To get the Amuselabs embed:**
- Go to amuselabs.com
- Upload your .puz file
- Copy the iframe embed code
- Paste the src URL into the embed field above

---

## Adding a Solutions Page

1. Create a new file in the **root** of the repo named: `solution-NNN.md`
2. Use this template:
```
---
layout: solution
title: "Your Puzzle Title"
number: 1
date: 2026-04-01
puzzle_slug: "puzzle-NNN"
permalink: /solutions/solution-NNN/
---

<div class="solutions-section">
  <h2 class="solutions-direction">Across</h2>

  <div class="solution-entry">
    <span class="solution-number">1</span>
    <div class="solution-content">
      <span class="solution-answer">ANSWER</span>
      <span class="solution-clue"><u>Definition</u> rest of clue (7)</span>
      <span class="solution-breakdown">WORD + PLAY</span>
    </div>
  </div>

</div>

<div class="solutions-section">
  <h2 class="solutions-direction">Down</h2>

  <div class="solution-entry">
    <span class="solution-number">1</span>
    <div class="solution-content">
      <span class="solution-answer">ANSWER</span>
      <span class="solution-clue"><u>Definition</u> rest of clue (7)</span>
      <span class="solution-breakdown">WORD + PLAY</span>
    </div>
  </div>

</div>
```

**Notes:**
- Underline the definition with `<u>definition</u>`
- Use `&lt;` for `<` and `&amp;` for `&` in breakdowns
- Solutions file goes in the **root**, not `_solutions/`

---

## Adding a Notes Post

1. Create a file in `_posts/` named: `YYYY-MM-DD-your-title.md`
2. Use this template:
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

## Editing Existing Content

| What | Where |
|------|-------|
| Site tagline | `_config.yml` → `tagline:` |
| Bio in sidebar | `_includes/sidebar.html` |
| About page | `about.html` |
| Footer text | `_includes/footer.html` |
| All styling | `assets/css/main.css` |
| Theme colours | `_includes/header.html` → JS themes object |

---

## Themes

Four themes, each with light and dark mode. Toggle with the moon/sun button. Switch palettes with the coloured dots — top right of every page.

| Swatch | Name |
|--------|------|
| Cream | Parchment |
| Blue-grey | Slate |
| Green | Forest |
| Near-black | Noir |
| Pink | Pink |

---

## Difficulty Scale

| Pips | Level |
|------|-------|
| 1 | Gentle |
| 2 | Easy-medium |
| 3 | Mid |
| 4 | Hard |
| 5 | Fiendish |

---

## File Structure
```
crypticsbyabdul/
├── _config.yml            ← site settings
├── _layouts/
│   ├── default.html       ← base layout
│   ├── puzzle.html        ← puzzle pages
│   ├── solution.html      ← solution pages
│   └── post.html          ← notes posts
├── _includes/
│   ├── header.html        ← header + theme switcher JS
│   ├── sidebar.html       ← sidebar
│   └── footer.html        ← footer
├── _puzzles/              ← ADD NEW PUZZLES HERE (puzzle-NNN.md)
├── _posts/                ← ADD NOTES POSTS HERE
├── assets/css/main.css    ← all styling
├── index.html             ← homepage (auto-updates)
├── archive.html           ← archive (auto-updates)
├── about.html             ← bio page
├── notes.html             ← notes listing (auto-updates)
└── solution-NNN.md        ← SOLUTION FILES GO IN ROOT
```

---

## Maintenance Tips

- After any update, hard refresh with **Ctrl+Shift+R** if you don't see changes
- Check the **Actions** tab in GitHub after commits to confirm the build succeeded
- Sort order on homepage and archive is by `number:` field, not filename
- The solutions file must live in the **root** of the repo with a `permalink:` in the front matter
