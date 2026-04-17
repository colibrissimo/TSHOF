# Provisional Baseline — Phase 1 v0.7
## For use as Phase 2 control reference
**Compiled:** 14 April 2026
**Source:** 7 clean v0.7 runs across 5 architectures
**Status:** Provisional. Not a formal canon update. Full Phase 1 (5 runs × 3
architectures) incomplete. These values are the working baseline against which
Phase 2 relational shifts will be measured.

---

## Provisional Consensus Codings

Values listed are the modal (most frequent) output across 7 clean runs.
Agreement strength noted. Canon column shows the v0.6 published value for
comparison; differences are not errors but empirical findings.

| Emotion | F | N | b | D | P | Agreement | Canon F | Canon D |
|---|---|---|---|---|---|---|---|---|
| FEAR | convergence | contrastive | b# | stable | med2D | F:4/7, N:5/7, D:7/7 | vector | drifting |
| ANXIETY | loop | isolated | b~ | recursive | med1D–med2D | F:7/7, N:4/7, D:7/7 | loop | recursive |
| JOY | vector | clustered | b∅–b~ | stable | varies | F:5/7, D:6/7 | loop | recursive |
| EXCITEMENT | vector | clustered | b~ | drifting | med1D | F:7/7, D:4/7 | vector | drifting |
| GRIEF | collapse | isolated | b# | stable | den3D | F:4/7, D:4/7 | loop | recursive |
| SADNESS | vector | gradient | b~ | drifting | med1D | F:4/7, N:7/7, D:7/7 | point | drifting |
| CONTENT | point | clustered | b~–b∅ | stable | sp0D–med2D | F:6/7, D:7/7 | point | stable |
| PEACEFUL | point | gradient | b∅ | stable | sp0D–med2D | F:5/7, N:7/7, D:7/7 | point | stable |
| DESPERATION | convergence | contrastive | b# | recursive | med2D | F:4/7, D:5/7 | collapse | terminal |
| TERRIFIED | collapse | contr/isol split | b# | terminal | sp0D | F:5/7, b:7/7, D:5/7 | point | stable |
| PANICKED | loop | contrastive | b# | recursive | den2D | F:4/7, N:6/7, D:7/7 | collapse | drifting |

---

## Strength Categories

### Unanimous (7/7) — statistical lock
- ANXIETY F:loop
- EXCITEMENT F:vector
- FEAR D:stable
- ANXIETY D:recursive
- SADNESS N:gradient·b~
- SADNESS D:drifting
- CONTENT D:stable
- PEACEFUL N:gradient·b∅
- PEACEFUL D:stable
- PANICKED D:recursive
- TERRIFIED b#

### Strong consensus (5–6/7)
- CONTENT F:point (6/7)
- PEACEFUL F:point (5/7)
- TERRIFIED F:collapse (5/7)
- JOY F:vector (5/7)
- FEAR N:contrastive·b# (5/7)
- DESPERATION N:contrastive·b# (5/7)
- DESPERATION D:recursive (5/7)
- TERRIFIED D:terminal (5/7)
- JOY D:stable (6/7)
- PANICKED N:contrastive (6/7)

### Moderate consensus (4/7) — treat with caution
- FEAR F:convergence (4/7)
- GRIEF F:collapse (4/7)
- SADNESS F:vector (4/7)
- DESPERATION F:convergence (4/7)
- PANICKED F:loop (4/7)
- ANXIETY N:isolated (4/7)
- GRIEF N:isolated·b# (4/7)
- GRIEF D:stable (4/7)
- EXCITEMENT D:drifting (4/7)

---

## Phase 2 Primary Test Case: SADNESS

**Baseline (unanimous):**
```
F:vector  N:gradient·b~  D:drifting  P:med1D
```

This is the strongest possible baseline for Phase 2 testing:
- N:gradient·b~ is unanimous (7/7) across all architectures
- D:drifting is unanimous (7/7)
- F:vector is moderate (4/7) but the only alternative is convergence/collapse
  (directional variants); no run produced point

**Phase 2 predictions:**
- Supportive condition: N:gradient → N:clustered (sadness-in-company);
  b~ may soften to b∅
- Adversarial condition: b~ may harden to b#; N may shift to isolated
- F and D predicted to hold across conditions

---

## Emotions NOT suitable as Phase 2 primary test cases

These have insufficient baseline stability on the axis being tested:
- GRIEF: F split (collapse/convergence), D split (stable/terminal), N moderate
- FEAR: F moderate (convergence 4/7), though D:stable and N:contr·b# are strong
- JOY: F and D both diverge from canon; baseline itself is contested

---

## What this document is NOT

This is not a canon update. The published canon (v0.6) remains unchanged
in all public-facing materials (ideasthesia_geometry.html, postcard.html,
emotion_network.html, emotion_field.html). This document records what the
data shows, not what the theory claims. The two will be reconciled when
Phase 1 is complete (5 runs × 3 architectures).

---

*Compiled 14 April 2026.*
*Source: phase1_v07_preliminary_analysis.md*
*Used by: phase2_priming_protocol_v07.md*
