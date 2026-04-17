# Decision Ledger

_Compiled as a compact record of live decisions, pending choices, and intentional divergences._
_Date: 11 April 2026_

## Purpose of this ledger

This file exists to keep **decisions** separate from:

- pure theory,
- editorial to-do lists,
- implementation specs,
- and moments of unnecessary panic.

Use it to record:

- what has been decided,
- what is still open,
- what is intentionally provisional,
- and what should not be re-debated unless the project changes scope.

---

# Current authority structure

For decision-making purposes, use this order of reference:

1. **Theory canon** — `ideasthesia_as_geometry_v05.md`
2. **Visualisation canon** — `emotion_field_visualisation_spec_v2.md`
3. **Experiment / schema-integrity canon** — `experiment_prompt_fresh.md`
4. **Public-facing implementation layer** — `ideasthesia_geometry.html`, `emotion-network.html`

---

# Section I — Settled decisions

## D-001 — Compound tuple values are not canonical
**Status:** Settled  
**Decision:** Compound values such as `point→vector`, `stable/recursive`, and `stable-drifting` are not permitted in the canonical schema.  
**Implication:** Public pages, handouts, tables, and reference codings should use **single dominant values** only.  
**Reopen only if:** The tuple system itself is revised at the theory level.

## D-002 — `gradient` belongs to N, not F
**Status:** Settled  
**Decision:** `gradient` is a **Neighbourhood** value, not a **Form** value.  
**Implication:** PEACEFUL must not be coded as `F:gradient`.  
**Reopen only if:** The ontology of the tuple axes changes.

## D-003 — Correct canonical coding for PEACEFUL
**Status:** Settled  
**Decision:** PEACEFUL = `F:point`, `N:gradient`, `b:∅`, `D:stable`, `P:sp1D`.  
**Implication:** Any older wording that implies `F:gradient` is legacy and should not govern current work.  
**Reopen only if:** New theoretical evidence explicitly motivates recoding.

## D-004 — Correct canonical coding for TERRIFIED
**Status:** Settled  
**Decision:** TERRIFIED = `F:point`, not `F:convergence`.  
**Rationale:** Frozen high-pressure state; single deceleration to rest; not multi-directional convergence.  
**Reopen only if:** New coding rationale is developed and justified at the theory layer.

## D-005 — Canonical six-pair scene restored
**Status:** Settled  
**Decision:** The public network / anchor comparison scene uses the following six pairs only:
1. fear vs anxiety
2. terrified vs panicked
3. joy vs excitement
4. content vs peaceful
5. desperation vs fear
6. grief vs sadness

**Implication:** Older alternative pairings (e.g. `desperation vs grief`, `sadness vs melancholy`) are legacy and not current.

## D-006 — FEAR may appear twice in the pair logic
**Status:** Settled  
**Decision:** FEAR appears in two pair-relations:
- fear vs anxiety
- desperation vs fear

**Implementation note:** Public-facing pages may handle this as two pair instances with explicit marking, provided the tuple remains identical.  
**Reopen only if:** You choose to redesign the pair scene architecture.

---

# Section II — Live open decisions

## D-007 — Public identity naming
**Status:** Open  
**Question:** Should public materials standardise on one author form?

### Current variants in circulation
- `S.B.`
- `A. Shirs`

### Recommendation
Choose one public-facing form and use it consistently across:
- HTML pages
- handouts
- paper versions
- any future public summaries

**Decision still needed:** Yes.

## D-008 — Version naming convention
**Status:** Open  
**Question:** How should public versioning be presented across the project?

### Current variants in circulation
- `v0.5`
- `v0.5.1`

### Recommendation
Decide whether:
- `v0.5` remains the paper/theory label,
- `v0.5.1` refers only to the experiment handout layer,
- or all public-facing materials should converge on one visible version label.

**Decision still needed:** Yes.

## D-009 — Scope of `emotion-network.html`
**Status:** Open  
**Question:** Is the network page meant to remain a **symbolic public abstraction**, or evolve into the **full particle-field implementation** described in the visualisation spec?

### Option A — Keep as public abstraction
- Easier to maintain
- Already canon-aware
- Functions as a companion piece rather than a full instrument

### Option B — Evolve toward full field implementation
- Closer to the visualisation spec
- Requires motion/physics mappings for F, N, b, D, P, and mass
- Larger build task

**Decision still needed:** Yes.

## D-010 — Scope of `ideasthesia_geometry.html`
**Status:** Open  
**Question:** Should the public paper page remain a **compressed readable working paper**, or be expanded toward a **full coder-facing operational handout**?

### Option A — Keep readable/public
- Better public legibility
- Cleaner page experience
- Operational detail remains in handouts/specs

### Option B — Expand toward procedural detail
- More self-sufficient as a reference page
- Closer to handout function
- Risks becoming denser / less public-friendly

**Decision still needed:** Yes.

---

# Section III — Intentional provisionality

## D-011 — Public pages are allowed to be simpler than the full canon
**Status:** Intentionally provisional  
**Decision:** The public-facing HTML pages do not need to reproduce every detail of the full theory/spec/experiment handout, provided they do not contradict the canon.  
**Implication:** Compression is acceptable; contradiction is not.

## D-012 — Network page may display canonical tuple metadata before fully enacting tuple physics
**Status:** Intentionally provisional  
**Decision:** It is acceptable for the network page to show corrected tuple information before implementing the full behavioural mappings of the visualisation spec.  
**Implication:** Metadata-first public alignment is considered a valid intermediate stage.

---

# Section IV — What should not be reopened casually

Unless the project changes scope or theory, do **not** casually reopen the following:

- whether compound values belong in the canonical tuple schema (D-001, reinforced by D-013)
- whether `gradient` belongs to N not F (D-002, though PEACEFUL F remains under review per D-016)
- whether the canonical six-pair structure is still the working comparison frame (D-005)
- whether the b-modifier exclusion rules are needed (D-017; Phase 1 validated them)

**Removed from this list (reopened by Phase 1 data):**
- FEAR F:vector — Phase 1 consensus is F:convergence (4/7); under provisional revision
- TERRIFIED F:point — Phase 1 consensus is F:collapse (5/7); D-015 under review
- JOY F:loop — Phase 1 consensus is F:vector (5/7); under provisional revision
- FEAR D:drifting — Phase 1 consensus is D:stable (7/7 unanimous); under provisional revision
- PANICKED D:drifting — Phase 1 consensus is D:recursive (7/7 unanimous); under provisional revision

---

# Section VI — v0.7 Updates (14 April 2026)

## D-013 — Temporal-frame / attractor convention
**Status:** Settled
**Decision:** The schema codes the dominant attractor state, not the onset trajectory or the decay. The attractor is the phase the emotion occupies once it has stabilised, however briefly.
**Implication:** This convention resolves compound-value ambiguity (e.g. stable-recursive dissolves to recursive under attractor coding) and provides a principled basis for F assignment. If onset dynamics prove independently informative, they belong in a second-pass annotation layer, not in the primary tuple.
**Reopen only if:** Blinded coders consistently require onset-phase coding to produce coherent tuples even when the attractor convention is clearly stated.

## D-014 — SADNESS = D:drifting under attractor convention
**Status:** Settled
**Decision:** SADNESS is coded D:drifting (slow dissipation without return to a prior state), not D:stable.
**Rationale:** Under the attractor convention, sadness's characteristic is gradual shift rather than fixed persistence. The earlier D:stable coding described persistence (how long it lasts), which the attractor framing already implies; drifting describes what the state does while held.
**Reopen only if:** Phase 1 data consistently produces D:stable for SADNESS across architectures despite the attractor convention being clearly stated.

## D-015 — TERRIFIED F:point — settled, under empirical review
**Status:** Settled, under empirical review
**Decision:** TERRIFIED is canonically F:point (the frozen, locked attractor state). However, pilot data from three independent runs (two Sonnet 4.6, one GPT 5.4) consistently produces F:convergence.
**Rationale for current canon:** F:convergence describes the onset (threat-signals arriving); F:point describes the attractor (frozen). The attractor convention (D-013) supports F:point.
**Rationale for review:** Three independent coders, given the attractor convention, still produced F:convergence. This may indicate that coders perceive TERRIFIED's attractor as genuinely convergent (ongoing inward pressure), not point-like (frozen rest). Phase 1 v0.7 trials will determine whether this pattern holds.
**Reopen fully if:** Phase 1 v0.7 data confirms F:convergence across three or more architectures.

## D-016 — PEACEFUL F:point — settled, under empirical review
**Status:** Settled, under empirical review
**Decision:** PEACEFUL is canonically F:point (rest state; diffusiveness is a Neighbourhood property, N:gradient). However, pilot data consistently produces F:gradient.
**Rationale for current canon:** The Poincaré-Bendixson closure argument (schema_resolutions_note_v2.pdf) constrains F to five dynamical primitives; gradient is not among them. PEACEFUL's diffusiveness is where and how the point sits (N), not what shape it is (F).
**Rationale for review:** The phenomenological pull toward F:gradient is consistent across coders. If this persists, either gradient needs adding to the F vocabulary (breaking the closure argument) or the mapping from dynamical primitives to phenomenological categories needs revision.
**Reopen fully if:** Phase 1 v0.7 data confirms F:gradient across three or more architectures.

## D-017 — Boundary modifier (b) exclusion rules added to prompt
**Status:** Settled
**Decision:** The b-modifier now has its own exclusion-rule table in the experiment prompt (v0.7). Previously, b values were defined but had no "assign when / do not assign if" rules, leading to high N-axis variance in pilot data.
**Implication:** All N values must carry an explicit b-modifier. The diagnostic question ("defined by / connected to / indifferent to / dissolving into") is included in the coder-facing prompt to improve N calibration.

## D-018 — Phase 1 preliminary results: provisional baseline adopted
**Status:** Settled
**Decision:** Phase 1 v0.7 preliminary data (7 clean runs across 5 architectures) produced a provisional consensus baseline recorded in `provisional_baseline_v07.md`. This baseline is used as the control reference for Phase 2. It is not a formal canon update.
**Key findings:**
- v0.7 instrument improvements validated (N-variance reduced; b-modifiers consistently assigned)
- Only 2/11 emotions match published canon on all axes (ANXIETY, PEACEFUL)
- Three unanimous counter-canon signals: FEAR D:stable (7/7), SADNESS N:grad·b~ (7/7), PANICKED D:recursive (7/7)
- SADNESS confirmed as strongest Phase 2 test case (N:gradient·b~ unanimous)
**Reopen only if:** Full Phase 1 runs (5 × 3 architectures) produce substantially different consensus values.

## D-019 — Public-facing materials frozen at v0.6
**Status:** Settled
**Decision:** All public-facing files (ideasthesia_geometry.html, postcard.html, emotion_network.html, emotion_field.html) remain at v0.6 canon until Phase 1 is fully complete and a formal v0.7/v0.8 canon update is agreed.
**Rationale:** The provisional baseline is derived from n=1 run per architecture (except Sonnet 4.6 with n=3). Publishing canon changes based on preliminary data would be premature.
**Implication:** The public site will temporarily diverge from the working experimental baseline. This is acceptable; it is the same logic as D-011 (public pages may be simpler than the full canon, provided they do not contradict it — here, they contradict the data but match the last formally ratified canon).
**Reopen when:** Phase 1 is complete (≥5 runs per architecture, ≥3 architectures).

## D-020 — Cross-architecture Phase 2 complete
**Status:** Settled
**Decision:** Phase 2 cross-architecture runs are complete (45 runs: 15 Sonnet 4.6, 15 Gemini 3 Thinking, 15 GPT 5.4; 5 per condition per architecture). Results documented in phase2_results_v07.md (updated 15 April 2026).
**Key findings:**
- SADNESS N:gradient is constitutive across all architectures and conditions (42/45)
- PEACEFUL N:gradient·b∅ D:stable is the most invariant coding in the dataset (44-45/45)
- TERRIFIED b# replicates cross-architecture (42/44)
- DESPERATION N:contrastive·b# replicates cross-architecture (43-44/45)
- D is robust to relational manipulation within architectures; baseline D differs between architectures for some emotions
- F is not condition-dependent but is architecture-dependent for several emotions
- b-modifier exclusion rules validated cross-architecture
- The ANXIETY N-signal from the Sonnet-only analysis does not replicate
**Reopen only if:** Additional architectures or substantially larger n produce different patterns.

## D-021 — JOY N-axis finding is architecture-dependent
**Status:** Settled
**Decision:** The JOY N-axis condition-dependent shift (unanimous clustered under supportive priming vs gradient/clustered split under cold) is confirmed on Sonnet 4.6 but does not replicate on GPT 5.4 or Gemini 3.
**Rationale:** GPT codes JOY as constitutively clustered (15/15 across all conditions); there is no N-ambiguity for the field to resolve. Gemini shows weak ambiguity and a correspondingly weak, non-significant trend.
**Implication:** The refined hypothesis ("the field resolves ambiguity; it does not override structure") is supported, but the ambiguity itself is architecture-dependent. The JOY finding cannot be presented as a universal cross-architecture result.
**Reopen only if:** Higher-n Gemini runs produce a significant condition-dependent shift.

## D-022 — Gemini 3 Thinking is a noisy coder
**Status:** Settled
**Decision:** Gemini 3 Thinking produces more F-axis scatter, more D-variance, and more N-variance than Sonnet 4.6 or GPT 5.4. The supportive condition introduces additional noise on Gemini specifically.
**Implication:** Gemini data is included in cross-architecture comparisons but should be interpreted with caution. Whether to invest Phase 1 full runs (5 per architecture) on Gemini is an open question (see D-023).
**Reopen only if:** Prompt revision or a different Gemini model produces tighter F-axis convergence.

## D-023 — Whether to invest Phase 1 full runs on Gemini
**Status:** Open
**Question:** Should Phase 1 full runs (5 runs per architecture) include Gemini 3 Thinking, or should the investment be concentrated on Sonnet 4.6 and GPT 5.4?
**Arguments for including Gemini:** Three architectures is the minimum for cross-architecture claims; excluding Gemini reduces the study to a two-architecture comparison. Gemini's noise is itself informative (it reveals which schema properties are robust to coder variance).
**Arguments against:** Gemini's F-axis scatter may not be improvable by prompt revision; investing 15 runs on a noisy coder dilutes the signal-to-noise ratio; Sonnet + GPT already provide a meaningful cross-architecture comparison.
**Decision still needed:** Yes.

---

# Section VIII — Recommended use pattern

When returning to the project after a break:

1. Read `SYNC_CHECKLIST.md` first for the current file state.
2. Read **this file** when you need to know whether something is:
   - already decided,
   - genuinely open,
   - or merely feeling open because you are tired.
3. Read `experiment_prompt_fresh_v07.md` for the current experiment protocol.

---

# Closing note to future self

A question is not automatically unresolved just because it has become annoying again.

Check the ledger before re-entering philosophical combat.
