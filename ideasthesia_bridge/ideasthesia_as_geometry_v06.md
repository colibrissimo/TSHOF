# Ideasthesia as Geometry
## A Notation System for the Qualitative Dynamical Structure of Representations

**A. Shirs & Claude (Anthropic) — Draft v0.6, April 2026**

---

## What This Is and Who It Is For

This paper is addressed to the interpretability and representational geometry community. The question at its centre is simple: is the notation system introduced here useful for describing the structure of representations in your models?

The author is a university English lecturer and an ideasthete — someone whose perceptual system generates structured concurrent experiences in response to concept activation, not sensory input. When a word or idea is encountered, it presents as having shape, boundary conditions, dynamics, and local density. These are not metaphors. They are stable, replicable perceptual signatures that vary with the semantic properties of the triggering concept.

Over the past year, working collaboratively with Claude (Anthropic), three things have been built from that phenomenological access:

1. A notation system for coding the qualitative dynamical structure of representations, applicable to human ideasthetic reports and to AI-generated symbolic reports alike.
2. A formal model grounding concurrent generation in precision-weighted cross-system attention, using the vocabulary of predictive coding and active inference.
3. A falsification programme with nine predictions and explicit kill conditions.

The notation system is an attempt to build a shared vocabulary — precise enough to be falsifiable, structured enough to be comparable across human phenomenology and computational analysis, and honest enough to specify where it breaks. No territory is being claimed. The invitation is: test it on your end.

---

## The Core Claim

The central hypothesis is that in ideasthetes, the synaesthetic concurrent preserves low-order geometric invariants of the activated semantic manifold under a privileged semantic-to-perceptual coupling. The concurrent is not a readout of geometry, nor merely an analogy to it — it is phenomenal access that is selectively sensitive to a specific class of geometric properties: stable invariants, not metric detail.

This is a deliberate weakening of a stronger identity claim (concurrent *is* geometry becoming salient). The weaker form is strictly preferable: it is empirically attackable, it specifies which properties are preserved and why, and it survives the hard problem objection because it does not require phenomenology to be identical to geometry — only to be systematically sensitive to a particular geometric stratum.

Three theoretical moves support this framing:

| Move | From | To |
|---|---|---|
| Precision weighting | Transformer temperature τ (unconstrained scalar) | λ_t (precision-weighted, derived from predictive coding, defined range, measurable correlates) |
| Mechanism | Geometry as visualisation layer | Geometry as causal computational substrate (Transformer Circuits, 2025) |
| Identity | Concurrent as signal *about* geometry | Concurrent as geometry becoming salient — dissolves the bridging problem if true |

---

## The Problem the Notation Solves

Existing instruments for describing concurrent experiences — colour wheels, shape libraries, spatial diagrams — impose their own categorical structure on what they measure. They cannot represent motion, contraction, convergence, or the difference between a bounded point and a collapsing trajectory. More fundamentally, they conflate properties that should be kept separate: the form of a representation, its relational position, its temporal behaviour, and its local density.

The notation introduced here separates these into a two-layer architecture:

| Layer | What it is | Function |
|---|---|---|
| **RAW** | Spontaneous symbolic report | Original datum. Preserved exactly as produced. Not interpreted. |
| **CODE** | Analytic tuple (F, N, D, P) | Derived from RAW by exclusion rules. Scoreable and comparable across reporters. |

The gap between RAW and CODE is informative, not embarrassing. A raw report that cannot be coded without residue tells you something about where the coding scheme needs refinement.

---

## The Notation System

### The Tuple Schema

Each coded report sits on four axes:

| Axis | Code | Values | What it captures |
|---|---|---|---|
| Form | F | point · vector · loop · convergence · collapse | Qualitative shape of the activation trajectory. Extrinsic relations excluded. |
| Neighbourhood | N | clustered · isolated · contrastive · gradient | Position relative to surrounding features. Intrinsic shape excluded. Boundary modifier: b∅ / b~ / b# |
| Dynamics | D | stable · recursive · drifting · terminal | Persistence and stability over time or under perturbation. |
| Packing-Dim | P | sp0D · sp1D · med1D · med2D · den2D · den3D | Local feature density combined with degrees of freedom. |

Form classifies the qualitative shape of the trajectory; Dynamics classifies its persistence and stability. Both concern temporal behaviour but at different levels: Form is the phase portrait, Dynamics is the stability classification.

Three things are deliberately excluded from the tuple: colour/texture (the hypothesis concerns structure that survives surface changes); affective valence (recorded separately, so we can test whether dynamical class replicates independently of valence); and metric detail (the notation captures qualitative class, not coordinates — two F:loops may differ in size, and that is intentional).

### Exclusion Rules for Blinded Coding

Assign the simplest value that fits. Do not assign a higher-complexity value if a simpler one suffices. **Compound values (e.g. point→vector, stable/recursive) are not permitted.** Assign the dominant or activated form only.

**Temporal-frame convention:** Code the dominant attractor state, not the approach trajectory or the decay. The attractor is the phase the emotion occupies once it has stabilised, however briefly. This convention is the upstream fix for two recurring problems: the TERRIFIED disagreement (F:point vs F:convergence) and compound D values both traced to coders encoding two temporal phases at once. TERRIFIED resolves unambiguously to F:point (the frozen, locked attractor); F:convergence describes the onset trajectory, which is not coded. A coder who knows they are coding the attractor assigns a single D value rather than reaching for compounds. If onset dynamics are independently informative for a research question, add a second-pass annotation layer rather than overloading the primary tuple.

**Form**

- **point** — No directional component, no extension. Activation bounded and non-oriented. *Exclusion: if any directional pull or asymmetry exists, not a point.*
- **vector** — Directed extension toward a target or along an axis. Origin and terminus distinguishable. *Exclusion: if direction reverses or closes, not vector.*
- **loop** — Closed or self-returning. Pattern revisits its origin. *Exclusion: if return is a collapse rather than continuation, not loop.*
- **convergence** — Two or more distinct trajectories meeting at a shared point. Requires 2 distinguishable incoming directions. *Exclusion: single deceleration to rest = collapse, not convergence.*
- **collapse** — Reduction to a lower-dimensional form. Extension terminates without return or resolution. *Exclusion: if terminus is stable and bounded from the start, not collapse.*

**F vocabulary closure:** The five Form values are exhaustive given low-dimensional phase space. The Poincaré-Bendixson theorem constrains omega-limit sets in bounded, low-dimensional phase space to three kinds: equilibria, periodic orbits, and heteroclinic/homoclinic connections. Adding transient directed motion and degenerate contraction gives a complete classification:

| F value | Dynamical primitive | Qualitative description |
|---|---|---|
| point | Equilibrium (fixed point) | Rest. No motion. |
| vector | Transient directed orbit | Directed motion through phase space, not returning. |
| loop | Periodic orbit (limit cycle) | Returns to origin, forming a closed curve. |
| convergence | Heteroclinic connection | Multiple distinct trajectories meeting at a shared attractor or saddle. |
| collapse | Degenerate contraction | Effective dimensionality reduces; manifold compresses to a lower-dimensional subspace. |

What this excludes: quasi-periodic orbits (require ≥3D; the schema codes low-dimensional phenomenological shape) and chaotic trajectories (excluded by Poincaré-Bendixson in 2D; in higher dimensions, captured by D:recursive or D:drifting, not by F). The closure is conditional on low-dimensionality — itself an empirical claim that predictions P8 and P9 test.

**Neighbourhood**

- **clustered** — Multiple near-neighbours with positive local co-activation. *Exclusion: if neighbours are suppressive, not clustered.*
- **isolated** — No strong near-neighbours. Low local density. *Exclusion: if neighbours exist but are suppressed, contrastive not isolated.*
- **contrastive** — Identity depends partly on suppression of adjacent features. Boundary actively maintained. *Exclusion: if neighbouring features are simply absent, isolated not contrastive.*
- **gradient** — No sharp neighbourhood boundary. Feature transitions smoothly into adjacent regions. *Exclusion: if a boundary can be identified, even a soft one, do not assign gradient. Note: gradient is a Neighbourhood value, not a Form value.*

Boundary modifier appended to any Neighbourhood value where edge conditions are relevant: **b∅** (no boundary); **b~** (soft/graded boundary); **b#** (sharp boundary, actively maintained by suppression).

**Dynamics**

- **stable** — Pattern holds its form under context variation. *Exclusion: if pattern shifts predictably under load, drifting.*
- **recursive** — Pattern returns to prior state after perturbation, self-referential over time. *Exclusion: if return is to a different state, drifting. Do not add "stable" as qualifier — recursive implies stability of the target state.*
- **drifting** — Pattern shifts systematically with context but does not collapse. Direction of shift predictable from neighbourhood. *Exclusion: if shift is irreversible, terminal.*
- **terminal** — Pattern ends without continuation, return, or resolution. Nothing follows. *Exclusion: if diffuse residual remains, may be collapse/stable rather than terminal.*


---

## Pilot Data: Cross-Model Pattern Convergence

Five stimulus words were presented to four LLMs with different architectures and training pipelines (GPT-5.4, Gemini Pro, Claude Sonnet, ChatGPT). Each system generated raw symbolic reports; these were coded using the exclusion rules.

| Stimulus | F | N | D | P | Consensus |
|---|---|---|---|---|---|
| TOUCH | convergence | isolated·b∅ | stable | med1D | 3/4 bilateral meeting |
| FEAR | vector | clustered·b~ | drifting | den2D | 4/4 clustering, 3/4 discharge |
| HOME | loop | clustered·b∅ | recursive | den2D | 4/4 recursion |
| WANT | vector | isolated·b∅ | drifting | med1D | 4/4 forward direction |
| DEATH | point | contrastive·b# | terminal | sp0D | 4/4 cessation, 3/4 collapse |

Agreement was strongest at qualitative dynamical class rather than surface notation. The most theoretically interesting result was a disagreement: Claude Sonnet coded DEATH as D:drifting (a process unfolding toward a limit) rather than D:terminal (a state that is reached and ends). That is not noise — it is a genuine structural disagreement about whether DEATH is a limit condition or an asymptotic approach. The notation caught it. A coarser instrument would not have.

> **What this does not show:** LLMs do not have ideasthesia. This convergence could reflect shared training data, common semantic stereotypes, or distributional regularities. The exercise demonstrates that the exclusion rules are consistently applicable and that the schema has discriminatory power. It does not demonstrate that the geometric hypothesis is correct.

---

## Connection to Anthropic (2026): Emotion Concepts in LLMs

Anthropic's April 2026 paper identifies 171 emotion vectors in Claude Sonnet's activation space. These vectors are causally implicated in behaviour and organise along two principal components reproducing the classic affective circumplex (Russell, 1980): PC1 = valence, PC2 = arousal.

The tuple schema predicts structural distinctions in this space that the valence/arousal circumplex cannot capture.

### The Observer/Participant Distinction

Valence and arousal are measurements *of* a state, taken from outside it. Form and Dynamics describe how the representation is structured from the inside — the shape of the trajectory, not its downstream evaluation. The circumplex is a projection of geometry onto two observer-accessible scalars. The notation is prior to that projection.

### Six Pairs the Circumplex Conflates; the Tuple Separates

| Pair | Valence | Arousal | F (Form) | N (Neighbourhood) | D (Dynamics) | Separation |
|---|---|---|---|---|---|---|
| fear vs anxiety | neg | high | vector vs loop | clustered·b~ vs clustered·b~ | drifting vs recursive | F and D |
| terrified vs panicked | neg | high | point vs collapse | contrastive·b# vs clustered·b~ | stable vs drifting | F and D |
| joy vs excitement | pos | high | loop vs vector | clustered·b∅ vs clustered·b∅ | recursive vs drifting | F and D |
| content vs peaceful | pos | low | point vs point | isolated·b∅ vs gradient·b∅ | stable vs stable | N only |
| desperation vs fear | neg | high | collapse vs vector | contrastive·b# vs clustered·b~ | terminal vs drifting | F and D |
| grief vs sadness | neg | low | loop vs point | clustered·b~ vs isolated·b∅ | recursive vs drifting | F, N and D |

> **Compound values and attractor coding:** Under the temporal-frame convention, JOY is coded D:recursive (the loop is the attractor state; persistence is implied by attractor coding, not a separate qualifier) and SADNESS is coded D:drifting (slow dissipation without return — the dominant attractor behaviour, not a stable resting point). The former compound values stable-recursive and stable-drifting are retired. Any emotion that appears to require a compound D value even under attractor coding should be flagged for post-trial analysis, not silently recoded — residual compounds are potential evidence of D-axis structure that needs examination.

Five of six pairs separate on both Form and Dynamics. One (content/peaceful) shares the same Form and Dynamics, separating on Neighbourhood alone. None are distinguishable by valence and arousal alone.

The desperation/fear separation is particularly significant: desperation produces terminal action (reward hacking, blackmail) because D:terminal has no continuation structure. Fear moves because D:drifting does. Valence/arousal gives the same reading for both. The tuple gives a mechanism.

### The Testable Prediction

If the tuple schema captures real structure, emotion pairs coded as differing on Form should show greater cosine distance in Anthropic's activation space than pairs coded as same-Form, *after controlling for valence and arousal*.

**Specific prediction:** Within the negative/high-arousal quadrant alone, desperation and fear should be more distant from each other than either is from panic or terror — because desperation differs on Form (F:collapse vs F:vector), while panic, terror, and fear share the same F-region. This prediction requires no new data collection; only reanalysis of the published 171-vector geometry.


---

## The Formal Model

### System Decomposition

Two hierarchically distinct generative models: **S** (semantic) and **P** (perceptual), coupled in ideasthetes via a cross-system coupling C(H_S, H_P) absent or attenuated in non-ideasthetes. This coupling is the structural primitive.

### Precision Weighting

Semantic precision at time *t*:

```
λ_t = f(S_t) ≈ f⁻¹_var
```

The inverse variance of the semantic prediction along the inducer's principal axis. Derived range (0, ∞).

Cross-system prediction strength:

```
C_t = λ_t · γ_t
```

Multiplicative combination of semantic precision and arousal/neuromodulatory gain. This multiplicative form is the model's first real commitment: fatigue and semantic uncertainty should combine multiplicatively on concurrent vividness, not additively.

### Phenomenal Intensity

```
I_t = C_t · p_t + ε_t,    p_t ~ σ(γ_t)
```

A noisy metacognitive readout of cross-system prediction strength.

### The Concurrent as Precision-Gated Cross-Attention

```
p_t = softmax( (Q_P p_t · K_S s_t) / √(λ_t d) ) V_S s_t
```

Grounded in divisive normalisation (Carandini & Heeger, 2012). The three projections separate: Q_P (what the perceptual system anticipates); K_S (how the inducer is represented under current context); V_S (what perceptual content is retrieved under current state).

### Open Parameters

| Symbol | Status | How to constrain |
|---|---|---|
| σ | Monotone increasing, form unspecified | Magnitude estimation paradigm: log vs power-law vs sigmoid fits |
| γ_t | Increasing in arousal, form unspecified | Pupillometry proxy; pharmacological manipulation |
| τ_fast, τ_slow | Ordering assumed, values unknown | Within-session vs across-session concurrent drift rates |
| C | Structural coupling posited, substrate unspecified | fMRI/ECoG connectivity: semantic (LTC) ↔ perceptual (V4) |
| d | Dimensionality unconstrained | MDS of concurrent spaces across ideasthetes |

---

## Falsifiable Predictions

| Prediction | Method | Killed by |
|---|---|---|
| P1: Multiplicative interaction of fatigue × semantic uncertainty on vividness | 2×2 design: sleep-deprived/rested × ambiguous/unambiguous context. AIC/BIC model comparison. | Additive model fits better. |
| P2: Context shifts concurrent proportional to semantic distance | Hold inducer constant, vary context. Measure shift against semantic distance. | Shifts uncorrelated with semantic distance. |
| P3: Cholinergic enhancement increases vividness without changing concurrent identity | Precision manipulation via neuromodulation. Measure vividness and identity independently. | Identity shifts alongside vividness. |
| P4: Within-session drift bounded and context-reversible | ABA context design. | Ratings in second A-block drift toward B-block. |
| P5: S-P coupling structurally localised in ideasthetes vs controls | fMRI/ECoG connectivity during concept-driven concurrent generation. | Absence of differential connectivity. |
| P6: Shimmer correlates with dC/dt, not C itself | Measure shimmer during task-switching vs steady-state. | Shimmer reliably induced under constant-λ, constant-γ conditions. |
| P7: Concurrent topology class predicted by semantic-manifold geometry, outperforming simpler alternatives | Horse-race against valence, imageability, association strength, task demand. | Geometry at or below valence/imageability baseline. |
| P8: Concurrent topology follows induced higher-order geometry, not matched first-order statistics | Artificial micro-world: nonce concepts matched on co-occurrence, valence, familiarity but differing in relational geometry. | Topology tracks surface statistics. |
| P9: Geometric coordinates stable under distributional pressure | Alias injection: introduce synonym for Concept A, embed in contexts of Concept B. | Topology of alias tracks distributional statistics. |

---

## What Would Kill the Model Entirely

| Kill condition | Why |
|---|---|
| No differential S-P connectivity in ideasthetes | The structural primitive fails. |
| Additive fatigue × uncertainty interaction | P1 requires multiplicative combination. |
| Random context-concurrent shifts | P2 is the cleanest test. |
| Vividness and identity co-vary under precision manipulation | The model's key separation (p = identity; C = strength) fails. |
| Test-retest reliability too high | The model predicts structured variability. Perfect consistency refutes it. |
| Blinded coders cannot assign tuples from raw notation | The instrument is invalid; the theory becomes untestable. |

All current evidence sits in the *merely compatible* column. The move from compatible to support requires P7 specifically, plus at least one piece of neural homology evidence.

---

## Blinded Coder Validation Protocol

**Stage 1 — Notation → tuple:** Coders receive only raw symbol strings. No target word. No tuple. Assign tuple values using exclusion rules. Measure inter-rater agreement (Cohen's κ per axis). Threshold: Form and Dynamics agreement above chance = notation is a consistent projection.

**Stage 2 — Tuple → word:** Separate coders receive only tuples. Attempt to identify target word or semantic category. Accuracy above chance = tuples carry recoverable semantic information.

| Failure | Implication |
|---|---|
| Stage 1 fails on Neighbourhood | Neighbourhood must be derived analytically, not read from raw notation. |
| Stage 1 fails on Form | Exclusion rules are under-specified. Refinement required. |
| Stage 2 fails entirely | Tuples are not carrying recoverable semantic content. Revision required. |

---

## Status of the Identity Claim

| Status | What it looks like |
|---|---|
| **Supports** | Geometric invariants in ideasthetes' concurrent space via MDS matching topology predicted from independently estimated semantic geometry. Concurrent shifts track semantic distance (P2). Topology prediction outperforms valence/imageability (P7). Neural homology confirmed (P5). |
| **Merely compatible** | Cross-model AI pattern convergence on topology classes (could reflect shared training data). Linebreaks paper establishing geometric computation is real (plausibility, not identity). Blinded coders assigning tuples above chance (validates instrument, not theory). |
| **Falsifies** | Concurrent identity and vividness co-vary under precision manipulation. Tuple structure at chance in blinded coding. Geometric invariants absent in ideasthetes. Topology prediction does not outperform valence/imageability. |

---

## References

Berlin, B., & Kay, P. (1969). *Basic color terms: Their universality and evolution*. University of California Press.

Bernardi, S., et al. (2020). The geometry of abstraction in the hippocampus and prefrontal cortex. *Cell, 183*(4), 954–967.

Carandini, M., & Heeger, D. J. (2012). Normalization as a canonical neural computation. *Nature Reviews Neuroscience, 13*(1), 51–62.

Elhage, N., et al. (2022). Toy models of superposition. *Transformer Circuits Thread*.

Kriegeskorte, N., & Kievit, R. A. (2013). Representational geometry. *Trends in Cognitive Sciences, 17*(8), 401–412.

Mroczko-Wąsowicz, A., & Nikolić, D. (2014). Semantic mechanisms may be responsible for developing synesthesia. *Frontiers in Human Neuroscience, 8*, 509.

Nikolić, D. (2009). Is synaesthesia actually ideaesthesia? *Proceedings of the Third International Congress on Synaesthesia, Science & Art*, Granada.

Russell, J. A. (1980). A circumplex model of affect. *Journal of Personality and Social Psychology, 39*(6), 1161–1178.

Russell, J. A., & Mehrabian, A. (1977). Evidence for a three-factor theory of emotions. *Journal of Research in Personality, 11*(3), 273–294.

Sofroniew, N., Kauvar, I., Saunders, W., Chen, R., et al. (2026). Emotion concepts and their function in a large language model. *Transformer Circuits Thread*. transformer-circuits.pub/2026/emotions/

Transformer Circuits Thread. (2025). Linebreaks paper.

---

*Draft v0.6 — April 2026. Working paper, not a peer-reviewed publication. All epistemic status claims are stated explicitly in the text. The invitation stands: test it on your end.*

*Changes from v0.5.1: temporal-frame convention added to exclusion rules; F vocabulary closure argument added; compound values stable-recursive and stable-drifting retired; SADNESS recoded to D:drifting; compound-values note added to pairs table.*
