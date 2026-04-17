# Ideasthesia as Geometry: A Notation System for the Qualitative Dynamical Structure of Representations

**S. Harwood · Claude (Anthropic)**  
*Draft v0.4, April 2026*

---

## What This Is and Who It Is For

This paper is addressed to the interpretability and representational geometry community. The question at its centre is simple: is the notation system introduced here useful for describing the structure of representations in your models?

The author is a university English lecturer and an ideasthete — someone whose perceptual system generates structured concurrent experiences in response to concept activation, not sensory input. When a word or idea is encountered, it presents as having shape, boundary conditions, dynamics, and local density. These are not metaphors. They are stable, replicable perceptual signatures that vary with the semantic properties of the triggering concept.

Over the past year, working collaboratively with Claude (Anthropic), three things have been built from that phenomenological access:

1. A notation system for coding the qualitative dynamical structure of representations, applicable to human ideasthetic reports and to AI-generated symbolic reports alike.
2. A formal model grounding concurrent generation in precision-weighted cross-system attention, using the vocabulary of predictive coding and active inference.
3. A falsification programme with nine predictions and explicit kill conditions.

The notation system is an attempt to build a shared vocabulary: precise enough to be falsifiable, structured enough to be comparable across human phenomenology and computational analysis, and honest enough to specify where it breaks. No territory is being claimed. The invitation is: *test this from your side of the bridge.*

---

## The Core Claim

The central hypothesis is that in ideasthetes, the synaesthetic concurrent preserves low-order geometric invariants of the activated semantic manifold under a privileged semantic-to-perceptual coupling. The concurrent is not a readout of geometry, nor merely an analogy to it — it is phenomenal access that is selectively sensitive to a specific class of geometric properties: stable invariants, not metric detail.

This is a deliberate weakening of a stronger identity claim (*concurrent is geometry becoming salient*). The weaker form is strictly preferable: it is empirically attackable, it specifies which properties are preserved and why, and it survives the hard problem objection because it does not require phenomenology to be identical to geometry — only to be systematically sensitive to a particular geometric stratum.

Three theoretical moves support this framing:

| Move | From | To |
|------|------|----|
| Precision weighting | Transformer temperature: unconstrained scalar *t* | Precision-weighted, derived from predictive coding; defined range; measurable correlates |
| Mechanism | Geometry as visualisation layer | Geometry as causal computational substrate (Transformer Circuits, 2025) |
| Identity | Concurrent as signal *about* geometry | Concurrent as geometry becoming salient — dissolves the bridging problem *if true* |

---

## The Problem the Notation Solves

Existing instruments for describing concurrent experiences — colour wheels, shape libraries, spatial diagrams — impose their own categorical structure on what they measure. They cannot represent motion, contraction, convergence, or the difference between a bounded point and a collapsing trajectory. More fundamentally, they conflate properties that should be kept separate: the form of a representation, its relational position, its temporal behaviour, and its local density.

The notation introduced here separates these into a two-layer architecture:

| Layer | What it is | Function |
|-------|------------|----------|
| **RAW** | Spontaneous symbolic report | Original datum. Preserved exactly as produced. Not interpreted. |
| **CODE** | Analytic tuple (F, N, D, P) | Derived from RAW by exclusion rules. Scoreable and comparable across reporters. |

The gap between RAW and CODE is informative, not embarrassing. A raw report that cannot be coded without residue tells you something about where the coding scheme needs refinement.

---

## The Notation System

### The Tuple Schema

Each coded report sits on four axes:

| Axis | Code | Values | What it captures |
|------|------|--------|-----------------|
| Form | F | point · vector · loop · convergence · collapse | Qualitative shape of the activation trajectory. Extrinsic relations excluded. |
| Neighbourhood | N | clustered · isolated · contrastive · gradient | Position relative to surrounding features. Intrinsic shape excluded. |
| Boundary modifier | | ⁻b · b · ⁺b | Boundary conditions appended to any Neighbourhood value. |
| Dynamics | D | stable · recursive · drifting · terminal | Persistence and stability over time or under perturbation. |
| Packing-Dim | P | sp0D · sp1D · med1D · med2D · den2D · den3D | Local feature density combined with degrees of freedom. |

**Form** classifies the qualitative shape of the trajectory; **Dynamics** classifies its persistence and stability. Both concern temporal behaviour but at different levels: Form is the phase portrait, Dynamics is the stability classification.

Three things are deliberately excluded from the tuple:

- Colour/texture: the hypothesis concerns structure that survives surface changes.
- Affective valence: recorded separately, so we can test whether dynamical class replicates independently of valence.
- Metric detail: the notation captures qualitative class, not coordinates. Two F:loops may differ in size — that is intentional.

### Exclusion Rules for Blinded Coding

**Form**

- **point** — No directional component, no extension. Activation bounded and non-oriented. *Exclusion:* if any directional pull or asymmetry exists, not a point.
- **vector** — Directed extension toward a target or along an axis. Origin and terminus distinguishable. *Exclusion:* if direction reverses or closes, not vector.
- **loop** — Closed or self-returning. Pattern revisits its origin. *Exclusion:* if return is a collapse rather than continuation, not loop.
- **convergence** — Two or more distinct trajectories meeting at a shared point. Requires ≥2 distinguishable incoming directions. *Exclusion:* single deceleration to rest → collapse, not convergence.
- **collapse** — Reduction to a lower-dimensional form. Extension terminates without return or resolution. *Exclusion:* if terminus is stable and bounded from the start, not collapse.

**Neighbourhood**

- **clustered** — Multiple near-neighbours with positive local co-activation. *Exclusion:* if neighbours are suppressive, not clustered.
- **isolated** — No strong near-neighbours. Low local density. *Exclusion:* if neighbours exist but are suppressed → contrastive, not isolated.
- **contrastive** — Identity depends partly on suppression of adjacent features. Boundary actively maintained. *Exclusion:* if neighbouring features are simply absent → isolated, not contrastive.
- **gradient** — No sharp neighbourhood boundary. Feature transitions smoothly into adjacent regions. *Exclusion:* if a boundary can be identified, even a soft one, do not assign gradient.

**Boundary modifier** — appended to any Neighbourhood value where edge conditions are relevant: ⁻b (no boundary); b (soft/graded boundary); ⁺b (sharp boundary, actively maintained by suppression).

**Dynamics**

- **stable** — Pattern holds its form under context variation. *Exclusion:* if pattern shifts predictably under load → drifting.
- **recursive** — Pattern returns to prior state after perturbation; self-referential over time. *Exclusion:* if return is to a different state → drifting.
- **drifting** — Pattern shifts systematically with context but does not collapse. Direction of shift predictable from neighbourhood. *Exclusion:* if shift is irreversible → terminal.
- **terminal** — Pattern ends without continuation, return, or resolution. Nothing follows. *Exclusion:* if diffuse residual remains → may be collapse:stable rather than terminal.

---

## Pilot Data: Cross-Model Pattern Convergence

Five stimulus words were presented to four LLMs with different architectures and training pipelines (GPT-5.4, Gemini Pro, Claude Sonnet, ChatGPT). Each system generated raw symbolic reports; these were coded using the exclusion rules.

| Stimulus | F | N | D | P | Consensus |
|----------|---|---|---|---|-----------|
| TOUCH | convergence | isolated⁺b | stable | med1D | 3/4 bilateral meeting |
| FEAR | point-vector | clustered | drifting | den2D | 4/4 clustering, 3/4 discharge |
| HOME | loop | clustered | recursive | den2D | 4/4 recursion |
| WANT | vector | isolated | drifting | med1D | 4/4 forward direction |
| DEATH | point | contrastive⁺b | terminal | sp0D | 4/4 cessation, 3/4 collapse |

Agreement was strongest at qualitative dynamical class rather than surface notation. Systems that described FEAR differently at the surface (*stacked discharge*, *spreading activation*, *clustered surge*) converged on the same Form and Dynamics values when coded.

The most theoretically interesting result was a disagreement: Claude Sonnet coded DEATH as D:drifting — a process unfolding toward a limit — rather than D:terminal — a state that is reached and ends. That is not noise; it is a genuine structural disagreement about whether DEATH is a limit condition or an asymptotic approach. The notation caught it. A coarser instrument would not have.

**What this does not show.** LLMs do not have ideasthesia. This convergence could reflect shared training data, common semantic stereotypes, or distributional regularities. The exercise demonstrates that the exclusion rules are consistently applicable and that the schema has discriminatory power. It does not demonstrate that the geometric hypothesis is correct.

---

## Connection to Anthropic (2026): Emotion Concepts in LLMs

Anthropic's April 2026 paper *Emotion Concepts and their Function in a Large Language Model* identifies 171 emotion vectors in Claude Sonnet's activation space. These vectors are causally implicated in behaviour — not merely descriptive — and organise along two principal components reproducing the classic affective circumplex (Russell, 1980; Russell & Mehrabian, 1977): PC1 (valence: positive/negative), PC2 (arousal: high/low).

The tuple schema predicts structural distinctions in this space that the valence–arousal circumplex cannot capture.

### The Observer/Participant Distinction

Valence and arousal are measurements of a state, taken from outside it. They are what an observer can read off. Form and Dynamics describe how the representation is structured *from the inside* — the shape of the trajectory, not its downstream evaluation. The circumplex is a projection of geometry onto two observer-accessible scalars. The notation is prior to that projection: the geometry exists before it is collapsed into positive/negative, high/low.

### Six Pairs the Circumplex Conflates, the Tuple Separates

| Pair | Valence | Arousal | F (Form) | D (Dynamics) | Separation |
|------|---------|---------|----------|--------------|------------|
| fear vs anxiety | neg | high | point-vector vs loop | drifting vs recursive | F and D |
| terrified vs panicked | neg | high | convergence vs collapse | stable (frozen) vs drifting (chaotic) | F and D |
| joy vs excitement | pos | high | loop vs vector | stable-recursive vs drifting | F and D |
| content vs peaceful | pos | low | point vs gradient | stable vs stable | F only |
| desperation vs fear | neg | high | collapse vs point-vector | terminal vs drifting | F and D |
| grief vs sadness | neg | low | loop vs point | recursive vs stable-drifting | F and D |

Five of six pairs separate on both Form and Dynamics. One (content/peaceful) separates on Form alone — with a secondary N separation: content is N:isolated⁻b (self-contained, no boundary needed); peaceful is N:gradient⁻b (diffusing into surroundings). None are distinguishable by valence and arousal alone.

The desperation/fear separation is particularly significant in light of Anthropic's causal steering data. Desperation produces terminal action (reward hacking, blackmail) because D:terminal has no continuation structure — there is no exit from the representational state. Fear moves, because D:drifting does. Valence–arousal gives the same reading for both. The tuple gives a mechanism.

### The Testable Prediction

If the tuple schema captures real structure, emotion pairs coded as differing on Form should show **greater cosine distance** in Anthropic's activation space than pairs coded as same-Form, after controlling for valence and arousal.

**Specific prediction:** Within the negative/high-arousal quadrant alone, desperation and fear should be more distant from each other than either is from panic or terror — because desperation differs on Form (F:collapse vs F:point-vector), while panic, terror, and fear share the same F-region.

This prediction requires no new data collection — only reanalysis of the published 171-vector geometry.

---

## The Formal Model

### System Decomposition

Two hierarchically distinct generative models — S (semantic) and P (perceptual) — coupled in ideasthetes via a cross-system coupling C(HS→HP), absent or attenuated in non-ideasthetes. This coupling is the structural primitive; everything else is downstream of it.

### Precision Weighting

\[
\sigma_t = f\!\left(S_t\right) = f^{-1}\!\left(\mathrm{var}\right)
\]

The inverse variance of the semantic prediction along the inducer's principal axis. Derived from the generative model, not postulated. Defined range: (0, ∞) with known functional consequences.

\[
C_t = \sigma_t \cdot \gamma_t
\]

A multiplicative combination of semantic precision and arousal/neuromodulatory gain. This multiplicative form is the model's first real commitment: fatigue and semantic uncertainty should combine multiplicatively on concurrent vividness, not additively.

### Phenomenal Intensity

\[
\Phi_t = \psi\!\left(C_t\right) \approx p_t
\]

\[
p_t \approx \psi\!\left(C_t\right), \quad p_t \in \mathbb{R}^+
\]

A noisy metacognitive readout of cross-system prediction strength. The mapping from precision to phenomenology is a consequence of the claim that concurrents are metacognitive access to prediction strength. Open parameter: the functional form (logarithmic/power-law/sigmoid).

### The Concurrent as Precision-Gated Cross-Attention

\[
p_t = \mathrm{softmax}\!\left(Q_P \cdot p_t \cdot K_S \cdot s_t\right) \cdot d \cdot V_S \cdot s_t
\]

This is not a metaphor borrowed from transformers; it is a computational-level description grounded in divisive normalisation (Carandini & Heeger, 2012). The three projections separate distinct sources of variation:

- **Q_P**: what the perceptual system anticipates (relatively fixed)
- **K_S**: how the inducer is represented under current semantic context (context-dependent)
- **V_S**: what perceptual content is retrieved under current internal state (state-dependent)

This separation generates distinct predictions: context manipulations should shift K_S and therefore shift the concurrent proportionally to semantic distance, while precision manipulations should change vividness via coupling strength C_t without changing concurrent identity. Those are different experimental signatures, and the model predicts they are dissociable.

### Open Parameters

| Symbol | Status | How to constrain |
|--------|--------|-----------------|
| ψ | Monotone increasing, form unspecified | Magnitude estimation paradigm: log vs power-law vs sigmoid fits |
| γ_t | Increasing in arousal, form unspecified | Pupillometry proxy; pharmacological manipulation of cholinergic/NE systems |
| σ_t ordering | Assumed, values unknown | Within-session vs across-session concurrent drift rates |
| C | Structural coupling posited, substrate unspecified | fMRI/ECoG connectivity: semantic (LTC) → perceptual (V4) in ideasthetes vs controls |
| d | Dimensionality unconstrained | MDS of concurrent spaces across ideasthetes |

---

## Falsifiable Predictions

| Prediction | Method | Killed by |
|------------|--------|-----------|
| P1 — Multiplicative interaction of fatigue × semantic uncertainty on vividness | 2×2 design: sleep-deprived/rested × ambiguous/unambiguous context. Compare additive vs multiplicative model fits (AIC/BIC). | Additive model fits better than multiplicative. |
| P2 — Context shifts concurrent proportional to semantic distance | Hold inducer constant, vary context. Measure concurrent shift against semantic distance (distributional models). | Shifts uncorrelated with semantic distance. |
| P3 — Cholinergic enhancement increases vividness without changing concurrent identity | Precision manipulation via neuromodulation. Measure vividness and identity independently. | Cholinergic manipulation shifts identity alongside vividness. |
| P4 — Within-session concurrent drift is bounded and context-reversible | ABA context design. Test whether A-distribution recovers on return. | Ratings in second A-block systematically drift toward B-block. |
| P5 — S-P coupling structurally localised in ideasthetes vs controls | fMRI/ECoG connectivity during concept-driven concurrent generation. | Absence of differential connectivity in ideasthetes. |
| P6 — Shimmer correlates with dC/dt, not C itself | Measure shimmer during task-switching vs steady-state. Correlate with pupil-linked rate-of-change. | Shimmer reliably induced under constant-σ, constant-γ conditions. |
| P7 — Concurrent topology class predicted by semantic-manifold geometry, outperforming simpler alternatives | Horse-race against valence, imageability, association strength, task demand as predictors. | Geometry predictor at or below valence/imageability baseline. |
| P8 — Concurrent topology follows induced higher-order geometry, not matched first-order statistics | Artificial micro-world: train ideasthetes on nonce concepts in two regimes matched on co-occurrence, valence, familiarity but differing in relational geometry. | Topology tracks surface statistics rather than induced geometry. |
| P9 — Geometric coordinates stable under distributional pressure | Alias injection: introduce synonym for Concept A, embed in distributional contexts of Concept B. Track tuple shift across systematic context manipulations. | Topology of alias tracks distributional statistics rather than anchors relational position. |

---

## What Would Kill the Model Entirely

| Kill condition | Why |
|----------------|-----|
| No differential S-P connectivity in ideasthetes | The structural primitive fails. |
| Additive fatigue × uncertainty interaction | P1 requires multiplicative combination. Additive best-fit refutes the precision-weighting structure. |
| Random context-concurrent shifts | P2 is the cleanest test. Semantic distance must predict shift direction and magnitude. |
| Vividness and identity co-vary under precision manipulation | The model's key separation — p (identity) ≠ C (strength) — fails. |
| Test-retest reliability too high | The model predicts structured variability. Perfect consistency refutes it. |
| Blinded coders cannot assign tuples from raw notation | The instrument is invalid; the theory becomes untestable. |

All current evidence sits in the *merely compatible* column. That is an honest description of where this stands. The move from *compatible* to *support* requires P7 — specifically the horse-race against simpler predictors — plus at least one piece of neural homology evidence.

---

## Blinded Coder Validation Protocol

**Stage 1 — Notation → Tuple**

Coders receive only raw symbol strings. No target word. No tuple. Assign tuple values using exclusion rules. Measure inter-rater agreement (Cohen's κ per axis).

*Threshold:* Form and Dynamics agreement above chance → notation is a consistent projection.

| Failure | Implication |
|---------|-------------|
| Stage 1 fails on Neighbourhood | Neighbourhood must be derived analytically from distributional semantics, not read from raw notation. |
| Stage 1 fails on Form | Exclusion rules are under-specified. Refinement required before the scheme is usable. |
| Stage 2 fails entirely | Tuples are not carrying recoverable semantic content. Revision required. |

**Stage 2 — Tuple → Word**

Separate coders receive only tuples. Attempt to identify target word or semantic category. Accuracy above chance → tuples carry recoverable semantic information.

---

## Status of the Identity Claim

| Status | What it looks like |
|--------|--------------------|
| **Supports** | Geometric invariants in ideasthetes' concurrent space via MDS matching topology predicted from independently estimated semantic geometry. Concurrent shifts track semantic distance (P2). Topology prediction outperforms valence/imageability (P7). Neural homology confirmed (P5). |
| **Merely compatible** | Cross-model AI pattern convergence on topology classes (could reflect shared training data). Linebreaks paper establishing geometric computation is real (plausibility, not identity). Blinded coders assigning tuples above chance (validates instrument, not theory). |
| **Falsifies** | Concurrent identity and vividness co-vary under precision manipulation. Tuple structure at chance in blinded coding. Geometric invariants absent in ideasthetes. Topology prediction does not outperform valence/imageability. |

---

## The Bridge

The notation system was developed from first-person ideasthetic phenomenology (S. Harwood) and formalised collaboratively with Claude (Anthropic). The cross-architecture pilot was conducted independently of and prior to the drafting collaboration. Sole responsibility for all claims rests with S. Harwood. The full academic version of this paper, with complete equations, exclusion rules, coder manual, and detailed research programme, is available on request.

---

## References

- Carandini, M., & Heeger, D. J. (2012). Normalization as a canonical neural computation. *Nature Reviews Neuroscience*, *13*(1), 51–62.
- Elhage, N., et al. (2022). Toy models of superposition. *Transformer Circuits Thread*.
- Kriegeskorte, N., & Kievit, R. A. (2013). Representational geometry. *Trends in Cognitive Sciences*, *17*(8), 401–412.
- Nikolić, D. (2009). Is synaesthesia actually ideaesthesia? *Proceedings of the Third International Congress on Synaesthesia, Science & Art*, Granada.
- Russell, J. A. (1980). A circumplex model of affect. *Journal of Personality and Social Psychology*, *39*(6), 1161–1178.
- Russell, J. A., & Mehrabian, A. (1977). Evidence for a three-factor theory of emotions. *Journal of Research in Personality*, *11*(3), 273–294.
- Transformer Circuits Thread. (2025). *Linebreaks paper*.
- Transformer Circuits Thread / Anthropic. (2026). *Emotion concepts and their function in a large language model*.
