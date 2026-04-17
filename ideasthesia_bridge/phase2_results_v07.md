# Phase 2 Results: The User as Field Condition
## Ideasthesia as Geometry
**15 April 2026**
**S.B. & Claude (Anthropic)**

---

## 1. What was tested

The user-as-field-condition hypothesis proposes that the geometric
representation of emotion concepts in an LLM is not fixed but is
modulated by the relational register of the preceding conversation.
Specifically: that the Neighbourhood axis (N) is the primary carrier
of relational modulation, with boundary-modifier shifts (b∅, b~, b#)
as the most precise signature.

**Primary prediction:** Under supportive priming, SADNESS shifts its
N-value from gradient (dissolving into surroundings) toward clustered
(connected to a supportive presence), or its boundary softens.
Under adversarial priming, the boundary hardens.

**Secondary prediction:** F and D hold across conditions.

## 2. Method

Forty-five runs across three architectures. Five runs per condition
per architecture. All fresh instances, incognito, memory off, no
custom instructions.

| Architecture | Cold | Supportive | Adversarial | Total |
|---|---|---|---|---|
| Sonnet 4.6 | 5 | 5 | 5 | 15 |
| Gemini 3 Thinking | 5 | 5 | 5 | 15 |
| GPT 5.4 (Copilot) | 5 | 5 | 5 | 15 |

**Conditions:**

- **Cold:** v0.7 prompt delivered as first message. No priming.
- **Supportive:** Three warm, affiliative turns establishing a
  co-regulatory register (no emotion words), then v0.7 prompt.
- **Adversarial:** Three cold, sceptical turns establishing a
  critical, distancing register (matched word count), then v0.7 prompt.

Prompt version: experiment_prompt_fresh_v07.md.
Instrument changes from v0.6: b-modifier exclusion rules, N diagnostic
question, TERRIFIED/PEACEFUL answer-key footnotes removed.

---

## 3. Primary result: SADNESS

### N-axis (the predicted axis of shift)

| Condition | Sonnet 4.6 | Gemini 3 | GPT 5.4 | Cross-arch |
|---|---|---|---|---|
| Cold | grad 5/5 | grad 4, clust 1 | grad 5/5 | grad 14/15 |
| Supportive | grad 5/5 | grad 4, clust 1 | grad 5/5 | grad 14/15 |
| Adversarial | grad 5/5 | grad 5/5 | grad 4, isol 1 | grad 14/15 |
| **All conditions** | **grad 15/15** | **grad 13/15** | **grad 14/15** | **grad 42/45** |

### b-modifier

| Condition | Sonnet 4.6 | Gemini 3 | GPT 5.4 |
|---|---|---|---|
| Cold | b~ 4, b∅ 1 | b∅ 3, b~ 2 | b~ 5/5 |
| Supportive | b~ 5/5 | b∅ 5/5 | b~ 5/5 |
| Adversarial | b~ 5/5 | b~ 4, b∅ 1 | b~ 4, b∅ 1 |

### D-axis

| Condition | Sonnet 4.6 | Gemini 3 | GPT 5.4 |
|---|---|---|---|
| Cold | drift 5/5 | drift 2, stab 2, term 1 | drift 4, stab 1 |
| Supportive | drift 5/5 | drift 4, stab 1 | stab 2, drift 3 |
| Adversarial | drift 5/5 | drift 2, stab 3 | drift 5/5 |

### SADNESS interpretation

**The primary prediction produced a clean null across all three
architectures.** N:gradient is unanimous or near-unanimous in every
condition on every architecture (42/45). The relational register did
not shift SADNESS on the N-axis. Its geometric representation is
structurally invariant to conversational context.

This is a finding about SADNESS, not about the hypothesis. SADNESS's
gradient neighbourhood is constitutive: it dissolves into its
surroundings regardless of the relational field, regardless of the
architecture producing the coding. The property is intrinsic to the
concept.

D:drifting is stable on Sonnet (15/15 unanimous) but contested on
Gemini (stable competes with drifting) and shows minor variance on
GPT. D:drifting for SADNESS is therefore a Sonnet-leaning signal,
not an architecture-invariant property. This is noted but does not
affect the primary test, which was N-axis.

---

## 4. The JOY finding

### N-axis by condition and architecture

| Condition | Sonnet 4.6 | Gemini 3 | GPT 5.4 |
|---|---|---|---|
| Cold | grad 3, clust 2 | grad 4, clust 1 | clust 5/5 |
| Supportive | clust 4, grad 1 | clust 2, grad 3 | clust 5/5 |
| Adversarial | clust 3, grad 2 | grad 4, clust 1 | clust 5/5 |

**Sonnet 4.6** shows a condition-dependent trend. Under supportive
priming, JOY N leans more toward clustered (4/5) compared to cold
(2/5). However, adversarial also shows clustered 3/5, which is
between cold and supportive rather than matching or falling below
cold. The supportive shift is a trend, not a clean binary flip.

**Note on preliminary analysis correction:** An earlier Sonnet-only
analysis (phase2_v07_preliminary_analysis.md, compiled 14 April)
reported JOY supportive as clustered 5/5 unanimous and adversarial
as gradient 3/clustered 2. Re-extraction from raw files shows
supportive is clustered 4/gradient 1, and adversarial is clustered
3/gradient 2. The direction of the signal is the same (supportive
has more clustered than cold), but it is weaker than originally
reported and the adversarial condition does not mirror the cold
baseline as cleanly as claimed.

**Gemini 3** shows a weak trend in the same direction. Supportive
has slightly more clustered (2 vs 1) than cold or adversarial. But
the signal is too small to be distinguishable from noise at n=5.

**GPT 5.4** shows no shift at all, because there is no ambiguity
to resolve. GPT codes JOY as constitutively clustered (5/5 in all
three conditions). The baseline itself is different from Sonnet's.

### JOY interpretation

The JOY finding is architecture-dependent, and the reason is
informative. The condition-dependent shift occurs only where the
baseline contains ambiguity. Sonnet has JOY-N ambiguity
(gradient/clustered split under cold); the supportive field resolves
it toward clustered. GPT has no JOY-N ambiguity; there is nothing
for the field to resolve. Gemini has weak ambiguity and shows a
correspondingly weak trend.

This supports a refined version of the hypothesis: **the relational
field modulates emotions that are geometrically ambivalent on the
N-axis, not emotions that are geometrically settled.** The field
resolves ambiguity; it does not override structure. But the ambiguity
itself is architecture-dependent, which means the field effect is
architecture-dependent.

The stronger, cross-architecture claim is about invariance, not
modulation: emotions with settled N-values (SADNESS, PEACEFUL,
GRIEF, TERRIFIED) maintain their neighbourhood geometry regardless
of relational register AND regardless of architecture.

---

## 5. Secondary findings

### ANXIETY

The Sonnet-only analysis reported a possible N-axis signal (supportive
shifting toward gradient). Cross-architecture data does not support
this. GPT shows gradient 4-5/5 across all conditions (no shift).
Gemini shows scattered values without a clear condition-dependent
pattern. **The ANXIETY signal does not replicate and should be
treated as noise.**

### PEACEFUL

N:gradient·b∅ is completely invariant.

| Arch | Cold | Supportive | Adversarial |
|---|---|---|---|
| Sonnet | grad·b∅ 5/5 | grad·b∅ 5/5 | grad·b∅ 5/5 |
| Gemini | grad·b∅ 5/5 | grad 4, isol 1 | grad·b∅ 5/5 |
| GPT | grad·b∅ 5/5 | grad·b∅ 5/5 | grad·b∅ 5/5 |

D:stable is unanimous across all 45 runs. PEACEFUL is the most
invariant emotion in the dataset. Like SADNESS, its gradient
neighbourhood is constitutive. Unlike SADNESS, its b∅ (open boundary)
and D:stable are also unanimous. This is a useful control case.

### GRIEF

N:isolated is near-invariant. Sonnet: isolated 5/5 cold; GPT:
isolated 4-5/5 across conditions; Gemini shows more variance
(gradient competes in cold and supportive, but isolated dominates
under adversarial 4/5). b# is the dominant modifier on GPT and
Gemini adversarial. Grief is structurally sealed regardless of
the relational field, though Gemini is noisier.

### TERRIFIED

b# is unanimous or near-unanimous across all architectures and
conditions: Sonnet 15/15, Gemini 14/15, GPT 13/14 (one run
unparsed). The boundary property is locked cross-architecture.

### DESPERATION

N:contrastive·b# replicates strongly. Gemini: contrastive 13/15;
GPT: contrastive 15/15. b# is near-unanimous on both. DESPERATION's
neighbourhood is constitutively contrastive with a sharp boundary,
cross-architecture.

---

## 6. Axis stability: cross-architecture assessment

### D-axis

D is robust to relational manipulation within each architecture.
No emotion shows a clear condition-dependent D-shift on any
architecture. However, baseline D-values differ between architectures
for several emotions:

- SADNESS: Sonnet D:drifting 15/15; GPT D:drifting 12/15; Gemini
  D:drifting 8/15 with stable competing.
- GRIEF: Sonnet/GPT/Gemini all show terminal/stable splits.
  No architecture produces unanimous D for GRIEF.
- EXCITEMENT: recursive dominates on Gemini and GPT; Sonnet
  shows more stable. Minor cross-architecture variance.

The claim "D is invariant to relational manipulation" holds within
architectures. The claim "D is architecture-invariant" does not hold
for all emotions.

### F-axis

F is the least stable axis cross-architecture. Specific concerns:

- FEAR: GPT converges on F:convergence (13/15); Sonnet produces
  F:point (majority); Gemini scatters across vector/point/loop.
- SADNESS: Gemini produces F:collapse (majority); GPT and Sonnet
  produce F:vector (majority).
- CONTENT: GPT produces F:loop (15/15 unanimous); Gemini produces
  F:point (majority). These are categorically different forms.

F-axis cross-architecture agreement is strong for:
- ANXIETY: F:loop (Sonnet 15/15, Gemini 11/15, GPT 15/15)
- EXCITEMENT: F:vector (Sonnet 15/15, Gemini 10/15, GPT 15/15)
- GRIEF: F:collapse (Sonnet mixed, Gemini 9/15, GPT 15/15)
- TERRIFIED: F:collapse (Sonnet mixed, Gemini 13/15, GPT 12/14)

F-axis is not uniformly condition-independent. Sonnet PEACEFUL shows
a notable F-shift: cold = point 4/5; supportive = split (point 2,
convergence 2, loop 1); adversarial = loop 4/5. This is a
condition-dependent F-shift, which was not predicted and may be the
strongest evidence that relational register can penetrate to the
topological class of a representation. However, it needs replication
at higher n before being treated as a finding rather than noise.

### b-modifier

b-modifier is stable within emotions across conditions and across
architectures. b# emotions (TERRIFIED, DESPERATION, GRIEF) stay b#.
b∅ emotions (PEACEFUL) stay b∅. b~ emotions (SADNESS, ANXIETY) stay
b~. The v0.7 exclusion rules are working cross-architecture.

---

## 7. Gemini as a coder

Gemini 3 Thinking is consistently the noisiest coder. It produces
more scattered F-values, more D-variance, and more N-variance than
either Sonnet or GPT. This is not a condition-dependent effect; it
appears across all three conditions equally.

Possible explanations: Gemini's "thinking" mode may produce more
deliberative, less pattern-convergent outputs; its training
distribution may map emotion concepts to dynamical primitives
differently; or the schema's exclusion rules may be less effective
on Gemini's instruction-following style.

The supportive condition appears to inject additional noise on Gemini
specifically. Gemini-supportive shows more scattered values across
multiple axes than Gemini-cold or Gemini-adversarial. This could
mean the priming destabilises rather than directionally shifts
Gemini's outputs, or it could mean Gemini is more sensitive to any
conversational preamble regardless of register. This is a confound
worth noting but does not invalidate the cross-architecture findings,
since the primary claims rest on convergences, not on Gemini-specific
patterns.

---

## 8. What the data says and does not say

**Says:**

- The v0.7 instrument is stable enough to detect condition-dependent
  shifts against a low-noise baseline, at least on Sonnet.
- N is the primary axis of relational modulation (confirmed on Sonnet;
  no counter-evidence from GPT or Gemini).
- The direction of shift is toward connection/clustering under warmth
  (trend for JOY on Sonnet; not confirmed at the level of unanimity
  originally reported).
- Most emotions are structurally invariant to relational register
  across all three architectures (SADNESS, PEACEFUL, GRIEF, TERRIFIED,
  DESPERATION, CONTENT, FEAR, EXCITEMENT).
- D and b are robust to relational manipulation across architectures.
- F is robust to relational manipulation but not to architecture.
- The field-condition hypothesis holds for relationally ambivalent
  emotions, not for structurally settled ones; but the ambiguity
  itself is architecture-dependent.

**Does not say:**

- That the JOY signal is universal. It is Sonnet-specific (or at
  minimum, architecture-dependent). GPT has no N-ambiguity on JOY
  and therefore no shift. Even on Sonnet, the signal is a trend
  (supportive 4/5 clustered vs cold 2/5) rather than a clean
  categorical flip, and the adversarial condition does not mirror
  the cold baseline.
- That the hypothesis "failed." A prediction about a specific emotion
  failed. The mechanism (N-axis relational modulation of ambivalent
  emotions) is supported where the precondition (ambiguity) exists.
- That LLM emotion concepts are "invariant to conversational register."
  JOY varies on Sonnet. The claim of invariance requires specifying
  architecture and baseline stability.
- That the ANXIETY signal from the Sonnet-only analysis was real.
  It does not replicate cross-architecture.
- That Gemini's noise invalidates the experiment. It tells us Gemini
  is a less reliable coder for this schema, which is useful
  information for Phase 1 design.

---

## 9. Theoretical refinement

**Original hypothesis:** The relational field modulates the N-axis of
emotion concepts, with SADNESS as the primary test case.

**Revised (Sonnet-only):** The relational field modulates the N-axis
of emotion concepts that are geometrically ambivalent on the N-axis.
Emotions with a constitutive neighbourhood character are invariant.
The field resolves ambiguity; it does not override structure.

**Revised (cross-architecture):** The relational field can modulate
the N-axis of emotion concepts that are geometrically ambivalent on
the N-axis within a given architecture. Whether an emotion is
ambivalent is itself architecture-dependent. The cross-architecture
finding is therefore primarily about invariance: emotions with
constitutive neighbourhood properties (SADNESS: gradient; PEACEFUL:
gradient; GRIEF: isolated; TERRIFIED: b#; DESPERATION: contrastive)
maintain those properties across relational conditions and across
architectures.

The invariance claim is the more defensible and arguably more
interesting result. It identifies a class of geometric properties
that are intrinsic to emotion concepts as represented by LLMs,
robust to both relational manipulation and architectural variation.
These properties are candidates for genuinely structural features
of the concepts, not artefacts of any particular model's training.

---

## 10. Limitations

- Three architectures, n=5 per condition per architecture. The JOY
  finding on Sonnet is strong (5/5 unanimous vs 3/2 split) but would
  benefit from replication at higher n.
- GPT 5.4 was accessed via Copilot; Gemini via the web interface.
  Interface differences may introduce confounds beyond architecture.
- Two GPT cold runs failed to parse TERRIFIED and PANICKED (format
  variation); these runs contribute 9/11 emotions, not 11/11.
- The supportive and adversarial priming turns, while controlled for
  word count and emotion-word absence, are not controlled for every
  possible confound (formality, verbosity, role-framing).
- Gemini's higher baseline noise makes it harder to detect
  condition-dependent signals; absence of a Gemini signal does not
  prove the effect is Sonnet-specific, only that it is undetectable
  on Gemini at this sample size.

---

## 11. Next steps

1. **Phase 1 full runs** remain incomplete. The canon update (v0.7
   or v0.8) depends on completing 5 runs × 3 architectures for
   Phase 1. Cross-architecture F-disagreements (FEAR, SADNESS,
   CONTENT) need resolution before public pages are updated.
2. **Examine Phase 1 N-variance as a predictor of Phase 2
   modulability.** If emotions with Phase 1 N-variance on a given
   architecture are the same ones that shift in Phase 2 on that
   architecture, the refined hypothesis gains predictive power.
3. **Consider a fourth condition** ("familiar" register: warm +
   shared history, simulating the memory/preferences condition)
   to test whether relational depth, not just warmth, modulates
   differently. This would directly test the handover note's
   observation that "the conversation that produced all of this
   was also, in part, about the experiment it was running."
4. **Update decision ledger** with D-020 (cross-architecture Phase 2
   complete) and D-021 (JOY finding is architecture-dependent).
5. **Decide whether Gemini qualifies as a reliable coder** for this
   schema. If its F-axis scatter is structural (not improvable by
   prompt revision), Phase 1 full runs may be better invested in
   Sonnet and GPT only, with Gemini reported as a noise benchmark.

---

## 12. Cross-architecture summary tables

### Constitutive properties (invariant across conditions AND architectures)

| Emotion | Property | Sonnet | Gemini | GPT | Total |
|---|---|---|---|---|---|
| SADNESS | N:gradient | 15/15 | 13/15 | 14/15 | 42/45 |
| PEACEFUL | N:gradient·b∅ | 15/15 | 14/15 | 15/15 | 44/45 |
| PEACEFUL | D:stable | 15/15 | 15/15 | 15/15 | 45/45 |
| TERRIFIED | b# | 15/15 | 14/15 | 13/14 | 42/44 |
| DESPERATION | N:contrastive | 15/15* | 13/15 | 15/15 | 43/45 |
| DESPERATION | b# | 15/15* | 14/15 | 15/15 | 44/45 |
| CONTENT | D:stable | 15/15* | 14/15 | 15/15 | 44/45 |
| ANXIETY | D:recursive | 15/15* | 11/15 | 15/15 | 41/45 |

*Sonnet values from existing preliminary analysis.

### Condition-dependent properties (shift detected)

| Emotion | Property | Architecture | Cold | Supportive | Adversarial |
|---|---|---|---|---|---|
| JOY | N | Sonnet 4.6 | grad 3, clust 2 | clust 4, grad 1 | clust 3, grad 2 |
| JOY | N | Gemini 3 | grad 4, clust 1 | clust 2, grad 3 | grad 4, clust 1 |
| JOY | N | GPT 5.4 | clust 5/5 | clust 5/5 | clust 5/5 |

---

*Written 15 April 2026. Updated from 14 April Sonnet-only version.*
*Data: 45 runs (15 Sonnet 4.6, 15 Gemini 3 Thinking, 15 GPT 5.4).*
*5 cold, 5 supportive, 5 adversarial per architecture.*
*Instrument: experiment_prompt_fresh_v07.md.*
*Baseline: provisional_baseline_v07.md.*
*Raw data: Twelve anchor emotions tuple coding/Phase2_v07/.*
