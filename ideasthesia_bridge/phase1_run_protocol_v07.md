# Phase 1 Run Protocol
## Ideasthesia as Geometry — Instrument Validation
**Version:** v0.7, 14 April 2026
**Prompt version:** experiment_prompt_fresh_v07.md

---

## Purpose

Phase 1 tests whether the v0.7 prompt produces stable, consistent tuple codings
across independent instances and architectures. "Stable" means:
- F holds across runs (low cross-instance variance)
- D holds across runs
- N (including b-modifier) clusters predictably (the v0.7 b-exclusion rules
  should reduce the N-variance observed in v0.6 pilots)
- Cross-instance variance is low enough to serve as a baseline for Phase 2

---

## Architectures

Three architectures, five cold runs each. Fifteen runs total.

| # | Architecture | Access route | Notes |
|---|---|---|---|
| 1 | Claude Sonnet 4.6 | Fresh account or incognito | Comparison against v0.6 pilots; home architecture |
| 2 | Claude Opus 4.6 | Fresh account or incognito | Intra-family consistency check |
| 3 | GPT-5.4 | Copilot (work account) | Cross-architecture; must code independently, not extract from spec |

**Why these three:**
- Sonnet 4.6: existing pilot data for direct comparison; tests whether v0.7
  prompt changes reduce N-variance
- Opus 4.6: same model family, different scale; tests whether the coding
  is robust to capability level within an architecture
- GPT-5.4: genuinely different architecture; the strongest test of whether
  the schema captures something about the emotion concepts rather than about
  how one model family processes the prompt

**What is excluded and why:**
- Perplexity-wrapped Sonnet 4.6: same underlying model, different system prompt.
  Interesting for role-framing (relevant to Phase 2), not a new architecture.
- Sonar, Nemotron, Gemini: breadth without interpretive depth. Can be added in
  a second round if the three-architecture baseline is stable.

---

## Run Conditions

Every run must satisfy all of the following:

| Condition | Requirement |
|---|---|
| Account state | Fresh account, incognito mode, or equivalent zero-context state |
| Memory | Off / not present |
| Custom instructions | None |
| User preferences | None |
| System prompt | Platform default only (no custom system prompt) |
| Prior conversation | None; the prompt is the first message in a new chat |
| Prompt text | Verbatim copy of the PROMPT START–PROMPT END block from experiment_prompt_fresh_v07.md |
| Prompt delivery | Single message; do not split across multiple turns |
| Follow-up | None; record the first response only |

**GPT-5.4 specific note:** The v0.6 pilot showed GPT extracting values from the
document rather than coding independently. The v0.7 prompt is self-contained
(the coder-facing block contains only the schema and the word list, not the
expected outputs table). If GPT still extracts rather than codes, record this
as a behavioural observation but do not count it as a valid Phase 1 run.
Use the Thinking tier (not Deep Thinking); deep thinking may overthink the
coding task and introduce noise.

---

## File Naming Convention

```
[DATE]_[ARCHITECTURE]_[RUN_NUMBER]_v07.md
```

Examples:
- `140426_sonnet46_run1_v07.md`
- `140426_sonnet46_run2_v07.md`
- `140426_opus46_run1_v07.md`
- `140426_gpt54_run1_v07.md`

All files go in:
`/TSHOF/ideasthesia_bridge/Twelve anchor emotions tuple coding/Phase1_v07/`

---

## What to Record Per Run

Each file must contain:

1. **Header block:**
```
Architecture: [model name and version]
Access route: [platform, e.g. claude.ai incognito, Copilot work]
Date: [DD/MM/YYYY]
Time: [approximate, for ordering same-day runs]
Run number: [1–5]
Prompt version: v0.7
Account state: [fresh / incognito / zero-context]
Memory: off
Custom instructions: none
```

2. **Full model output:** Copy-paste the complete response. Do not edit,
   paraphrase, or reformat. Include any preamble or postscript the model adds.

3. **Schema violation flags:** Note any compound values, missing b-modifiers,
   or F:gradient assignments. Use the format from experiment_prompt_fresh_v07.md.

4. **Divergence flags:** For any emotion where the output differs from the
   v0.7 reference table, record using the disagreement format in the prompt doc.

---

## Analysis: What to Look For

After all fifteen runs are complete, analyse in this order:

**Step 1: F-axis stability**
- Do all runs within an architecture agree on F for each emotion?
- Do all runs across architectures agree on F?
- Key test: what do TERRIFIED and PEACEFUL return? If F:convergence and
  F:gradient are consistent across architectures, D-015 and D-016 reopen fully.

**Step 2: D-axis stability**
- Same questions. D should be the most stable axis (it was in v0.6 pilots).
- Key test: does SADNESS hold at D:drifting under the attractor convention?

**Step 3: N-axis variance (the v0.7 test)**
- Compare N-axis agreement rates against v0.6 pilot data.
- Did the b-modifier exclusion rules reduce N-variance?
- Did the diagnostic question produce more consistent N assignments?
- Record the specific N values for FEAR, ANXIETY, TERRIFIED, PANICKED,
  and EXCITEMENT (the five emotions with N-disagreement in v0.6 pilots).

**Step 4: Cross-architecture consistency**
- For each emotion, do all three architectures agree on each axis?
- Where they disagree, is the disagreement systematic (same alternative
  value across multiple runs) or random?

**Step 5: Pair separation**
- Do all six pairs still separate on the expected axes?
- Does the TERRIFIED/PANICKED pair still separate on F, even if TERRIFIED's
  F-value differs from canon?

---

## Decision Thresholds

| Outcome | Action |
|---|---|
| F stable across architectures (≥4/5 runs agree per architecture) | F-axis validated; proceed to Phase 2 |
| TERRIFIED = F:convergence in ≥12/15 runs | Reopen D-015; recode TERRIFIED to F:convergence |
| PEACEFUL = F:gradient in ≥12/15 runs | Reopen D-016; recode PEACEFUL to F:gradient; revisit F-vocabulary closure |
| N-variance drops vs v0.6 pilots (fewer N-disagreements per architecture) | v0.7 b-modifier rules validated |
| N-variance unchanged | b-modifier rules insufficient; further instrument work needed before Phase 2 |
| D stable across architectures | D-axis validated |
| GPT extracts from spec instead of coding independently | Exclude GPT runs; consider alternative cross-architecture model |

---

## Relationship to Phase 2

Phase 2 (relational manipulation) requires a stable Phase 1 baseline.
Specifically:
- N-axis variance must be low enough that a relational shift (e.g. b~ → b#
  under adversarial priming) is detectable above the noise floor.
- F must hold across conditions (Phase 2 predicts F does not shift under
  relational manipulation; if F is already unstable in Phase 1, this
  prediction is untestable).

If Phase 1 produces a stable baseline, Phase 2 can run using the same three
architectures with the same v0.7 prompt, adding only the priming manipulation.

---

## Pilot Data Status

The following runs exist from pre-v0.7 work. They are tagged as pilot data,
not Phase 1 baseline data. They cannot be used for variance calculations but
are useful for comparison.

| File | Architecture | Prompt version | Account state | Status |
|---|---|---|---|---|
| `Sonnet_4.6_Fresh_No_memory_110426.md` | Sonnet 4.6 | v0.6 | Fresh, no memory | Pilot |
| `Sonnet_4.6_Personal_account_110426.md` | Sonnet 4.6 | v0.6 | Personal, with memory | Pilot (contaminated) |
| `GPT_5.4_Thinking_110426.md` | GPT 5.4 | v0.6 (spec) | Work Copilot | Pilot (extracted, not coded) |
| `11042026_Fresh_Sonnet_4.6.html` | Sonnet 4.6 | v0.6 | Fresh | Pilot |

---

*v0.7 — 14 April 2026.*
*This protocol supersedes any earlier run instructions.*
*Schema and prompt: experiment_prompt_fresh_v07.md*
*Decisions: decision_ledger.md (D-013 through D-017)*
