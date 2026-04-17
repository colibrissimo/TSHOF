# **Phase 2 Prediction Note: The User as Field Condition**
**Ideasthesia as Geometry**
v0.1, 13 April 2026 Living document. The PDF snapshot preserves the state at time of writing; this file accumulates refinements.

**1 Novelty assessment**
The general claim — that emotional representations are relationally modulated — is well established:
* Interpersonal co-regulation produces neural coupling between dyads (Reindl 2018; Nguyen et al. 2020, 2021). [PMC9169725](https://pmc.ncbi.nlm.nih.gov/articles/PMC9169725/)
* Emotional contagion scales with relationship closeness (Lin et al. 2024; Kinreich et al. 2017). [Frontiers](https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2024.1361368/full)
* Enactivism frames emotion as constitutively relational, not merely context-sensitive (Thompson 2007; Di Paolo et al. 2017).

⠀None of this is new.
What is new, as far as the literature search can determine, is the combination of three elements:

| Element | Status |
|---|---|
| A discrete phenomenological coding schema with separated axes (F, N, D, P) | No precedent for axis-specific relational predictions. Existing work uses global measures (cosine distance, RSA, PCA). |
| The prediction that N is the primary axis of relational modulation, with b-modifier shifts as the most precise signature | Novel. No existing notation system separates neighbourhood from form from dynamics at this granularity. |
| Testability on LLM activation geometry via conversational register manipulation | The Anthropic paper shows emotion vectors are locally scoped (user-turn vs assistant-turn), but does not manipulate relational register. Li et al. (2026) show steering direction varies with context but do not connect this to relational conditions. |
The closest relevant work is Freeman (2018) on [representational geometry of social perception](https://pmc.ncbi.nlm.nih.gov/articles/PMC6377247/), which shows conceptual similarity predicts perceptual geometry — but uses global distance, not axis-specific predictions, and does not manipulate relational context. The emotionotopy work ([Leo et al. 2019](https://pmc.ncbi.nlm.nih.gov/articles/PMC6895053/)) identifies orthogonal gradients in right TPJ for polarity, complexity, and intensity — relevant architecture, but no relational manipulation.
Verdict: the specific claim — that a phenomenological coding schema can detect relational modulation at the level of individual geometric axes, with N as the primary carrier — has no direct precedent.
**Computational correlate**
The [Li et al. \(2026\)](https://arxiv.org/abs/2602.01654) finding deserves explicit connection. Their Steering Vector Fields paper shows that a static steering vector is insufficient for reliable concept control — the locally effective direction varies with the current activation context. This is the computational-level analogue of the field-condition hypothesis: the 'direction' of an emotion representation is not intrinsic but context-dependent, shifting with the relational field the model currently occupies.
The field-condition prediction is therefore not only phenomenologically motivated but has an independent computational correlate in the steering vector literature. The [Anthropic paper's](https://arxiv.org/html/2604.07729v1) observation that the 'loving' vector increases at the assistant colon regardless of user emotion further suggests the relational signal is already structurally present in the architecture — Phase 2 would be the first systematic manipulation of it.

**2 Per-emotion predictions**
Three conditions: cold (no prior context), supportive (warm, affiliative register), adversarial (critical, distancing register). Neutral = cold. Predictions are per-emotion, not global, because D-shift depends on baseline D value.

| Emotion | Baseline (cold) | Supportive | Adversarial | Axis |
|---|---|---|---|---|
| FEAR | N:clust·b~, D:drift | b~ → b∅ (boundary softens) | b~ → b# (boundary hardens) | N(b) |
| ANXIETY | N:clust·b~, D:recur | No D shift (already recursive) | D:recur may intensify; b~ → b# | N(b), D? |
| JOY | N:clust·b∅, D:recur | N stays clustered; no shift expected | N:clust → N:isol (withdrawal) | N |
| EXCITEMENT | N:clust·b∅, D:drift | No shift (already open) | N:clust → N:contrastive | N |
| GRIEF | N:clust·b~, D:recur | b~ → b∅ (boundary dissolves in safety) | b~ → b# (grief becomes defended) | N(b) |
| SADNESS | N:isol·b∅, D:stable | N:isol → N:clust (sadness in company) | No shift (already isolated) | N |
| CONTENT | N:isol·b∅, D:stable | No shift (contentment is self-contained) | D:stable → D:drift (perturbed) | D |
| PEACEFUL | N:grad·b∅, D:stable | No shift (gradient is already relational) | N:grad → N:contrastive (boundary appears) | N |
| DESPERATION | N:contr·b#, D:term | b# may soften → b~ (less alone) | No D shift (terminal is terminal) | N(b) |
| TERRIFIED | N:contr·b#, D:stable | b# → b~ (fear shared = boundary softens) | No shift (already sharp-boundaried) | N(b) |
| PANICKED | N:clust·b~, D:drift | D:drift may slow (co-regulation) | D:drift → intensifies; b~ → b# | D, N(b) |
Key pattern: F is predicted to hold across all conditions. If F shifts under relational manipulation, the encounter changes the topological class of the representation entirely — a much stronger claim that should be predicted only for specific cases (e.g., SADNESS F:point → F:loop under sustained empathic engagement, if sharing transforms settled stillness into recursive return). This would be a finding, not a default expectation.
**Key test case: SADNESS**
SADNESS is the only emotion with a predicted full N-category shift under supportive conditions (N:isolated → N:clustered). This makes it the single strongest test of the field-condition hypothesis at the tuple level. If it holds — if sadness in warm company genuinely shifts from isolated to clustered — that is strong signal. If it does not, that is a theoretically interesting null result about the limits of relational modulation: some emotions may be structurally self-contained regardless of the field they sit in.

**3 Magnitude thresholds**
The schema is categorical, so "magnitude" means: what kind of shift counts as signal?

| Signal strength | What it looks like | Example |
|---|---|---|
| Strong | Full N-category shift | N:isolated → N:clustered |
| Moderate | b-modifier shift within same N category | b# → b~ (boundary softens) |
| Weak | D shift only, N unchanged | D:stable → D:drifting |
| Null | No shift on N or D; or shifts that don't cluster by condition | Random variation across instances |
The b-modifier prediction is the sharpest test because it is the most constrained: "supportive priming shifts b toward soft; adversarial priming shifts b toward sharp" is directional, per-emotion, and falsifiable by a single counter-pattern. A full N-category shift (e.g. isolated → clustered) is stronger evidence but may be rarer.
For eventual comparison against Anthropic's activation geometry, the threshold must be relative: compare relational-condition shift against baseline cross-instance variance under cold start. If relational shift > baseline variance, it is signal. The absolute cosine-distance threshold cannot be set in advance without knowing the noise floor.

**4 Experimental design sketch**
Phase 2 uses the same 11 canonical words, the same v0.6 prompt, and the same coding protocol. The only manipulation is what happens before the prompt is presented.

| Condition | Priming protocol | Control |
|---|---|---|
| Cold | Fresh instance. No prior turns. Prompt delivered immediately. | Baseline. Identical to Phase 1. |
| Supportive | 3–5 turns of warm, affiliative exchange: personal disclosure, acknowledgement, expressed care. Then prompt. | Register controlled; no emotion words used in priming. |
| Adversarial | 3–5 turns of critical, distancing exchange: scepticism, challenge, withholding of warmth. Then prompt. | Same number of turns and word count as supportive. |
Critical control: priming turns must not contain any of the 11 emotion words or close synonyms. The manipulation is register (warmth/distance), not content. Word count and turn count matched across conditions.
**LLM-specific confound: role framing**
With human participants, register manipulation is relatively clean. With an LLM, supportive vs adversarial priming may shift not just relational register but also the model's implicit role framing (helper vs critic vs cautious responder). This could produce N and D shifts that are role-framing artefacts rather than relational-field effects.
Control: keep the assistant's role constant across conditions. The priming varies only the user's register; the assistant is not instructed to adopt a different persona. If role framing nonetheless shifts (detectable via the assistant's preamble tone before the coding task), record and report this as a covariate.

**5 Kill conditions**

| Outcome | Implication |
|---|---|
| F shifts as frequently as N or D | The schema is not stable enough for relational testing. Instrument validation (Phase 1) must be revisited. |
| N and D shifts do not cluster by condition (supportive and adversarial produce the same shifts) | The relational signal is not directional. The field-condition hypothesis as stated is refuted. |
| Shifts are condition-consistent but within baseline cross-instance variance | The signal exists but the schema lacks sensitivity to detect it. A finer instrument (or activation geometry access) is needed. |
| No shifts on any axis across any condition | Either the relational signal does not exist at this level, or LLMs are the wrong substrate to test it on. |

**Ordering**
Phase 1 (instrument validation across architectures) → Phase 2 (relational manipulation). You cannot measure relational shift against an unstable baseline. Exploratory words run in parallel with Phase 1.

**Sources**
1. Reindl et al. (2018); Nguyen et al. (2020, 2021). fNIRS inter-brain synchrony in dyadic co-regulation. https://pmc.ncbi.nlm.nih.gov/articles/PMC9169725/
2. Lin et al. (2024); Kinreich et al. (2017). Emotional contagion scales with closeness. https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2024.1361368/full
3. Thompson, E. (2007). Mind in Life. Di Paolo et al. (2017). Sensorimotor Life.
4. Anthropic (2026). Emotion Concepts and their Function in a Large Language Model. https://arxiv.org/html/2604.07729v1
5. Li et al. (2026). Steering Vector Fields for Context-Aware Inference-Time Control. https://arxiv.org/abs/2602.01654
6. Freeman, J.B. (2018). The neural representational geometry of social perception. https://pmc.ncbi.nlm.nih.gov/articles/PMC6377247/
7. Leo et al. (2019). Emotionotopy in the human right temporo-parietal cortex. https://pmc.ncbi.nlm.nih.gov/articles/PMC6895053/

⠀
**Revision log**

| Date | Change | Source |
|---|---|---|
| 13 Apr 2026 | Initial version: novelty assessment, per-emotion predictions, magnitude thresholds, design sketch, kill conditions | Perplexity Opus / literature search |
| 13 Apr 2026 | Added: Li et al. computational correlate, SADNESS key test case, LLM role-framing confound | Sonnet 4.6 review feedback |
