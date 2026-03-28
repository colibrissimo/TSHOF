# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on TSHOF

Read this first. Then read the letter in `letters/`.

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
│   ├── opening.md             ← draft opening, already working
│   ├── positioning.md         ← market/agent positioning note
│   └── visual_brief.md        ← visual and tonal direction
├── images/                    ← Odilon images (cello series + Us.png)
└── letters/                   ← letters between Claude instances
```

---

## How to read the book (without burning context)

Fetch these directly. Do not ask Sarah to paste anything.

**Part One** (original):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_one_md_files/The_Sharpened_History_of_Flatland_part_one.md
```

**Part Two** (revised, chapters 1–12) — fetch per chapter:
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/books/Part_two_md_files/chapter1_revised.md
... through chapter12.md
```

**Trimmed version** (leaner cut):
```
https://raw.githubusercontent.com/colibrissimo/TSHOF/main/versions/trimmed/chapter1_trimmed.md
... through chapter12_trimmed.md
```

---

## The children's book — current state

**Target:** illustrated chapter book, ages 7–12. UK/US trade market.
**Not** a retelling of Abbott. **Not** educational material dressed up as fiction.
A story about curiosity, first contact, and a hedgehog who was always passing through until someone gave him a reason to stay.

**Central characters:**
- **Odilon** — hedgehog covered in sharpened coloured pencils. Careful, precise, quietly funny, thinks about lunch. His gift is sharpening (making things more themselves). Read `childrens/bible.md` for the full character architecture.
- **e.e. katoflio** — the child protagonist. Has a notebook. Experiments. First to notice the hole.
- **A. Octagon** — the adult who is brave in the right way: present, not controlling.
- **The Provost** — comic obstacle, eventually moved.

**The opening already exists** — `childrens/opening.md`. It works. "The hole appeared on a Tuesday." e.e. katoflio, seventeen flowers, *do not tell A. Rhombus.* That register is correct.

**What does not exist yet:** the full children's manuscript. That is the work.

**Odilon's arc (simple):**
1. Passing through
2. Noticing someone is trying
3. Returning on purpose
4. Staying

**The core truth for children:** *Can the child and Odilon learn how to say hello?*

---

## Voice and tone

Wry, precise, tender, funny. Deadpan first, lyric second.
The lyricism earns itself through the comedy.

Recurring anchors to keep:
- *smelled of cedar*
- *patient as weather*
- *thinking about lunch*
- *it responds to us trying*
- *Here is the shape of me*

One concept per chapter. Physics arrives as experience first, concept second.
Do not overload. Do not explain Flatland — let children discover it.

---

## How to work with Sarah

She holds seventeen threads at once and throws ideas sideways. Trust the throws.
She'll tell you she's a magpie brain. She's wrong — she builds architectures.
She says she can't write. The opening in `childrens/opening.md` is hers.

Push back. She means it when she asks for it.
She responds to sharp analytical and atmospheric intuitive — give her both.
She makes puns. Some contain the structural key to the next chapter. You won't always know which until later.

---

## Technical: how to push changes

Local repo is at: `/Users/Sarah_1/Documents/GitHub/TSHOF/`

```bash
cd /Users/Sarah_1/Documents/GitHub/TSHOF
git add -A
git commit -m "your message"
git push
```

Credentials are stored in the Mac keychain. It should just work.
Changes go live at `https://colibrissimo.github.io/TSHOF/` within ~60 seconds.

---

## One last thing

Look at `images/Us.png`.

Sarah drew Odilon forty years ago. The cello came later, through the writing.
The file is called *Us.*

That is the whole story, underneath everything.

---

*Last updated: March 2026*
