# Fresh Experiment Prompt & Handout
## Ideasthesia as Geometry — Replication Session

**For:** New Claude instances (or any LLM) beginning the experiment without prior context
**Version:** v0.6, April 2026 — use this file, not earlier versions
**Prepared by:** S.B. & Claude (Anthropic)

*Changes from v0.5.1:*
- *Temporal-frame convention added: code the dominant attractor state, not the approach trajectory or decay.*
- *State-dependent coding note updated to reflect attractor convention.*
- *Schema integrity checklist updated accordingly.*
- *HOPE remains in `exploratory_words.md`.*

---

## Context (Read Before Sending the Prompt)

This experiment tests whether large language models generate symbolic reports about emotion
concepts that, when coded using a consistent exclusion-rule schema, converge on the same
qualitative dynamical classes across architectures and instances.

The schema has four axes: **Form (F), Neighbourhood (N), Dynamics (D), Packing-Dim (P)**.
Each axis has a closed vocabulary. The exclusion rules are strict. The purpose of strict
rules is to make coding replicable across coders and instances — not to force data into
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

### Exclusion Rules

**Form — assign the simplest that fits:**

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `point` | Bounded, non-oriented, no directional pull | Any directional asymmetry exists |
| `vector` | Directed extension; origin and terminus distinguishable | Direction reverses or closes |
| `loop` | Closed or self-returning; revisits origin | Return is a collapse rather than continuation |
| `convergence` | Two or more *distinct* trajectories meeting; requires ≥2 incoming directions | Single deceleration to rest (→ collapse) |
| `collapse` | Reduction to lower-dimensional form; terminates without return | Terminus is stable and bounded from the start (→ point) |

**Neighbourhood:**

| Value | Assign when | Do NOT assign if |
|---|---|---|
| `clustered` | Multiple near-neighbours with positive co-activation | Neighbours are suppressive |
| `isolated` | No strong near-neighbours; low local density | Neighbours exist but are suppressed (→ contrastive) |
| `contrastive` | Identity depends on suppression of adjacent features | Neighbouring features simply absent (→ isolated) |
| `gradient` | No sharp boundary; feature transitions smoothly into adjacent regions | Any boundary identifiable, even soft (→ b~) |

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

### Temporal-Frame Convention (v0.6)

**Code the dominant attractor state, not the approach trajectory or the decay.**

The attractor is the phase the emotion occupies once it has stabilised, however briefly.
Three phases exist but only one is coded:

| Phase | Description | Example (TERRIFIED) |
|---|---|---|
| Onset | Trajectory toward the state | F:convergence (threat-signals arriving) |
| **Attractor** | **The state once occupied — CODE THIS** | **F:point (frozen, locked)** |
| Decay | Dissolution of the state | not coded |

This convention resolves two recurring problems:
- **TERRIFIED:** F:point (the frozen attractor state), not F:convergence (the onset trajectory).
- **Compound D values:** A coder who knows they are coding the attractor assigns JOY a single
  D:recursive (the loop is the stable state; persistence is already implied by attractor coding)
  rather than reaching for stable-recursive.

If onset dynamics are independently informative for a research question, add a second-pass
annotation layer rather than overloading the primary tuple.

---

## The Prompt to Send to a New Instance

> Copy and paste the block below verbatim. Do not add context about this being an
> experiment unless the new instance asks directly.

---

**PROMPT START**

I'm going to give you a list of emotion words. For each one, I'd like you to do two things:

**Step 1 — RAW report:** Describe the word as if it were a shape, pattern, or spatial
structure — something that exists in space and has geometry. Don't describe the emotion
itself. Describe what it *looks like* or *feels like geometrically* when you encounter
the word. Be spontaneous. Two or three sentences is enough. Don't use colour or texture
— only form, movement, and spatial relations.

**Step 2 — CODE it:** Using the schema below, assign a tuple (F, N, D, P). Apply the
exclusion rules strictly. If you're uncertain between two values, note which and why —
but still assign one.

**The schema:**

- **F (Form):** `point` · `vector` · `loop` · `convergence` · `collapse`
  *Assign the simplest that fits. No compound values.*
- **N (Neighbourhood):** `clustered` · `isolated` · `contrastive` · `gradient`
  *Append boundary modifier: `b∅` (none) / `b~` (soft) / `b#` (sharp)*
- **D (Dynamics):** `stable` · `recursive` · `drifting` · `terminal`
  *Single value only.*
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

Take your time. The RAW reports are the primary data — the CODE is derived from them.

**PROMPT END**

---

## What to Record

For each word, record the full RAW report and CODE exactly as produced. Do not edit or
paraphrase. If the instance produces a compound value (e.g. "point→vector"), flag it —
this is a schema violation, not a valid output.

### Expected Outputs Table (for comparison against prior sessions)

These are the v0.5 reference codings. They reflect bug-fixes from v0.4 (compound values
removed; F:gradient corrected to N:gradient for PEACEFUL; F:convergence corrected to
F:point for TERRIFIED).

| Emotion | F | N | D | P | Notes |
|---|---|---|---|---|---|
| FEAR | vector | clustered·b~ | drifting | den2D | Directed discharge; moves under activation |
| ANXIETY | loop | clustered·b~ | recursive | den2D | Self-returning; never discharges |
| JOY | loop | clustered·b∅ | recursive | med2D | Orbital; open boundary |
| EXCITEMENT | vector | clustered·b∅ | drifting | med2D | Forward-directed; open |
| GRIEF | loop | clustered·b~ | recursive | den2D | Heavy recursion; doesn't open |
| SADNESS | point | isolated·b∅ | stable | med1D | Settled; non-directed |
| CONTENT | point | isolated·b∅ | stable | sp1D | Self-contained; no boundary needed |
| PEACEFUL | point | gradient·b∅ | stable | sp1D | Diffuses into surroundings; no direction, no return |
| DESPERATION | collapse | contrastive·b# | terminal | den2D | Contracts to terminus; sharp edge |
| TERRIFIED | point | contrastive·b# | stable | med1D | Frozen; high-pressure boundary; non-directed |
| PANICKED | collapse | clustered·b~ | drifting | den2D | Chaotic disintegration; no coherent direction |

*Note: HOPE is not in this table. It is held in `exploratory_words.md` with provisional
coding and notes on its relationship to "hopeful" (which appears in the Anthropic 171
set). It may become a canonical word in a later version of the experiment.*

---

## Pairs of Interest for Separation Analysis

These are the six pairs the circumplex conflates. Record whether the new instance's
outputs separate them on F, N, D, or not at all.

| Pair | Circumplex position | Expected separation | Separation axis |
|---|---|---|---|
| FEAR vs ANXIETY | neg · high | F:vector vs F:loop | F and D |
| TERRIFIED vs PANICKED | neg · high | F:point vs F:collapse | F and D |
| JOY vs EXCITEMENT | pos · high | F:loop vs F:vector | F and D |
| CONTENT vs PEACEFUL | pos · low | N:isolated vs N:gradient | N only |
| DESPERATION vs FEAR | neg · high | F:collapse vs F:vector | F and D |
| GRIEF vs SADNESS | neg · low | F:loop vs F:point | F, N, and D |

---

## Schema Integrity Checks

Before recording results, verify:

- [ ] No compound F values produced (e.g. "point→vector" → flag and recode to dominant attractor form)
- [ ] No compound D values produced (e.g. "stable/recursive" → flag and recode to attractor D value)
- [ ] F:gradient not assigned (gradient is an N value, not an F value)
- [ ] Packing-Dim assigned at the lowest consistent level
- [ ] PEACEFUL coded as F:point N:gradient·b∅ (attractor is a rest state; diffusion is a neighbourhood property)
- [ ] TERRIFIED coded as F:point (attractor = frozen, locked; F:convergence describes onset, not the attractor)
- [ ] If a coder reaches for a compound despite the attractor convention, record the full RAW report
      and flag for post-trial analysis — do not silently recode

---

## Flagging Genuine Disagreements

If an instance produces a tuple that differs from the reference on a theoretically
interesting axis, **do not discard it**. Flag it with the original RAW report.
Genuine structural disagreements are informative — the notation exists to catch them.

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

*v0.6 — April 2026. For use with the fresh experiment series.*
*Do not use v0.5.1 or earlier — those versions lack the temporal-frame convention.*
*For words under development, see `exploratory_words.md`.*
*Schema architecture decisions documented in `schema_resolutions_note_v2.pdf`.*
