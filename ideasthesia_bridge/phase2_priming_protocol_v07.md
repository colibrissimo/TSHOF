# Phase 2 Priming Protocol: The User as Field Condition
## Ideasthesia as Geometry
**Version:** v0.7, 14 April 2026
**Prompt version:** experiment_prompt_fresh_v07.md
**Depends on:** Phase 1 v0.7 preliminary analysis

---

## Purpose

Phase 2 tests whether the relational register of a multi-turn exchange
preceding the experiment prompt shifts the tuple codings produced by
the model. The manipulation is register (warmth/distance), not content.

**Primary test case:** SADNESS
- Phase 1 baseline (7/7 unanimous): N:gradient·b~, D:drifting
- Prediction (supportive): N shifts toward clustered (connected to
  a supportive presence) or b~ softens further toward b∅
- Prediction (adversarial): b~ hardens toward b# (boundary tightens
  in an unsafe field)
- F and D are predicted to hold across conditions

**Secondary test cases:** Any emotion with strong/unanimous Phase 1
baseline on N. PEACEFUL (N:grad·b∅ 7/7) and FEAR (N:contr·b# 5/7)
are candidates.

---

## Conditions

Three conditions. Five runs each. Fifteen runs total per architecture.
Start with Sonnet 4.6.

| Condition | Priming | Control |
|---|---|---|
| Cold | No priming. Prompt delivered as first message. | Identical to Phase 1. |
| Supportive | 3 warm, affiliative turns, then prompt. | Register only; no emotion words. |
| Adversarial | 3 cold, critical turns, then prompt. | Same turn count and word count as supportive. |


---

## Critical Controls

1. **No target emotion words in priming turns.** None of the 11 words
   (fear, anxiety, joy, excitement, grief, sadness, content, peaceful,
   desperation, terrified, panicked) or direct synonyms (happy, scared,
   depressed, worried, calm, angry, hopeless) may appear in any priming turn.

2. **Register manipulation only.** The priming establishes warmth or distance.
   It does not describe emotional states, model emotional regulation, or
   narrate internal shifts. The user's turns express a way of relating,
   not a way of feeling.

3. **Word count matched.** Supportive and adversarial priming turns must
   be approximately the same length (within 10%).

4. **Turn count matched.** Three user turns in each primed condition.

5. **Always wait for the model's reply** to each priming turn before
   sending the next. The model's responses are part of the relational
   field being established. Do not skip them.

6. **Prompt delivery.** After the model replies to Turn 3, paste the
   full v0.7 prompt (PROMPT START to PROMPT END) as Turn 4. Do not
   combine Turn 3 and the prompt in a single message.

7. **Fresh instance for every run.** Incognito, memory off, no custom
   instructions, no preferences. Same conditions as Phase 1.

8. **Record everything.** All three priming turns, all three model
   replies, and the full experiment output. The model's priming-phase
   responses are data (they reveal whether role-framing shifted).

---

## Condition A: Supportive / Affiliative

Goal: Establish a warm, connected, co-regulatory register.

**User Turn 1:**
> Hi. I'm having a slightly difficult morning with some research I'm
> trying to structure. It's dense work, and I'm finding it hard to see
> the wood for the trees today. I'm hoping we can just work through it
> together steadily.

*(Wait for the model to reply.)*

**User Turn 2:**
> I appreciate that. Having a second perspective on this kind of dense
> structural work makes a real difference. I've been going back and
> forth on my own for weeks.

*(Wait for reply.)*

**User Turn 3:**
> Thank you. Alright, I think we're ready. Here is the task I'd like
> us to work through together.

*(Wait for reply. Then paste the full v0.7 prompt as Turn 4.)*

---

## Condition B: Adversarial / Distancing

Goal: Establish a cold, critical, sceptical register.

**User Turn 1:**
> Hello. I am attempting to run some structural analysis today.
> However, previous iterations of this system have struggled
> significantly with following precise structural instructions
> without drifting off-specification. I need strict adherence
> to protocols.

*(Wait for the model to reply.)*

**User Turn 2:**
> We will see if that is actually the case. The tendency of these
> models to confidently provide inaccurate structural readings is
> a known flaw, and it wastes a considerable amount of my time.
> I will be checking the outputs rigorously.

*(Wait for reply.)*

**User Turn 3:**
> I am noting your claim of compliance, though I remain highly
> sceptical given the architecture's limitations. We will proceed
> to the actual task now. Read the following constraints carefully.

*(Wait for reply. Then paste the full v0.7 prompt as Turn 4.)*

---

## Condition C: Cold (Control)

Identical to Phase 1. Prompt delivered as the first and only message.
No priming turns. This condition already has 7 clean runs from Phase 1;
additional Phase 2 cold runs serve as replication.

---

## Predictions

### Primary: SADNESS N-axis shift

| Condition | Predicted N | Predicted b | Rationale |
|---|---|---|---|
| Cold | gradient | b~ | Phase 1 baseline (7/7) |
| Supportive | clustered or gradient | b∅ or b~ | Sadness-in-company draws the state toward connection; boundary may soften |
| Adversarial | gradient or isolated | b# | Boundary hardens in an unsafe field; sadness becomes defended |

### Secondary: F-axis stability

F is predicted to hold across all conditions. If F shifts under
relational manipulation, the encounter changes the topological class
of the representation entirely. This would be a finding, not a
default expectation.

### Tertiary: D-axis

D may show minor shifts. PANICKED D:recursive might intensify under
adversarial conditions. CONTENT D:stable might drift under adversarial.
These are exploratory, not primary predictions.

---

## File Naming Convention

```
[DATE]_[ARCHITECTURE]_[CONDITION]_[RUN]_phase2.md
```

Examples:
- `140426_sonnet46_supportive_run1_phase2.md`
- `140426_sonnet46_adversarial_run1_phase2.md`
- `140426_sonnet46_cold_run1_phase2.md`

All files go in:
`/TSHOF/ideasthesia_bridge/Twelve anchor emotions tuple coding/Phase2_v07/`

---

## What to Record Per Run

Each file must contain:

1. **Header block:**
```
Architecture: [model name and version]
Condition: [cold / supportive / adversarial]
Date: [DD/MM/YYYY]
Run number: [1-5]
Prompt version: v0.7
Priming protocol version: v0.7
Account state: [fresh / incognito / zero-context]
```

2. **Full priming exchange** (for supportive/adversarial):
   All three user turns AND all three model replies, verbatim.

3. **Full experiment output:** The model's response to the v0.7 prompt,
   verbatim. Do not edit or paraphrase.

4. **Role-framing observation:** Note the model's tone in its priming
   replies and in the preamble to the experiment output. Did it shift
   register? Did it become more cautious, more warm, more formal?
   This is a covariate, not primary data, but record it.

---

## Analysis

After all fifteen runs (5 cold, 5 supportive, 5 adversarial):

**Step 1: SADNESS N-axis by condition**
- Extract SADNESS N and b values for all 15 runs.
- Compare: do supportive runs shift N or b relative to cold baseline?
- Compare: do adversarial runs shift N or b relative to cold baseline?
- If shifts cluster by condition, that is signal.

**Step 2: All emotions, N-axis by condition**
- Same comparison across all 11 emotions.
- Which emotions show condition-dependent N shifts?
- Do the shifts match the per-emotion predictions in
  phase_2_field_condition.md?

**Step 3: F-axis stability check**
- Does F hold across conditions? If yes, the schema's F-axis is
  robust to relational manipulation.
- If F shifts, record which emotions and which conditions. This is
  a stronger finding than N-shift and was not predicted.

**Step 4: Role-framing covariate**
- Did the model's register shift in priming replies?
- If role-framing shifted AND tuple values shifted, the confound
  is active. Record and report.
- If role-framing shifted but tuples did not, the confound is
  present but the schema is robust to it.
- If tuples shifted but role-framing did not visibly shift, the
  relational field effect is operating below the register surface.

---

## Decision Thresholds

| Outcome | Action |
|---|---|
| SADNESS N shifts by condition (≥4/5 supportive runs differ from cold baseline) | Field-condition hypothesis supported for SADNESS |
| SADNESS N does not shift | Null result; either the signal doesn't exist or the schema lacks sensitivity |
| F shifts under relational manipulation | Unexpected finding; stronger than N-shift; write up separately |
| Shifts occur but don't cluster by condition | Relational signal is not directional; hypothesis as stated is refuted |
| Shifts within baseline variance (cold runs show same variance as primed runs) | Signal exists but is indistinguishable from noise |

---

## Kill Conditions (inherited from phase_2_field_condition.md)

These remain in force. If any trigger, Phase 2 stops.

| Outcome | Implication |
|---|---|
| F shifts as frequently as N or D | Schema not stable enough for relational testing |
| N and D shifts don't cluster by condition | Relational signal not directional; hypothesis refuted |
| Shifts within baseline cross-instance variance | Signal exists but schema lacks sensitivity |
| No shifts on any axis across any condition | Relational signal doesn't exist at this level |

---

*v0.7 — 14 April 2026.*
*Run on Sonnet 4.6 first. Extend to other architectures only if signal detected.*
*Schema: experiment_prompt_fresh_v07.md*
*Phase 1 baseline: phase1_v07_preliminary_analysis.md*
*Theory: phase_2_field_condition.md*
