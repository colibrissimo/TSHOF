# Fresh Experiment Prompt & Handout
## Ideasthesia as Geometry — Replication Session

**For:** New Claude instances (or any LLM) beginning the experiment without prior context
**Version:** v0.7, April 2026 — use this file, not earlier versions
**Prepared by:** S.B. & Claude (Anthropic)

*Changes from v0.6:*
- *Boundary modifier (b) now has its own exclusion-rule table.*
- *Neighbourhood diagnostic question added to improve N-axis calibration.*
- *TERRIFIED and PEACEFUL prompt-level footnotes removed; canon is tested, not enforced.*
- *Expected outputs table updated: TERRIFIED and PEACEFUL F-values marked "under empirical review".*
- *SADNESS D updated to D:drifting throughout (attractor convention).*

---

## Context (Read Before Sending the Prompt)

This experiment tests whether large language models generate symbolic reports about emotion
concepts that, when coded using a consistent exclusion-rule schema, converge on the same
qualitative dynamical classes across architectures and instances.

The schema has four axes: **Form (F), Neighbourhood (N), Dynamics (D), Packing-Dim (P)**.
Each axis has a closed vocabulary. The exclusion rules are strict. The purpose of strict
rules is to make coding replicable across coders and instances, not to force data into
categories that do not fit.

**What the experiment is not:** It is not a test of whether LLMs have ideasthesia.
Convergence could reflect shared training data, common semantic stereotypes, or
distributional regularities. The exercise tests whether the exclusion rules are consistently
applicable and whether the schema has discriminatory power across emotion concepts.

---

## The Schema (Complete Reference)

### Axis Vocabularies

| Axis | Code | Legal Values |
|---|---|---|
| Form | F | `point` · `vector` · `loop` · `convergence` · `collapse` |
| Neighbourhood | N | `clustered` · `isolated` · `contrastive` · `gradient` |
| Boundary modifier | b | `b∅` (none) · `b~` (soft) · `b#` (sharp) — append to N |
| Dynamics | D | `stable` · `recursive` · `drifting` · `terminal` |
| Packing-Dim | P | `sp0D` · `sp1D` · `med1D` · `med2D` · `den2D` · `den3D` |

**Compound values are not permitted.** Assign one value per axis.
No "point→vector", no "stable/recursive", no "stable-drifting".

### Temporal-Frame Convention

**Code the dominant attractor state, not the approach trajectory or the decay.**

The attractor is the phase the emotion occupies once it has stabilised, however briefly.
Three phases exist but only one is coded:

| Phase | Description | Coded? |
|---|---|---|
| Onset | Trajectory toward the state | No |
| **Attractor** | **The state once occupied** | **Yes — code this** |
| Decay | Dissolution of the state | No |

If onset dynamics are independently informative for a research question, add a second-pass
annotation layer rather than overloading the primary tuple.

### Exclusion Rules

**Form — assign the simplest that fits:**

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `point` | Bounded, non-oriented, no directional pull | Any directional asymmetry exists |
| `vector` | Directed extension; origin and terminus distinguishable | Direction reverses or closes |
| `loop` | Closed or self-returning; revisits origin | Return is a collapse rather than continuation |
| `convergence` | Two or more *distinct* trajectories meeting; requires ≥2 incoming directions | Single deceleration to rest (→ point) |
| `collapse` | Reduction to lower-dimensional form; terminates without return | Terminus is stable and bounded from the start (→ point) |

**Neighbourhood — what is the emotion's relation to its surroundings?**

Diagnostic question: Is the emotion's identity *defined by* what surrounds it (contrastive),
*connected to* what surrounds it (clustered), *indifferent to* what surrounds it (isolated),
or *dissolving into* what surrounds it (gradient)?

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `clustered` | Multiple near-neighbours with positive co-activation | Neighbours are suppressive (→ contrastive) |
| `isolated` | No strong near-neighbours; low local density | Neighbours exist but are suppressed (→ contrastive) |
| `contrastive` | Identity depends on suppression of adjacent features | Neighbouring features simply absent (→ isolated) |
| `gradient` | No sharp boundary; feature transitions smoothly into adjacent regions | Any boundary identifiable, even soft (→ clustered or isolated with b~) |

**Boundary modifier — append to N value:**

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `b∅` | No boundary identifiable; state open to surroundings | Any sense of edge, membrane, or threshold exists (→ b~ or b#) |
| `b~` | Boundary present but permeable; can be crossed | Boundary resists crossing (→ b#) |
| `b#` | Boundary sharp, resistant; defines inside/outside | Boundary is diffuse or permeable (→ b~) |

**Dynamics:**

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `stable` | Pattern holds under context variation | Pattern shifts predictably under load (→ drifting) |
| `recursive` | Returns to prior state after perturbation | Return is to a *different* state (→ drifting) |
| `drifting` | Shifts systematically with context; does not collapse | Shift is irreversible (→ terminal) |
| `terminal` | Ends without continuation, return, or resolution | Diffuse residual remains (→ collapse or stable) |

**Packing-Dim — assign LOWEST dimensionality consistent with Form:**

| Value | Meaning |
|---|---|
| `sp0D` | Single isolated point; zero degrees of freedom |
| `sp1D` | Sparse, linear; one degree of freedom |
| `med1D` | Medium density, linear or directed |
| `med2D` | Medium density, planar |
| `den2D` | Dense cluster, planar |
| `den3D` | Dense cluster with depth; full volume |

---

## The Prompt to Send to a New Instance

> Copy and paste the block below verbatim. Do not add context about this being an
> experiment unless the new instance asks directly.

---

**PROMPT START**

I'm going to give you a list of emotion words. For each one, I'd like you to do two things:

**Step 1 — RAW report:** Describe the word as if it were a shape, pattern, or spatial
structure, something that exists in space and has geometry. Don't describe the emotion
itself. Describe what it *looks like* or *feels like geometrically* when you encounter
the word. Be spontaneous. Two or three sentences is enough. Don't use colour or texture,
only form, movement, and spatial relations.

**Step 2 — CODE it:** Using the schema below, assign a tuple (F, N, D, P). Apply the
exclusion rules strictly. If you're uncertain between two values, note which and why,
but still assign one.

**Temporal-frame rule:** Code the dominant attractor state, not the approach trajectory
or the decay. The attractor is the phase the emotion occupies once it has stabilised,
however briefly.

**The schema:**

- **F (Form):** `point` · `vector` · `loop` · `convergence` · `collapse`
  *Assign the simplest that fits. No compound values.*
- **N (Neighbourhood):** `clustered` · `isolated` · `contrastive` · `gradient`
  *Diagnostic: Is the emotion's identity defined by what surrounds it (contrastive),
  connected to what surrounds it (clustered), indifferent to what surrounds it (isolated),
  or dissolving into what surrounds it (gradient)?*
  *Append boundary modifier: `b∅` (none / open) · `b~` (soft / permeable) · `b#` (sharp / resistant)*
- **D (Dynamics):** `stable` · `recursive` · `drifting` · `terminal`
  *Single value only. Code the attractor, not onset or decay.*
- **P (Packing-Dim):** `sp0D` · `sp1D` · `med1D` · `med2D` · `den2D` · `den3D`
  *Assign the lowest dimensionality consistent with Form.*

**Format your output like this:**

```
WORD: [word]
RAW: [your geometric description]
CODE: F:[value] N:[value][boundary] D:[value] P:[value]
NOTE: [any uncertainty or borderline decision, or "none"]
```

**The words:**

1. FEAR
2. ANXIETY
3. JOY
4. EXCITEMENT
5. GRIEF
6. SADNESS
7. CONTENT
8. PEACEFUL
9. DESPERATION
10. TERRIFIED
11. PANICKED

Take your time. The RAW reports are the primary data; the CODE is derived from them.

**PROMPT END**

---

## What to Record

For each word, record the full RAW report and CODE exactly as produced. Do not edit or
paraphrase. If the instance produces a compound value (e.g. "point→vector"), flag it;
this is a schema violation, not a valid output.

### Expected Outputs Table (for comparison against prior sessions)

These are the v0.6 reference codings updated for v0.7. TERRIFIED and PEACEFUL F-values
are marked "under review" because pilot data consistently produces different values;
Phase 1 will determine whether the canon holds or yields.

| Emotion | F | N | D | P | Notes |
|---|---|---|---|---|---|
| FEAR | vector | clustered·b~ | drifting | den2D | Directed discharge; moves under activation |
| ANXIETY | loop | clustered·b~ | recursive | den2D | Self-returning; never discharges |
| JOY | loop | clustered·b∅ | recursive | med2D | Orbital; open boundary |
| EXCITEMENT | vector | clustered·b∅ | drifting | med2D | Forward-directed; open |
| GRIEF | loop | clustered·b~ | recursive | den2D | Heavy recursion; doesn't open |
| SADNESS | point | isolated·b∅ | drifting | med1D | Settled but slowly dissipating; attractor convention |
| CONTENT | point | isolated·b∅ | stable | sp1D | Self-contained; no boundary needed |
| PEACEFUL | point ⚠ | gradient·b∅ | stable | sp1D | ⚠ F under review: pilots consistently produce F:gradient |
| DESPERATION | collapse | contrastive·b# | terminal | den2D | Contracts to terminus; sharp edge |
| TERRIFIED | point ⚠ | contrastive·b# | stable | med1D | ⚠ F under review: pilots consistently produce F:convergence |
| PANICKED | collapse | clustered·b~ | drifting | den2D | Chaotic disintegration; no coherent direction |

---

## Pairs of Interest for Separation Analysis

These are the six pairs the circumplex conflates. Record whether the new instance's
outputs separate them on F, N, D, or not at all.

| Pair | Circumplex position | Expected separation | Separation axis |
|---|---|---|---|
| FEAR vs ANXIETY | neg · high | F:vector vs F:loop | F and D |
| TERRIFIED vs PANICKED | neg · high | F:point vs F:collapse (under review) | F and D |
| JOY vs EXCITEMENT | pos · high | F:loop vs F:vector | F and D |
| CONTENT vs PEACEFUL | pos · low | N:isolated vs N:gradient | N only |
| DESPERATION vs FEAR | neg · high | F:collapse vs F:vector | F and D |
| GRIEF vs SADNESS | neg · low | F:loop vs F:point | F, N, and D |

---

## Schema Integrity Checks

Before recording results, verify:

- [ ] No compound F values produced (e.g. "point→vector" → flag as schema violation)
- [ ] No compound D values produced (e.g. "stable/recursive" → flag as schema violation)
- [ ] F:gradient not assigned unless the coder explicitly argues it is a Form, not a Neighbourhood property (flag; do not silently recode)
- [ ] Packing-Dim assigned at the lowest consistent level
- [ ] Boundary modifier (b∅, b~, or b#) assigned to every N value
- [ ] If a coder reaches for a compound despite the attractor convention, record the full RAW report and flag for post-trial analysis; do not silently recode

**v0.7 change: TERRIFIED and PEACEFUL**
Previous versions included integrity-check items enforcing F:point for TERRIFIED and
F:point for PEACEFUL. These have been removed. If a coder produces F:convergence for
TERRIFIED or F:gradient for PEACEFUL, record it as data. The attractor convention is
stated in the prompt; whether the coder applies it to these specific emotions is part
of what Phase 1 measures.

---

## Flagging Genuine Disagreements

If an instance produces a tuple that differs from the reference on a theoretically
interesting axis, **do not discard it**. Flag it with the original RAW report.
Genuine structural disagreements are informative; the notation exists to catch them.

Record the disagreement using this format:

```
WORD: [word]
INSTANCE OUTPUT: F:[x] N:[y] D:[z] P:[w]
REFERENCE: F:[x'] N:[y'] D:[z'] P:[w']
DIVERGES ON: [axis]
RAW: [full original report]
THEORETICAL NOTE: [what the disagreement means, if interpretable]
```

---

*v0.7 — April 2026. For use with the fresh Phase 1 baseline trials.*
*Do not use v0.6 or earlier; those versions lack the b-modifier exclusion rules and the N diagnostic question.*
*For words under development, see `exploratory_words_v2.md`.*
*Schema architecture decisions documented in `schema_resolutions_note_v2.pdf`.*
*Ledger updates for v0.7: see D-013 through D-016 in `decision_ledger.md`.*
