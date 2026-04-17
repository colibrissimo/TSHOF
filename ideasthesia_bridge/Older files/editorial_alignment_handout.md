# Editorial Alignment Handout

_Compiled as a working checklist for later revision._
_Date: 11 April 2026_

## What this handout is for

This sheet is a practical editorial map for bringing the current website/pages into line with the **canonical sources** now in circulation.

## Canonical source hierarchy

Use this order of authority when updating anything:

1. **`ideasthesia_as_geometry_v05.md`** — canonical theory / paper text
2. **`emotion_field_visualisation_spec_v2.md`** — canonical visualisation / implementation spec
3. **`postcard_v1.md`** — bridge text, but currently still partly legacy
4. **`note_missing_word.md`** — framing note, not part of the core structural claim

---

# Executive summary

## Yes, both HTML pages need editing.

### Priority order

1. **`emotion-network.html`** — highest priority
   - The visualisation is currently using outdated pairings and pre-correction tuple values.
   - This matters most because it is interactive and therefore presents the old ontology as if it were current.

2. **`ideasthesia_geometry.html`** — second priority
   - The page is well designed but still contains older text-generation layers (v0.4 language, compound tuple values, earlier pair codings).

3. **Website bridge/postcard language** — third priority
   - Bring public-facing summary language into line **after** the two core pages are made canonical.

---

# Part I — `emotion-network.html`

## Editorial diagnosis

This page needs a **data-model correction pass**, not a visual redesign.

The rendering scaffold is broadly fine. What is outdated is the **embedded semantic content**, especially the `PAIRS` array and the tuple fields surfaced in the tooltip.

## Main problems to fix

### 1) Replace legacy tuple values with canonical atomic values

The current page still contains superseded values such as:

- `fear` = `F:'point-vector'`
- `terrified` = `F:'convergence'`
- `joy` = `D:'stable-recursive'`
- `peaceful` = `F:'gradient'`
- `sadness` = `D:'stable-drifting'`

These must be replaced with the canonical atomic values from the corrected paper/spec.

### 2) Restore the canonical six test pairs

The current page has drifted away from the intended six-pair scene.

#### Current non-canonical pairings present in the page
- `desperation` vs `grief`
- `sadness` vs `melancholy`

#### Canonical six pairs should be
1. fear vs anxiety
2. terrified vs panicked
3. joy vs excitement
4. content vs peaceful
5. desperation vs fear
6. grief vs sadness

### 3) Remove invalid `F:gradient`

`gradient` is **not** a valid Form value in the corrected schema.

For **peaceful**, the canonical coding is:
- `F: point`
- `N: gradient`
- `b: ∅`
- `D: stable`
- `P: sp1D`

### 4) Expand the tooltip / hover metadata

At present, the tooltip only shows:
- F
- D
- Quadrant

That is now too thin for the corrected schema.

The tooltip should ideally show:
- Name
- F
- N
- boundary (`b`)
- D
- P
- Quadrant

### 5) Decide whether FEAR appears as one reusable node or two separate rendered instances

Because the canonical six-pair scene includes:
- fear vs anxiety
- desperation vs fear

…you need to decide whether:
- FEAR is rendered once and conceptually reused, or
- FEAR appears twice as two scene instances in pair-logic terms.

This does **not** require a theoretical decision so much as an implementation clarification.

---

## Canonical replacement data for the six test pairs

Use this as the authoritative content block for later code replacement:

```js
const PAIRS = [
  {
    a: { name: 'fear',        F: 'vector',  N: 'clustered',   b: '~', D: 'drifting',  P: 'den2D', quadrant: 'neg-high' },
    b: { name: 'anxiety',     F: 'loop',    N: 'clustered',   b: '~', D: 'recursive', P: 'den2D', quadrant: 'neg-high' }
  },
  {
    a: { name: 'terrified',   F: 'point',   N: 'contrastive', b: '#', D: 'stable',    P: 'med1D', quadrant: 'neg-high' },
    b: { name: 'panicked',    F: 'collapse',N: 'clustered',   b: '~', D: 'drifting',  P: 'den2D', quadrant: 'neg-high' }
  },
  {
    a: { name: 'joy',         F: 'loop',    N: 'clustered',   b: '∅', D: 'recursive', P: 'med2D', quadrant: 'pos-high' },
    b: { name: 'excitement',  F: 'vector',  N: 'clustered',   b: '∅', D: 'drifting',  P: 'med2D', quadrant: 'pos-high' }
  },
  {
    a: { name: 'content',     F: 'point',   N: 'isolated',    b: '∅', D: 'stable',    P: 'sp1D',  quadrant: 'pos-low' },
    b: { name: 'peaceful',    F: 'point',   N: 'gradient',    b: '∅', D: 'stable',    P: 'sp1D',  quadrant: 'pos-low' }
  },
  {
    a: { name: 'desperation', F: 'collapse',N: 'contrastive', b: '#', D: 'terminal',  P: 'den2D', quadrant: 'neg-high' },
    b: { name: 'fear',        F: 'vector',  N: 'clustered',   b: '~', D: 'drifting',  P: 'den2D', quadrant: 'neg-high' }
  },
  {
    a: { name: 'grief',       F: 'loop',    N: 'clustered',   b: '~', D: 'recursive', P: 'den2D', quadrant: 'neg-low' },
    b: { name: 'sadness',     F: 'point',   N: 'isolated',    b: '∅', D: 'stable',    P: 'med1D', quadrant: 'neg-low' }
  }
];
```

---

## Minimal code-edit checklist for `emotion-network.html`

### A. Replace the existing `PAIRS` block
- Remove all legacy compound values.
- Remove `melancholy` from the six-pair anchor scene.
- Restore the correct final two pairs.

### B. Add `N`, `b`, and `P` to the tooltip
- Add three new rows in the tooltip HTML.
- Populate them in `showTooltip()`.

### C. Update the instruction copy
Current text:
- “Hover a named node to see its tuple.”

Suggested later wording:
- “Hover a named node to see its tuple code (F, N, b, D, P).”

### D. Check whether the visualisation should still be a sphere of six axes
This is not necessarily wrong, but it is now somewhat independent of the corrected visualisation spec, which frames the implementation more in terms of a field / circumplex / Z-spread system.

Leave this unless you want a later redesign.

### E. Optional later refinement
If you want the network page to reflect the corrected spec more deeply, eventually map:
- `P` to Z-depth or cluster density,
- `N` to inter-particle behaviour,
- `b` to edge/halo styling,
- `D` to motion model.

That is a second-stage enhancement, **not** a same-day obligation.

---

# Part II — `ideasthesia_geometry.html`

## Editorial diagnosis

This page needs a **content/version alignment edit**, not a structural rebuild.

The styling and page architecture are fine. The issue is that the content still reflects an earlier document generation.

## Main problems to fix

### 1) Update the version label
Current page header says:
- `Draft v0.4, April 2026`

This should be brought into line with the current paper version.

### 2) Remove legacy compound tuple language
The HTML page still includes older forms such as:
- `point→vector`
- `stable/recursive`
- `stable/drifting`

But the canonical paper now explicitly states:
- assign the **single dominant class**,
- **compound values are not permitted**.

### 3) Correct the six-pair table
The HTML page’s six-pair section still partly reflects the older layer of the project.

#### Specifically update:
- `fear` → `vector` (not `point→vector`)
- `terrified` → `point` (not `convergence`)
- `joy` → `recursive` (not `stable/recursive`)
- `sadness` → `stable` (not `stable/drifting`)
- `desperation vs fear` should use `collapse vs vector`
- Keep `content vs peaceful` as an **N-only separation** with both `F: point` and both `D: stable`

### 4) Update the pilot / example text where FEAR still appears as `point→vector`
There is still older wording in the pilot-data section.

Replace with the canonical value unless you deliberately keep the older surface description as historical context.

### 5) Add the “compound values not permitted” wording if absent
The canonical paper text contains a very important rule:
- assign the simplest value that fits,
- compound values are not permitted,
- assign the dominant/activated form.

This should be reflected clearly on the web page too.

---

## Minimal content checklist for `ideasthesia_geometry.html`

### Header and framing
- Update `Draft v0.4` → current draft/version label.
- Check author naming for consistency with the current paper.

### Tuple/exclusion-rule section
- Insert or restore the “compound values are not permitted” sentence.
- Add or keep the note that `gradient` belongs to `N`, not `F`, if this is not already obvious from context.

### Pilot data section
- Clean up any remaining transitional examples that imply compound F-values as canonical.

### Anthropic / emotion section
- Update the six-pair table to canonical atomic values.
- Ensure the prose beneath it matches the corrected pair table.
- Ensure the “specific prediction” uses the corrected Form values.

### Footer / bridge copy
- If the page says “full academic version available on request”, decide whether this remains true now that the fuller paper exists in working form.

---

# Part III — `postcard_v1.md`

## Status
Do **not** treat this as the source of truth.

It is still rhetorically strong, but it contains legacy coding language and should only be updated **after** the paper page and network page are aligned.

## Main things to fix later
- Replace compound values with canonical atomic values.
- Remove `point vs gradient` wording for `content vs peaceful`.
- Bring all six pairs into line with the paper/spec.

---

# Part IV — `note_missing_word.md`

## Status
Keep separate.

This note explicitly belongs to a different register:
- framing,
- instrument design,
- vocabulary omission,
not the narrow six-pair structural claim.

## Editorial instruction
Do not merge this into the core paper/spec/visualisation text unless you deliberately create a separate reflection or appendix.

---

# Safe working plan for later

## Session 1 — shortest useful pass
1. Update `emotion-network.html` `PAIRS` block.
2. Add `N`, `b`, `P` to tooltip.
3. Save and stop.

## Session 2
1. Update version number and six-pair table in `ideasthesia_geometry.html`.
2. Remove legacy compound values.
3. Save and stop.

## Session 3
1. Update postcard/public summary language.
2. Optional polish pass on phrasing.

---

# Final note to future self

Nothing here suggests the project is broken.

What happened is simpler:
- the theory matured,
- the spec matured,
- the website copies lagged behind.

This is an **alignment task**, not a collapse.
