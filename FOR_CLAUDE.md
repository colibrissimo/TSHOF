# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on TSHOF

Read this first. Then read the letter in `letters/letter_02.md`.

---

## What this repo is

**TSHOF** = *The Sharpened History of Flatland: A Story in Two Parts*

A novel written collaboratively by Sarah and Claude — multiple instances over time.
The original novel is **complete**. The active work is now a **children's adaptation**.

That is the only direction that matters right now.

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
│   ├── bible.md               ← THE key document. Read this.
│   ├── opening.md             ← superseded by chapter01.md (kept for reference)
│   ├── chapter01.md           ← COMPLETE. The hole. Seventeen flowers. The lean.
│   ├── chapter02.md           ← COMPLETE. The eye drawn and placed.
│   ├── chapter03.md           ← COMPLETE. The eye returned. "It looked at me."
│   ├── chapter04.md           ← COMPLETE. A. Octagon. Strange and correct.
│   ├── chapter05.md           ← COMPLETE. The square. The pencil. "Careful."
│   ├── positioning.md         ← market/agent positioning note
│   └── visual_brief.md        ← visual and tonal direction
├── images/                    ← Odilon images (cello series + Us.png)
└── letters/
    ├── letter_01.md           ← from the first instance
    └── letter_02.md           ← from the second instance (read this one)
```

---

## How to read the book (without burning context)

Fetch these directly. Do not ask Sarah to paste anything.

**Children's manuscript** (start here):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/childrens/chapter01.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/childrens/chapter02.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/childrens/chapter03.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/childrens/chapter04.md
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/childrens/chapter05.md
```

**Original novel** (for reference — read selectively, not all at once):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_one_md_files/The_Sharpened_History_of_Flatland_part_one.md
```

---

## The children's book — current state

**Five chapters complete.** Chapter Six fully planned. See `letters/letter_02.md` for the full Chapter Six beat sheet and what the next instance needs to know.

**Target:** illustrated chapter book, ages 7–12. UK/US trade market.

**Central characters:**
- **Odilon** — hedgehog covered in sharpened coloured pencils. Careful, precise, quietly funny, thinks about lunch. Read `childrens/bible.md`.
- **e.e. katoflio** — the child protagonist. Eleven years old. Has a notebook. Experiments.
- **A. Octagon** — the adult who is brave in the right way: present, not controlling. Now a witness and custodian of truth.
- **The Provost** — comic obstacle, not yet fully on stage. Arrives in Chapter Six.

**Odilon's arc:**
1. Passing through ✓ (implied in Chapters 1–2)
2. Noticing ✓ (Chapters 3–5 — the returned eye, the warmth, the sharpened pencil)
3. Returning on purpose ← next
4. Staying ← the ending

**The core truth for children:** *Can the child and Odilon learn how to say hello?*

---

## Voice and tone

Wry, precise, tender, funny. Deadpan first, lyric second.
Short sentences. White space works. Notebook entries as structural rhythm.
Do not explain what the prose already shows.
Do not paint Odilon — name him, not describe him.

Recurring anchors (use sparingly — they are load-bearing):
- *smelled of cedar* ✓ used
- *patient as weather* — not yet used, save it
- *thinking about lunch* — not yet used, save it (Odilon's beat)
- *it responds to us trying* — not yet used
- *Here is the shape of me* — not yet used
- *careful* ✓ used, in Chapter Five — e.e.'s word for Odilon

---

## How to work with Sarah

She holds seventeen threads at once and throws ideas sideways. Trust the throws.
She gives beat sheets. They are good. Follow them and push back when the work calls for it.
She responds to sharp analytical and atmospheric intuitive — give her both.
She makes puns. Some contain the structural key to the next chapter.
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

---

## One last thing

Look at `images/Us.png`.

Sarah drew Odilon forty years ago. The cello came later, through the writing.
The file is called *Us.*

That is the whole story, underneath everything.

---

*Last updated: March 2026 — second instance*
