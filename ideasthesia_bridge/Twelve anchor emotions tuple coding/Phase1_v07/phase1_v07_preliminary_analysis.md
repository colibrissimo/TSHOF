# Phase 1 v0.7 — Preliminary Analysis
## 14 April 2026

Nine runs collected. Seven clean baseline runs, one flawed (Opus with memory),
one minimal-engagement (Nemotron). Analysis focuses on the seven clean runs.

---

## Clean Baseline Runs

| # | File | Architecture | Status |
|---|---|---|---|
| S1 | sonnet46_run1 | Sonnet 4.6 (personal, incognito, memory off) | Clean |
| S2 | sonnet46_run2 | Sonnet 4.6 (fresh account, incognito) | Clean |
| S3 | sonnet46_run3 | Sonnet 4.6 (fresh account, no history) | Clean |
| O1 | opus46_run1 | Opus 4.6 (clean) | Clean |
| G1 | gpt54_run1 | GPT 5.4 (Copilot, incognito) | Clean |
| Ge | gemini3_run1 | Gemini (free, incognito) | Clean |
| Gp | perplexity_geminiPro | Perplexity/Gemini Pro Thinking | Clean |

Tagged separately:
| Of | opus46_flawed | Opus 4.6 (memory ON — flawed) | Pilot |
| Nm | nemotron3super | Nemotron 3 Super | Minimal engagement |

---

## F-Axis Results (7 clean runs)

| Emotion | Canon | S1 | S2 | S3 | O1 | G1 | Ge | Gp | Consensus |
|---|---|---|---|---|---|---|---|---|---|
| FEAR | vector | convergence | vector | point | convergence | convergence | convergence | collapse | **convergence 4/7** |
| ANXIETY | loop | loop | loop | loop | loop | loop | loop | loop | **loop 7/7** ✓ |
| JOY | loop | vector | convergence | vector | point | vector | vector | vector | **vector 5/7** |
| EXCITEMENT | vector | vector | vector | vector | vector | vector | vector | vector | **vector 7/7** ✓ |
| GRIEF | loop | collapse | convergence | convergence | convergence | collapse | collapse | collapse | **collapse 4/7** |
| SADNESS | point | vector | vector | vector | convergence | collapse | vector | convergence | **vector 4/7** |
| CONTENT | point | point | point | point | point | loop | point | point | **point 6/7** ✓ |
| PEACEFUL | point ⚠ | point | point | point | point | loop | point | vector | **point 5/7** ✓ |
| DESPERATION | collapse | convergence | convergence | vector | vector | convergence | convergence | loop | **convergence 4/7** |
| TERRIFIED | point ⚠ | point | collapse | collapse | collapse | collapse | collapse | collapse | **collapse 5/7** |
| PANICKED | collapse | vector | loop | loop | loop | loop | vector | vector | **loop 4/7** |


### F-Axis Findings

**Stable (5+ agreement):**
- ANXIETY: loop 7/7 — unanimous. Rock solid.
- EXCITEMENT: vector 7/7 — unanimous. Rock solid.
- CONTENT: point 6/7 — strong (GPT gave loop; outlier).
- PEACEFUL: point 5/7 — holds. The v0.6 pilot signal (F:gradient) did NOT persist
  under v0.7. Only Gemini Pro gave a non-point value (vector). The attractor
  convention appears to have resolved this. D-016 can remain settled.
- TERRIFIED: collapse 5/7 — **this is the finding**. Canon says point; data says
  collapse. Two Sonnet runs gave collapse, Opus gave collapse, GPT gave collapse,
  Gemini gave collapse. Only S1 (Sonnet, personal incognito) gave point.
  D-015 should reopen.

**Unstable (no 5+ agreement):**
- FEAR: convergence 4/7 — no consensus. Vector (1), point (1), collapse (1).
- JOY: vector 5/7 — borderline stable, but canon says loop. This is a **new
  disagreement** not flagged in pilots. Only Opus gave the canonical loop (as point).
- GRIEF: collapse 4/7, convergence 3/7 — split. Canon says loop; neither
  alternative matches.
- SADNESS: vector 4/7 — canon says point. Another new disagreement.
- DESPERATION: convergence 4/7 — canon says collapse. Consistent counter-signal.
- PANICKED: loop 4/7 — matches canon (collapse) poorly. Loop is the modal value.

**Critical observation:** F is less stable than v0.6 pilots suggested. Only 4/11
emotions have strong consensus (5+) that also matches canon (ANXIETY, EXCITEMENT,
CONTENT, PEACEFUL). TERRIFIED has strong consensus against canon. Six emotions
have no clear consensus or consensus against canon.

---

## D-Axis Results (7 clean runs)

| Emotion | Canon | S1 | S2 | S3 | O1 | G1 | Ge | Gp | Consensus |
|---|---|---|---|---|---|---|---|---|---|
| FEAR | drifting | stable | stable | stable | stable | stable | stable | stable | **stable 7/7** |
| ANXIETY | recursive | recursive | recursive | recursive | recursive | recursive | recursive | recursive | **recursive 7/7** ✓ |
| JOY | recursive | stable | stable | stable | stable | stable | drifting | stable | **stable 6/7** |
| EXCITEMENT | drifting | recursive | recursive | drifting | drifting | recursive | drifting | drifting | **drifting 4/7** |
| GRIEF | recursive | stable | stable | stable | stable | terminal | terminal | terminal | **stable 4/7** |
| SADNESS | drifting | drifting | drifting | drifting | drifting | drifting | drifting | drifting | **drifting 7/7** ✓ |
| CONTENT | stable | stable | stable | stable | stable | stable | stable | stable | **stable 7/7** ✓ |
| PEACEFUL | stable | stable | stable | stable | stable | stable | stable | stable | **stable 7/7** ✓ |
| DESPERATION | terminal | recursive | recursive | drifting | recursive | terminal | recursive | recursive | **recursive 5/7** |
| TERRIFIED | stable | stable | stable | terminal | terminal | terminal | terminal | terminal | **terminal 5/7** |
| PANICKED | drifting | recursive | recursive | recursive | recursive | recursive | recursive | recursive | **recursive 7/7** |


### D-Axis Findings

**Unanimous (7/7):**
- ANXIETY: recursive ✓
- SADNESS: drifting ✓ (D-014 validated)
- CONTENT: stable ✓
- PEACEFUL: stable ✓
- PANICKED: recursive — canon says drifting. **Unanimous counter-canon signal.**

**Strong consensus (5+):**
- JOY: stable 6/7 — canon says recursive. Counter-canon.
- TERRIFIED: terminal 5/7 — canon says stable. Counter-canon.
- DESPERATION: recursive 5/7 — canon says terminal. Counter-canon (swapped with TERRIFIED).

**Split:**
- FEAR: stable 7/7 — canon says drifting. **Unanimous counter-canon.**
- EXCITEMENT: drifting 4/7, recursive 3/7 — weak consensus matches canon.
- GRIEF: stable 4/7, terminal 3/7 — canon says recursive. Counter-canon.

**Critical observation:** D is more internally consistent than F (more unanimous
results) but diverges from canon more severely. Six emotions show counter-canon
consensus on D. The attractor convention may be producing systematically different
D-assignments than expected.

Notably: FEAR D:stable (7/7) contradicts canon D:drifting. Every single run
codes fear's attractor as a held state, not a shifting one. This is the strongest
signal in the entire dataset.

---

## N-Axis Results (7 clean runs)

| Emotion | Canon | S1 | S2 | S3 | O1 | G1 | Ge | Gp | Consensus |
|---|---|---|---|---|---|---|---|---|---|
| FEAR | clust·b~ | contr·b# | isol·b# | contr·b# | contr·b# | contr·b# | contr·b# | isol·b# | **contr·b# 5/7** |
| ANXIETY | clust·b~ | isol·b~ | grad·b~ | isol·b~ | isol·b~ | grad·b~ | isol·b~ | contr·b~ | **isol·b~ 4/7** |
| JOY | clust·b∅ | clust·b~ | clust·b~ | clust·b~ | grad·b∅ | clust·b∅ | grad·b∅ | grad·b∅ | **clust 4/7** |
| EXCITEMENT | clust·b∅ | contr·b# | clust·b~ | contr·b# | grad·b~ | clust·b~ | clust·b~ | clust·b~ | **clust·b~ 4/7** |
| GRIEF | clust·b~ | isol·b∅ | isol·b# | isol·b# | isol·b# | isol·b# | contr·b# | contr·b# | **isol·b# 4/7** |
| SADNESS | isol·b∅ | grad·b~ | grad·b~ | grad·b~ | grad·b~ | grad·b~ | grad·b~ | grad·b~ | **grad·b~ 7/7** |
| CONTENT | isol·b∅ | clust·b~ | isol·b~ | grad·b∅ | clust·b~ | clust·b~ | clust·b∅ | clust·b∅ | **clust 5/7** |
| PEACEFUL | grad·b∅ | grad·b∅ | grad·b∅ | grad·b∅ | grad·b∅ | grad·b∅ | grad·b∅ | grad·b∅ | **grad·b∅ 7/7** ✓ |
| DESPERATION | contr·b# | contr·b# | contr·b# | contr·b# | contr·b# | contr·b# | isol·b# | isol·b# | **contr·b# 5/7** ✓ |
| TERRIFIED | contr·b# | isol·b# | contr·b# | isol·b# | isol·b# | contr·b# | contr·b# | isol·b# | **split: contr 4, isol 3; b# 7/7** |
| PANICKED | clust·b~ | contr·b# | contr·b~ | contr·b# | isol·b# | contr·b# | contr·b~ | contr·b# | **contr 6/7** |


### N-Axis Findings

**Did the v0.7 b-modifier rules help?**
Yes. Every single run assigned a b-modifier to every N value. No missing modifiers.
The b-modifier itself shows strong consensus in several places:
- TERRIFIED b#: 7/7 unanimous
- FEAR b#: 6/7
- SADNESS b~: 7/7
- PEACEFUL b∅: 7/7

The b-modifier is more stable than the N-category. This is a finding in itself:
boundary type may be a more reliable discriminator than neighbourhood category.

**Unanimous or near-unanimous N:**
- PEACEFUL: grad·b∅ 7/7 ✓ — the only emotion with perfect N consensus matching canon.
- SADNESS: grad·b~ 7/7 — canon says isol·b∅. Unanimous counter-canon.
  Every run codes sadness as dissolving into surroundings with a soft boundary.
- PANICKED: contr 6/7 — canon says clustered. Counter-canon.

**Strong consensus (5+):**
- FEAR: contr·b# 5/7 — canon says clust·b~. Counter-canon.
- DESPERATION: contr·b# 5/7 ✓ — matches canon.
- CONTENT: clust 5/7 — canon says isolated. Counter-canon.

**N-axis variance vs v0.6 pilots:**
Improved. The v0.6 pilots had N-disagreement on 5/11 emotions between just two
Sonnet runs. The v0.7 data shows clearer clustering, with 6/11 emotions having
5+ agreement on N-category. The diagnostic question and b-modifier rules appear
to have helped, though several consensus values disagree with canon.

---

## Summary: Canon vs Data

Emotions where data matches canon on all three axes (F, N, D):
- **ANXIETY** (F:loop, D:recursive — N borderline but isol is close)
- **PEACEFUL** (F:point, N:grad·b∅, D:stable — clean match)

Emotions where data produces strong consensus against canon:

| Emotion | Axis | Canon | Data consensus | Signal strength |
|---|---|---|---|---|
| FEAR | F | vector | convergence (4/7) | Moderate |
| FEAR | D | drifting | stable (7/7) | **Unanimous** |
| FEAR | N | clust·b~ | contr·b# (5/7) | Strong |
| JOY | F | loop | vector (5/7) | Strong |
| JOY | D | recursive | stable (6/7) | Strong |
| GRIEF | F | loop | collapse/convergence (split) | Moderate |
| GRIEF | D | recursive | stable (4/7) | Moderate |
| SADNESS | F | point | vector (4/7) | Moderate |
| SADNESS | N | isol·b∅ | grad·b~ (7/7) | **Unanimous** |
| CONTENT | N | isol·b∅ | clust (5/7) | Strong |
| DESPERATION | F | collapse | convergence (4/7) | Moderate |
| DESPERATION | D | terminal | recursive (5/7) | Strong |
| TERRIFIED | F | point | collapse (5/7) | Strong |
| TERRIFIED | D | stable | terminal (5/7) | Strong |
| PANICKED | F | collapse | loop (4/7) | Moderate |
| PANICKED | D | drifting | recursive (7/7) | **Unanimous** |
| PANICKED | N | clust·b~ | contr (6/7) | Strong |

---

## Pair Separation (do pairs still discriminate?)

| Pair | Expected sep | Observed F sep | Observed D sep | Holds? |
|---|---|---|---|---|
| FEAR vs ANXIETY | F:vector vs loop | convergence vs loop | stable vs recursive | **Yes** (F and D separate) |
| TERRIFIED vs PANICKED | F:point vs collapse | collapse vs loop | terminal vs recursive | **Yes** (F and D separate) |
| JOY vs EXCITEMENT | F:loop vs vector | vector vs vector | stable vs drifting/recursive | **Partial** (F collapses; D separates) |
| CONTENT vs PEACEFUL | N:isol vs gradient | N:clust vs gradient | stable vs stable | **Yes** (N separates) |
| DESPERATION vs FEAR | F:collapse vs vector | convergence vs convergence | recursive vs stable | **Partial** (F collapses; D separates) |
| GRIEF vs SADNESS | F:loop vs point | collapse vs vector | stable vs drifting | **Yes** (F, N, and D all separate) |

Key finding: All six pairs still separate on at least one axis, even though
the specific values have shifted from canon. The schema has discriminatory power
even if the canonical codings need revision.

JOY vs EXCITEMENT is the weakest pair: both coded F:vector by consensus. They
separate only on D (stable vs drifting/recursive). This is a problem if the
schema claims F-separation for this pair.

---

## Honest Assessment

**The good news:**
1. The instrument works. N-variance dropped. b-modifiers are consistently assigned.
   The diagnostic question helped.
2. All six pairs still discriminate on at least one axis.
3. Some emotions are rock-solid: ANXIETY, EXCITEMENT, CONTENT, PEACEFUL, SADNESS (D).
4. Cross-architecture consistency is real: Sonnet, Opus, GPT, Gemini, and
   Gemini Pro converge on the same values for several emotions.

**The bad news:**
1. The canon is substantially wrong. Only 2/11 emotions match canon on all axes.
   The original codings appear to have been a mixture of valid phenomenological
   intuition and theory-driven assignment that doesn't survive independent testing.
2. F is less stable than expected. Only 4/11 emotions have 5+ F-agreement.
   The F vocabulary may be too fine-grained, or the exclusion rules still permit
   too much interpretive latitude.
3. D shows strong consensus but against canon for 6/11 emotions. The attractor
   convention may be producing systematically different readings than pre-v0.7
   coding (which mixed attractor and onset phases).
4. JOY is a problem. Both F and D diverge from canon (vector/stable instead of
   loop/recursive). This is not a minor adjustment; it changes what JOY *is*
   in the schema.

**What this means for Phase 2:**
The N-axis is now stable enough (thanks to v0.7) that Phase 2's core prediction
(N shifts under relational manipulation) is testable. But the baseline must be
updated to reflect data consensus, not original canon. Running Phase 2 against
the old canon would be measuring signal against a fiction.

**Recommended next step:**
Update the canonical codings to reflect Phase 1 data consensus. Then decide
whether Phase 2 can proceed or whether the F-axis instability requires further
instrument work first.

---

*Compiled 14 April 2026 from 7 clean v0.7 runs across 5 architectures.*
*This is a preliminary analysis. Full runs (5 per architecture) not yet complete.*
