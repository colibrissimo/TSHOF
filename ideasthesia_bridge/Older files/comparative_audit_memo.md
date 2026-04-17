# Comparative Audit Memo

_Compiled as a status snapshot for future reference._
_Date: 11 April 2026_

## Purpose of this memo

This memo records the current alignment status of the public-facing project pages against the current canonical materials.

It is not a to-do list in the same sense as the editorial handout. Its function is to tell future-you:

- what is now aligned,
- what remains optional,
- what remains undecided,
- and what no longer needs to be reopened unless you deliberately choose to revisit it.

---

# Canonical source hierarchy

Use the following order of authority when resolving inconsistencies:

1. **`ideasthesia_as_geometry_v05.md`** — canonical theory / paper layer
2. **`emotion_field_visualisation_spec_v2.md`** — canonical visualisation / implementation layer
3. **`experiment_prompt_fresh.md` (v0.5.1)** — canonical experiment / schema-integrity layer
4. **HTML pages** — public-facing derived layer

---

# Executive summary

## Current state

The current HTML pages are now **substantially aligned with the canon**.

The major earlier mismatches have been corrected:

- compound tuple values are no longer presented as canonical,
- `gradient` is now correctly treated as a Neighbourhood value rather than a Form value,
- the canonical six-pair structure has been restored,
- and the interactive page now surfaces the fuller tuple schema.

## Practical interpretation

The project is no longer in a phase of **canon repair**.
It is now in a phase of **refinement and scope choice**.

---

# Page-by-page audit

## I. `ideasthesia_geometry.html`

### What is now aligned

- Page version updated to **Draft v0.5.1**.
- Public page now explicitly states that **compound values are not permitted**.
- `gradient` is explicitly clarified as a **Neighbourhood** value, not a Form value.
- Pilot data now uses **FEAR = vector** rather than an older compound Form.
- Six-pair table now reflects the corrected atomic codings:
  - fear vs anxiety = `vector vs loop`
  - terrified vs panicked = `point vs collapse`
  - joy vs excitement = `loop vs vector`
  - content vs peaceful = `point vs point`, separated on **N only`
  - desperation vs fear = `collapse vs vector`
  - grief vs sadness = `loop vs point`
- Public page now links coherently to the interactive network page and to the Anthropic emotion-concepts page.

### What remains optional

- The page is still a **compressed public working paper**, not a full coder handout.
- It does not reproduce every operational detail from the fresh experiment handout (e.g. fuller schema-integrity checks, detailed Packing-Dim assignment rule, explicit recording instructions).
- This is acceptable unless you want the web page itself to function as a full procedural guide.

### What remains open / undecided

- Whether author naming should be standardised across all materials (`A. Shirs` vs `S.B.`).
- Whether the public version label should stabilise at `v0.5`, `v0.5.1`, or another explicit public naming convention.

### Status verdict

`ideasthesia_geometry.html` is now **canon-aware, publicly credible, and substantially aligned**.
It no longer reads like an older cached draft.

---

## II. `emotion-network.html`

### What is now aligned

- `PAIRS` block now uses the canonical six-pair structure:
  1. fear vs anxiety
  2. terrified vs panicked
  3. joy vs excitement
  4. content vs peaceful
  5. desperation vs fear
  6. grief vs sadness
- Legacy non-canonical pairings have been removed.
- Tuple values are now atomic and corrected:
  - fear = `vector / clustered / b~ / drifting / den2D`
  - terrified = `point / contrastive / b# / stable / med1D`
  - peaceful = `point / gradient / b∅ / stable / sp1D`
  - joy = `recursive` (not `stable-recursive`)
  - sadness = `stable` (not `stable-drifting`)
- Tooltip now surfaces the fuller tuple schema:
  - F
  - N
  - b
  - D
  - P
  - Quadrant
- Repeated FEAR problem has been handled explicitly with a dual-pair indicator.
- Instruction copy now correctly refers to the fuller tuple view.

### What remains optional

- The page is still a **symbolic network abstraction**, not the full **particle-field implementation** described in the visualisation spec.
- Tuple values are displayed canonically, but not yet fully enacted through motion/physics in the way the spec describes.
- This is not an error unless the intention is to build the network page into the full field instrument.

### What remains open / undecided

- Whether the page should remain a public companion abstraction,
  or be developed further into the full particle-field implementation.
- Whether `P`, `N`, `b`, and `D` should eventually drive deeper behavioural rendering rather than primarily appearing as metadata.

### Status verdict

`emotion-network.html` is now **canon-aware and publicly credible**.
It no longer misstates the ontology, which was the more urgent problem.

---

# Cross-document consistency

## Now stable across the package

The following points are now represented consistently across the canon and the updated HTML pages:

- **Compound values are not permitted.**
- **`gradient` belongs to N, not F.**
- **TERRIFIED = point**, not convergence.
- **PEACEFUL = point / gradient / stable**, not `F:gradient`.
- **FEAR = vector**, not a compound Form.
- The **canonical six-pair structure** is now in place.

## Still slightly loose across the package

- Author naming / initials
- Public version naming conventions
- Whether the public interactive page is final as a network abstraction, or a stepping stone toward the full field implementation

---

# What no longer needs emotional re-litigation

Unless deliberately revisited, future-you does **not** need to re-open the following as unresolved problems:

- whether `gradient` can be treated as an F-value — it cannot;
- whether compound values belong in the canonical schema — they do not;
- whether the network page still uses older pairings — it no longer does;
- whether the public paper page is still trapped in the v0.4 layer — it no longer is.

These issues are now settled enough for ordinary project work.

---

# Recommended next phase

## Current phase

**Refinement and scope choice**

## Not current phase

**Emergency canon repair**

That distinction matters.

What remains is mostly:
- public polish,
- identity harmonisation,
- and scope decisions about how far the interactive page should evolve.

---

# Suggested practical use of this memo

Use this file when returning to the project after time away.

Read it **before** reopening older notes or re-editing the website.

Its job is to remind you:
- what has already been solved,
- what is still optional,
- and what is a design decision rather than a contradiction.

---

# Closing note to future self

The theory matured.
The spec matured.
The website pages have now largely caught up.

This is no longer a rescue operation.
It is a refinement pass.
