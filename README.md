# 26B Class Hub

> Discord-themed course hub for **Equinim College Intake 26B** — front-end web development (12 weeks, 24 classes).

A single home for everything students need: weekly schedule with status, every lesson deck, all course downloads, curated learning resources, and worked code examples.

🔗 **Live site:** _will appear after first Vercel deploy_

---

## What's in here

```
.
├── index.html              # Main hub — weekly schedule with class tiles
├── resources.html          # Curated games, templates, repos, tools, docs
├── downloads.html          # Every PDF / zip / asset in one place
├── vercel.json             # Deploy config (clean URLs + cache headers)
├── README.md
│
├── assets/                 # Brand assets used by every page
│   ├── favicon.svg
│   ├── logo.svg
│   ├── og-image.svg
│   └── theme.css           # Shared stylesheet (Discord palette, nav, cards)
│
├── lessons/                # Every lesson deck + plan, named by date
│   ├── index.html          # Lesson archive listing page
│   ├── 2026-05-25-lesson-plan.html
│   ├── 2026-05-20-class.html
│   └── …
│
├── downloads/
│   ├── pdfs/               # All course PDFs (briefs, wireframes, cheat sheets)
│   ├── code/               # Starter zips (Bin Chicken Bistro, Yearbook, etc.)
│   ├── data/               # JSON data files (yearbook payload)
│   └── images/             # Reference images used in lessons
│
├── examples/               # Working example sites — view source to learn
│   ├── website-build/      # Skywings travel site (Subject 1 demo)
│   ├── yearbook-wall/      # 26B yearbook wall (v1, v2, v3, final)
│   └── trivia/             # In-class trivia game (HTML + XLSX questions)
│
└── _archive/               # Older variants preserved for reference
```

---

## Design system

| Token             | Hex        | Used for                              |
| ----------------- | ---------- | ------------------------------------- |
| `--dc-bg`         | `#1e1f22`  | Page background                       |
| `--dc-bg2`        | `#2b2d31`  | Card / nav background                 |
| `--dc-bg3`        | `#313338`  | Hover / elevated surfaces             |
| `--dc-blurple`    | `#5865f2`  | Primary accent (links, brand)         |
| `--dc-green`      | `#57f287`  | "Done" status                         |
| `--dc-current`    | `#f0b232`  | "Now / This week" status              |
| `--dc-fuchsia`    | `#eb459e`  | Hub / activity badges                 |
| `--dc-orange`     | `#fcb045`  | Highlights, demos                     |

Shared styles live in [`assets/theme.css`](assets/theme.css) — the main hub keeps its own inline styles for now to avoid breaking the working week-card layout.

---

## Local development

This is a static site — no build step.

```bash
# any static server works. The committed launch config uses:
npx serve -l 3456

# then open
open http://localhost:3456
```

The repo includes a `.claude/launch.json` for Claude Code's preview tool.

---

## Deploy

```bash
# first time — links the project
npx vercel

# subsequent prod deploys
npx vercel --prod
```

The `vercel.json` enables:
- **Clean URLs** — `/resources` instead of `/resources.html`
- **Long-cache** on `/assets/*` (1 year, immutable)
- **Short-cache** on `/downloads/*` (1 day)

---

## Maintenance notes

**Marking a week complete (after the last class of the week):**

In `index.html`:
1. Change the week-card class from `current open` to `completed`
2. Change the status pill from `now` to `done`
3. Find the next week, change `upcoming` → `current open`, status pill `soon` → `now`
4. Update the progress text (e.g. `Week 9 of 12` → `Week 10 of 12`) and the progress-bar `style="width: …%"`

**Adding a new lesson:**

1. Drop the file in `lessons/` with the naming convention `YYYY-MM-DD-{slug}.html`
2. Add a card to `lessons/index.html` so it shows in the archive
3. Add a `<span class="badge file">` to the relevant class tile in `index.html`, wrapping the filename in an `<a href="lessons/…">`

**Adding a download:**

1. Drop into the appropriate `downloads/{pdfs|code|data|images}/` subfolder
2. Use kebab-case lowercase names (`my-file.pdf`, not `My File.PDF`)
3. Add an `<a class="dl-row">` to the matching section in `downloads.html`

---

## Trainer

**Tim Daly** — Equinim College, Perth WA
[`thetimdaly@gmail.com`](mailto:thetimdaly@gmail.com) · [`tim@equinimcollege.com`](mailto:tim@equinimcollege.com) · `0414 265 050`

The Daly Creative

---

## Notes for students

This site is open source. If you spot a typo, a broken link, or have a resource you think should be added — open an issue or send Tim a message.

You're also welcome to fork the structure for your own course site. Discord theme + flat HTML/CSS = easy to maintain.
