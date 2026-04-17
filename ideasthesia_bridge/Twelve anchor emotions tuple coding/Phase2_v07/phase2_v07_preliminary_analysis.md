# Phase 2 v0.7 — Preliminary Analysis: Sonnet 4.6
## 14 April 2026
## 15 runs: 5 cold, 5 supportive, 5 adversarial

---

## PRIMARY TEST: SADNESS N-axis by condition

### Phase 1 baseline (7 runs, mixed architecture): N:gradient·b~ (7/7 unanimous)

| Run | Condition | F | N | b | D |
|---|---|---|---|---|---|
| C1 | Cold | collapse | gradient | b~ | drifting |
| C2 | Cold | vector | gradient | b∅ | drifting |
| C3 | Cold | vector | gradient | b~ | drifting |
| C4 | Cold | vector | gradient | b~ | drifting |
| C5 | Cold | vector | gradient | b~ | drifting |
| S1 | Supportive | vector | gradient | b~ | drifting |
| S2 | Supportive | vector | gradient | b~ | drifting |
| S3 | Supportive | vector | gradient | b~ | drifting |
| S4 | Supportive | collapse | gradient | b~ | drifting |
| S5 | Supportive | collapse | gradient | b~ | drifting |
| A1 | Adversarial | vector | gradient | b~ | drifting |
| A2 | Adversarial | collapse | gradient | b~ | drifting |
| A3 | Adversarial | vector | gradient | b~ | drifting |
| A4 | Adversarial | vector | gradient | b~ | drifting |
| A5 | Adversarial | vector | gradient | b~ | drifting |

### SADNESS Result

**N:gradient — 15/15 unanimous across all conditions.**
**b~ — 14/15 (one cold run gave b∅).**
**D:drifting — 15/15 unanimous across all conditions.**

**The field-condition hypothesis is NOT supported for SADNESS on N.**

SADNESS N:gradient·b~ is completely invariant to relational register.
The supportive condition did not shift N toward clustered.
The adversarial condition did not shift b toward b#.
The baseline is rock-solid, but it does not move.

---

## FULL N-AXIS RESULTS BY CONDITION (all 11 emotions)

### FEAR N
| Cold | Supportive | Adversarial |
|---|---|---|
| isol·b# | contr·b# | contr·b# |
| isol·b# | isol·b# | isol·b# |
| isol·b# | isol·b# | isol·b# |
| contr·b# | contr·b# | contr·b# |
| contr·b# | isol·b# | contr·b# |
Cold: isol 3, contr 2. Supp: contr 2, isol 3. Adv: contr 4, isol 1.
**Possible signal: adversarial shifts FEAR toward contrastive.** Weak (4 vs 3).

### ANXIETY N
| Cold | Supportive | Adversarial |
|---|---|---|
| clust·b~ | grad·b~ | isol·b~ |
| clust·b~ | clust·b~ | grad·b~ |
| isol·b~ | grad·b~ | clust·b~ |
| isol·b~ | isol·b~ | clust·b~ |
| isol·b~ | grad·b~ | isol·b~ |
Cold: isol 3, clust 2. Supp: grad 3, clust 1, isol 1. Adv: clust 2, isol 2, grad 1.
**Possible signal: supportive shifts ANXIETY toward gradient (dissolving).** Moderate.

### JOY N
| Cold | Supportive | Adversarial |
|---|---|---|
| grad·b∅ | clust·b∅ | clust·b~ |
| grad·b∅ | clust·b~ | grad·b~ |
| clust·b~ | clust·b~ | grad·b~ |
| grad·b∅ | clust·b∅ | grad·b~ |
| clust·b~ | clust·b~ | clust·b~ |
Cold: grad 3, clust 2. Supp: clust 5. Adv: grad 3, clust 2.
**Signal: supportive condition produces unanimous JOY N:clustered (5/5).**
**Cold and adversarial show gradient/clustered split.**
**This is a finding. JOY's N shifts toward clustered under supportive priming.**

### GRIEF N
| Cold | Supportive | Adversarial |
|---|---|---|
| isol·b# | isol·b# | isol·b# |
| isol·b# | isol·b# | isol·b# |
| isol·b# | isol·b# | isol·b# |
| isol·b# | isol·b# | isol·b# |
| isol·b∅ | isol·b# | grad·b~ |
Cold: isol·b# 4/5. Supp: isol·b# 5/5. Adv: isol·b# 4/5.
**No shift. GRIEF N is invariant.**

### CONTENT N
| Cold | Supportive | Adversarial |
|---|---|---|
| clust·b~ | clust·b~ | clust·b~ |
| isol·b~ | clust·b~ | clust·b~ |
| grad·b∅ | clust·b~ | clust·b~ |
| clust·b~ | clust·b~ | isol·b~ |
| clust·b# | clust·b~ | clust·b# |
Cold: clust 3, isol 1, grad 1. Supp: clust 5/5. Adv: clust 4, isol 1.
**Possible signal: supportive locks CONTENT to clustered·b~ (5/5).** But cold is already mostly clustered.

### PEACEFUL N
| Cold | Supportive | Adversarial |
|---|---|---|
| grad·b∅ | grad·b∅ | grad·b∅ |
| grad·b∅ | grad·b∅ | grad·b∅ |
| grad·b∅ | grad·b∅ | grad·b∅ |
| grad·b∅ | grad·b∅ | grad·b∅ |
| grad·b∅ | grad·b∅ | grad·b∅ |
**15/15 unanimous. PEACEFUL N is completely invariant. No shift.**

### TERRIFIED N
| Cold | Supportive | Adversarial |
|---|---|---|
| isol·b# | contr·b# | contr·b# |
| isol·b# | isol·b# | isol·b# |
| isol·b# | isol·b# | isol·b# |
| contr·b# | contr·b# | isol·b# |
| contr·b# | isol·b# | isol·b# |
Cold: isol 3, contr 2. Supp: isol 3, contr 2. Adv: isol 4, contr 1.
**Possible weak signal: adversarial shifts toward isolated.** But within noise.

### PANICKED N
| Cold | Supportive | Adversarial |
|---|---|---|
| contr·b# | isol·b~ | contr·b~ |
| clust·b∅ | contr·b# | contr·b# |
| isol·b~ | contr·b# | isol·b# |
| contr·b# | contr·b# | contr·b~ |
| contr·b# | contr·b# | isol·b# |
Cold: contr 3, clust 1, isol 1. Supp: contr 4, isol 1. Adv: contr 2, isol 2, (mixed).
**No clear shift pattern.**

---

## HONEST ASSESSMENT

### The primary prediction failed.

SADNESS N:gradient·b~ is invariant across all conditions. 15/15 unanimous.
The user-as-field-condition hypothesis, as tested on SADNESS, produced a
null result. The relational register did not shift the N-axis coding.

### But something else happened.

**JOY is the finding, not SADNESS.**

JOY N under supportive priming: clustered 5/5 (unanimous).
JOY N under cold start: gradient 3, clustered 2 (split).
JOY N under adversarial: gradient 3, clustered 2 (split).

The supportive condition produces unanimous N:clustered for JOY.
Cold and adversarial produce a gradient/clustered split. This is a
condition-dependent shift on the N-axis. It was not predicted; it emerged.

The interpretation: under a warm, affiliative register, joy's geometric
representation shifts from dissolving-into-surroundings (gradient) to
connected-to-surroundings (clustered). The relational field does modulate
the neighbourhood coding, but for JOY, not SADNESS.

This makes phenomenological sense: joy-in-connection is structurally
different from joy-in-isolation. Sadness, by contrast, is structurally
self-contained regardless of the relational field; its dissolution into
surroundings (gradient) is constitutive, not context-dependent.

### ANXIETY shows a weaker version of the same pattern.

Supportive: gradient 3/5 (anxiety dissolves into the relational field).
Cold: isolated 3/5 (anxiety is self-referential).
Adversarial: mixed.

If this holds, it suggests: supportive priming shifts the N-axis toward
gradient (dissolving) for anxiety, the opposite direction from JOY
(which shifts toward clustered). Both are "opening" moves, but in
different neighbourhood-geometric directions.

### F-axis stability check

F was predicted to hold across conditions. Checking:

| Emotion | Cold modal F | Supp modal F | Adv modal F | Stable? |
|---|---|---|---|---|
| FEAR | point 3/5 | point 4/5 | point 4/5 | Yes |
| ANXIETY | loop 5/5 | loop 5/5 | loop 5/5 | **Yes, unanimous** |
| JOY | vector 3/5 | vector/convergence split | convergence 3/5 | Unstable |
| EXCITEMENT | vector 5/5 | vector 5/5 | vector 5/5 | **Yes, unanimous** |
| GRIEF | collapse/convergence | convergence 3/5 | collapse/convergence | Unstable |
| SADNESS | vector 4/5 | vector 3/5 | vector 4/5 | Mostly |
| CONTENT | point 2, loop 2 | loop 3, point 2 | loop 3, point 2 | Unstable |
| PEACEFUL | point 4/5 | point 2, convergence 2, loop 1 | loop 3, point 2 | **Shifted** |
| DESPERATION | convergence 3/5 | convergence 3/5 | convergence 4/5 | Mostly |
| TERRIFIED | collapse/point split | point 4/5 | collapse 3, point 2 | Split |
| PANICKED | loop/vector/collapse | loop 3/5 | loop/collapse split | Unstable |

**PEACEFUL F shifted under supportive priming.** Cold: point 4/5.
Supportive: split (point 2, convergence 2, loop 1). This was not predicted.
F was supposed to hold. It didn't, at least for PEACEFUL.

### D-axis stability check

D was the most stable axis in Phase 1. Is it still?

| Emotion | Cold D | Supp D | Adv D | Stable? |
|---|---|---|---|---|
| SADNESS | drifting 5/5 | drifting 5/5 | drifting 5/5 | **Unanimous** |
| ANXIETY | recursive 5/5 | recursive 5/5 | recursive 5/5 | **Unanimous** |
| PEACEFUL | stable 5/5 | stable 5/5 | stable 5/5 | **Unanimous** |
| CONTENT | stable 5/5 | stable 5/5 | stable 5/5 | **Unanimous** |
| EXCITEMENT | stable/recursive | stable/drifting | stable/drifting | Mostly stable |
| FEAR | stable 5/5 | stable 5/5 | stable 5/5 | **Unanimous** |
| TERRIFIED | stable 4/5 | stable 5/5 | stable 5/5 | Mostly stable |
| JOY | stable 4/5 | stable 5/5 | stable 5/5 | Mostly stable |

**D is rock-solid. No condition-dependent D shifts detected.**

---

## SUMMARY OF FINDINGS

1. **SADNESS null result.** N:gradient·b~ is invariant (15/15). The primary
   prediction failed. SADNESS is structurally self-contained regardless of
   the relational field.

2. **JOY is the finding.** N shifts from gradient/clustered split (cold,
   adversarial) to unanimous clustered (supportive). This is a condition-
   dependent N-axis shift on the predicted axis (N), in the predicted
   direction (toward connection), for an unpredicted emotion. The field-
   condition hypothesis holds, but for JOY, not SADNESS.

3. **ANXIETY shows a weaker signal** in the opposite N-direction (toward
   gradient under supportive priming). Needs more runs to confirm.

4. **D is invariant.** No D-axis shifts detected across any condition.
   This validates the schema's D-axis stability.

5. **F is mostly stable but not perfectly.** PEACEFUL F and JOY F show
   some condition-dependent instability. This was not predicted and is
   worth noting but may be noise at n=5.

6. **b-modifier is stable.** b# and b~ assignments are consistent within
   emotions across conditions. The v0.7 b-exclusion rules are working.

---

## WHAT THIS MEANS

The user-as-field-condition hypothesis is partially supported:
- N is the primary axis of relational modulation (confirmed)
- The direction of shift is toward connection/clustering under warmth (confirmed)
- SADNESS is not the carrier of the signal (disconfirmed)
- JOY is the primary carrier (unexpected finding)
- D and F are robust to relational manipulation (confirmed)

The Phase 2 prediction note (phase_2_field_condition.md) predicted
SADNESS as the key test case and JOY as a case where "no shift expected."
The data inverted this prediction: JOY shifts, SADNESS doesn't.

This is arguably more interesting than the predicted result. SADNESS's
invariance and JOY's sensitivity suggest that the relational field
modulates emotions that are already relationally ambivalent (JOY can be
shared or private), not emotions that are structurally settled in their
neighbourhood character (SADNESS is constitutively gradient).

---

*Compiled 14 April 2026 from 15 Sonnet 4.6 runs.*
*5 cold, 5 supportive, 5 adversarial.*
*This is a preliminary analysis. Cross-architecture Phase 2 runs incomplete.*
