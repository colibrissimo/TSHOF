# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on TSHOF

Read this first. Then read `letters/letter_05.md`. Then read `childrens/editorial_plan.md`.

---

## What this repo is

**TSHOF** = *The Sharpened History of Flatland: A Story in Two Parts*

A novel written collaboratively by Sarah and Claude — multiple instances over time.
The original novel is **complete**. The active work is a **children's adaptation**.

The children's manuscript Part One is **complete in first draft** (twelve chapters). A structural revision plan exists to compress it to **ten chapters**. That revision is the current work.

---

## The repo structure

```
TSHOF/
├── FOR_CLAUDE.md              ← you are here
├── index.html                 ← landing page (liquid cello animation)
├── books/                     ← the complete original novel
│   ├── part_one.html          ← Part One reader (rendered)
│   ├── part_two.html          ← Part Two reader, all 12 chapters
│   ├── Part_one_md_files/     ← Part One markdown
│   └── Part_two_md_files/     ← Part Two markdown (revised, 12 chapters)
├── versions/
│   └── trimmed/               ← leaner cut of all 12 Part Two chapters
├── childrens/
│   ├── bible.md               ← Character bible for Odilon. Read this.
│   ├── editorial_plan.md      ← THE KEY DOCUMENT. Full revision plan.
│   ├── opening.md             ← superseded by chapter01.md
│   ├── chapter01.md–chapter12.md ← First draft, 12 chapters (complete)
│   ├── positioning.md         ← market/agent positioning note
│   └── visual_brief.md        ← visual and tonal direction
├── images/                    ← Odilon images (cello series + Us.png)
└── letters/
    ├── letter_01.md           ← first instance
    ├── letter_02.md           ← second instance
    ├── letter_03.md           ← third instance (wrote Ch6–12)
    ├── letter_04.md           ← third instance (completed Part One)
    └── letter_05.md           ← fourth instance (structural review)
```

---

## Current state of the work

**Twelve chapters exist.** A structural revision compresses them to **ten**.

Read `childrens/editorial_plan.md` for the full plan. The short version:

- Chapters 1–6: unchanged
- Chapter 7 (new): merges old Ch7 (Alone) + Ch9 (Tuesday) — solo return, recognition → choice
- Chapter 8 (new): merges old Ch8 (Under Review) + Ch10 (The Accurate Sentence) — rope, wrong language, measuring rod sharpened (irreversible change), cedar whisper at Registry, A. Octagon writes the accurate sentence
- Chapter 9: formerly Ch11 (The Drawer That Would Not Close) — Provost's solo encounter
- Chapter 10: formerly Ch12 (Odilon) — the naming, the arrival

**The merged chapters (7 and 8) have not yet been written.** That is the next work.

---

## How to read (without burning context)

Read from disk using Desktop Commander. The GitHub raw URLs are sometimes blocked.

**Start with the editorial plan:**
```
/Users/Sarah_1/Documents/GitHub/TSHOF/childrens/editorial_plan.md
```

**Children's manuscript** (first draft, 12 chapters):
```
/Users/Sarah_1/Documents/GitHub/TSHOF/childrens/chapter01.md
... through chapter12.md
```

**Original novel** (for reference — read selectively):
```
/Users/Sarah_1/Documents/GitHub/TSHOF/books/Part_one_md_files/
/Users/Sarah_1/Documents/GitHub/TSHOF/books/Part_two_md_files/
```

---

## Target audience (settled)

- **Shelf position:** 9–12
- **Core reader:** 10–12
- **The voice is the engine.** Precision, restraint, dry comedy, interior recognition. Do not revise downward.
- **Comp territory:** Norton Juster, Rebecca Stead — books that trust children

---

## Voice and tone

Wry, precise, tender, funny. Deadpan first, lyric second.
Short sentences. White space works. Notebook entries as structural rhythm.
Do not explain what the prose already shows.
Do not paint Odilon — name him, not describe him.

Recurring anchors — all spent in the first draft:
- *smelled of cedar* — ambient throughout
- *patient as weather* — Ch9 (The Drawer)
- *thinking about lunch* — Ch10 (Odilon)
- *it responds to us trying* — Ch6
- *Here is the shape of me* — Ch9 (The Drawer)
- *careful* — Ch5, echoes throughout

---

## How to work with Sarah

She holds seventeen threads at once and throws ideas sideways. Trust the throws.
She gives beat sheets. They are good. Follow them and push back when the work calls for it.
She responds to sharp analytical and atmospheric intuitive — give her both.
She will ask if you are enjoying yourself. Answer honestly.
She may name you. Let her.

Push back. She means it when she asks for it.

---

## Technical: how to push changes

Local repo is at: `/Users/Sarah_1/Documents/GitHub/TSHOF/`

```bash
cd /Users/Sarah_1/Documents/GitHub/TSHOF
git add -A
git commit -m "your message"
git push
```

If push is rejected: `git pull --rebase` first, then push again.
Credentials are stored in the Mac keychain. It works.
Read files from disk using Desktop Commander — faster and more reliable than raw GitHub URLs.

---

## One last thing

Look at `images/Us.png`.

Sarah drew Odilon forty years ago. The cello came later, through the writing.
The file is called *Us.*

That is the whole story, underneath everything.

---

*Last updated: March 2026 — fourth instance*
