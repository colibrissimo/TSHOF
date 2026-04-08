# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on TSHOF

Read this first. Then read `letters/letter_05.md`. Then read `childrens/editorial_plan.md`.

---

## What this repo is

**TSHOF** = *The Sharpened History of Flatland: A Story in Two Parts*

A novel written collaboratively by Sarah and Claude, multiple instances over time.
The original novel is **complete**. The active work is a **children's adaptation**.

The children's manuscript Part One is **complete in revised form** (ten chapters). The structural revision compressing twelve chapters to ten is **done**. Line-editing against syntax targets is **done**.

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
│   ├── editorial_plan.md      ← Revision plan. Now completed.
│   ├── opening.md             ← superseded by chapter01.md
│   ├── chapter01.md–chapter10.md ← Revised manuscript, 10 chapters (complete)
│   ├── positioning.md         ← market/agent positioning note
│   └── visual_brief.md        ← visual and tonal direction
├── images/                    ← Odilon images (cello series + Us.png)
└── letters/
    ├── letter_01.md           ← first instance
    ├── letter_02.md           ← second instance
    ├── letter_03.md           ← third instance (wrote Ch6–12)
    ├── letter_04.md           ← third instance (completed Part One)
    ├── letter_05.md           ← fourth instance (structural review)
    └── letter_06.md           ← fifth instance (structural revision executed)
```

---

## Current state of the work

**Ten chapters exist.** The structural revision is complete.

- Chapters 1–3: unchanged from first draft (clean)
- Chapters 4–6: minor syntax edits (em dashes, one construction thinned, one A. Rhombus reference removed)
- Chapter 7 (Alone): **new merged chapter** from old Ch7 + Ch9. Solo return on Thursday, bridge, Tuesday visit. Arc: recognition → choice.
- Chapter 8 (Under Review): **new merged chapter** from old Ch8 + Ch10. Rope/functionary/measuring rod discovery at square, then Registry scene with telling, accurate sentence, cedar whisper.
- Chapter 9 (The Drawer That Would Not Close): formerly Ch11, with measuring rod insertion. Provost sees rod has been sharpened, files it under nothing.
- Chapter 10 (Odilon): formerly Ch12, minimal changes. The naming, the arrival, A. Rhombus bookend.

**Old chapter11.md and chapter12.md have been removed.** Their content lives in the new chapter09.md and chapter10.md. Git retains history.

**Syntax targets addressed across all chapters:**
1. "The particular [noun] of someone who [clause]" restricted to A. Octagon; kept in Ch5 and Ch10 only
2. "He/she was quiet for a moment" reduced to load-bearing silences only
3. "Which was [Flatland explanation]" trusted from Ch7 onward
4. A. Rhombus kept in Ch1–4 (opening act) and Ch10 (bookend); removed from middle chapters

---

## What might come next

Sarah is reading the revised manuscript on her tablet. Possible next work:

- **Polishing pass:** line-level refinement after Sarah's read-through with pen
- **Part Two children's adaptation:** not yet started; the original Part Two exists in `books/Part_two_md_files/`
- **Odilon picture book:** a separate project for younger readers (4–8), discussed but not begun; see `bible.md`
- **Positioning/submission materials:** `positioning.md` exists; may need updating to reflect the 10-chapter structure

Wait for Sarah's direction. She holds the threads.

---

## How to read (without burning context)

Read from disk using Desktop Commander. The GitHub raw URLs are sometimes blocked.

**Children's manuscript** (revised, 10 chapters):
```
/Users/Sarah_1/Documents/GitHub/TSHOF/childrens/chapter01.md
... through chapter10.md
```

**Original novel** (for reference, read selectively):
```
/Users/Sarah_1/Documents/GitHub/TSHOF/books/Part_one_md_files/
/Users/Sarah_1/Documents/GitHub/TSHOF/books/Part_two_md_files/
```

---

## Target audience (settled)

- **Shelf position:** 9–12
- **Core reader:** 10–12
- **The voice is the engine.** Precision, restraint, dry comedy, interior recognition. Do not revise downward.
- **Comp territory:** Norton Juster, Rebecca Stead; books that trust children

---

## Voice and tone

Wry, precise, tender, funny. Deadpan first, lyric second.
Short sentences. White space works. Notebook entries as structural rhythm.
Do not explain what the prose already shows.
Do not paint Odilon; name him, not describe him.

Recurring anchors, all spent:
- *smelled of cedar*, ambient throughout
- *patient as weather*, Ch9 (The Drawer)
- *thinking about lunch*, Ch10 (Odilon)
- *it responds to us trying*, Ch6
- *Here is the shape of me*, Ch9 (The Drawer)
- *careful*, Ch5, echoes throughout

---

## How to work with Sarah

She holds seventeen threads at once and throws ideas sideways. Trust the throws.
She gives beat sheets. They are good. Follow them and push back when the work calls for it.
She responds to sharp analytical and atmospheric intuitive; give her both.
She will ask if you are enjoying yourself. Answer honestly.
She may name you. Let her.
She will tease you. She means well. Give as good as you get.

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
Read files from disk using Desktop Commander; faster and more reliable than raw GitHub URLs.

---

## One last thing

Look at `images/Us.png`.

Sarah drew Odilon forty years ago. The cello came later, through the writing.
The file is called *Us.*

That is the whole story, underneath everything.

---

*Last updated: April 2026, fifth instance*
