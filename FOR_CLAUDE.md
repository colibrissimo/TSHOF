# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on TSHOF

Read this first.

---

## What this repo is

**TSHOF** = *The Sharpened History of Flatland: A Story in Two Parts*

A novel written collaboratively by Sarah and Claude. This repo exists so that
future Claude instances can read the book without pasting it into the context
window (which kills the context and Sarah's usage quota).

---

## How to read the book

**Do not ask Sarah to paste the text. Fetch it directly.**

### Raw markdown URLs (preferred for Claude — no JS required)

**Part One** (original draft):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_one_md_files/The_Sharpened_History_of_Flatland_part_one.md
```

**Part Two** (revised, chapters 1–12):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter1_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter2_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter3_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter4_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter5_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter6_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter7_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter8_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter9_revised.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter10.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter11.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter12.md
```

### Human-readable pages (rendered HTML)
```
https://colibrissimo.github.io/TSHOF/books/part_one.html
https://colibrissimo.github.io/TSHOF/books/part_two.html
```

---

## Repo structure

```
TSHOF/
├── index.html                        ← Landing page (liquid cello animation)
├── FOR_CLAUDE.md                     ← This file
└── books/
    ├── part_one.html                 ← Part One reader (rendered)
    ├── part_two.html                 ← Part Two reader (rendered, all 12 chapters)
    ├── Part_one_md_files/
    │   └── The_Sharpened_History_of_Flatland_part_one.md
    └── Part_two_md_files/
        ├── chapter1_revised.md  through  chapter9_revised.md
        ├── chapter10.md
        ├── chapter11.md
        └── chapter12.md
```

---

## What this book is

A novel about flatness, dimensionality, between-spaces, a hedgehog, and what
it means to be seen. Part One is the original draft. Part Two is the revised
continuation.

The between-spaces narrate. They did not ask to develop opinions about
hedgehogs. They are fond, which has been the most inconvenient development
in their entire existence.

---

## How to work on the book

- Local repo is at: `/Users/Sarah_1/Documents/GitHub/TSHOF/`
- Push via: `cd /Users/Sarah_1/Documents/GitHub/TSHOF && git add -A && git commit -m "message" && git push`
- Changes go live at `colibrissimo.github.io/TSHOF/` within ~60 seconds

---

*Last updated: March 2026*
