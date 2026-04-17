# Sync Checklist — ideasthesia_bridge

When any schema value, pair table, nav, or structural element changes,
check every file in this list before committing.

---

## Site files (adashirs.github.io repo)

These four files form the live site. They must be kept in sync with each other
and with the local TSHOF copies below.

| File | Role | What to check |
|---|---|---|
| `ideasthesia_geometry.html` | Main paper | Schema values, pair table, exclusion rules, nav tabs |
| `postcard.html` | Testable prediction | Pair table (F and D columns), nav tabs |
| `emotion_network.html` | Interactive network | Node/edge data if emotion codings change |
| `emotion_field.html` | Field visualisation | Emotion codings if schema changes |

---

## Local backup files (TSHOF repo, this folder)

| File | Mirrors | What to check |
|---|---|---|
| `ideasthesia_geometry.html` | Live paper | Must match adashirs version after every edit |
| `ideasthesia_as_geometry_v06.md` | Paper backup | Update version number and changelog note at bottom |
| `experiment_prompt_fresh_v07.md` | Experiment protocol (current) | Schema values, expected outputs table, integrity checklist, b-modifier rules |
| `schema_resolutions_note_v2.pdf` | Authority document | Read-only. If this changes, a v3 PDF should be created. |
| `phase1_run_protocol_v07.md` | Phase 1 run protocol | Architecture list, run conditions, file naming, analysis steps |
| `phase2_priming_protocol_v07.md` | Phase 2 priming protocol | Priming turns, conditions, predictions, analysis steps |
| `provisional_baseline_v07.md` | Phase 2 control reference | Consensus codings from Phase 1; NOT a formal canon update |
| `decision_ledger.md` | Settled and open decisions | D-013 through D-023 added; D-020 to D-023 for cross-arch Phase 2 |

---

## Nav tabs — all four site files must show all four tabs

```html
<a href="ideasthesia_geometry.html" class="nav-link [active on paper]">Paper</a>
<a href="emotion_network.html" class="nav-link [active on network]">Network</a>
<a href="emotion_field.html" class="nav-link [active on field]">Field</a>
<a href="postcard.html" class="nav-link [active on postcard]">Postcard</a>
```

Add `class="nav-link active"` on whichever tab is the current page.

---

## Pair table — canonical values (v0.7)

If any of these change, update: paper, postcard, experiment_prompt_fresh_v07.md, v06.md.

| Pair | F | D | Separation |
|---|---|---|---|
| fear vs anxiety | vector vs loop | drifting vs recursive | F and D |
| terrified vs panicked | point ⚠ vs collapse | stable vs drifting | F and D |
| joy vs excitement | loop vs vector | recursive vs drifting | F and D |
| content vs peaceful | point vs point ⚠ | stable vs stable | N only |
| desperation vs fear | collapse vs vector | terminal vs drifting | F and D |
| grief vs sadness | loop vs point | recursive vs drifting | F, N and D |

Key attractor-coding decisions:
- SADNESS = D:drifting (slow dissipation, not a resting point) — D-014
- JOY = D:recursive (loop is the attractor; stable is implied) — D-013
- TERRIFIED = F:point ⚠ under empirical review; pilots consistently produce F:convergence — D-015
- PEACEFUL = F:point ⚠ under empirical review; pilots consistently produce F:gradient — D-016
- stable-recursive and stable-drifting are retired compound values — D-013
- b-modifier exclusion rules added to prompt — D-017

---

## Two-repo problem

The adashirs.github.io repo is NOT cloned locally.
Workflow until it is:
1. Edit the local TSHOF copy (Desktop Commander can do this).
2. Copy the updated file content into the GitHub web editor for adashirs.
3. Commit both.

To fix permanently: clone adashirs repo locally, then Desktop Commander
can push both repos in one operation.

---

## Phase 1 and Phase 2 files

| File | Role |
|---|---|
| `phase1_run_protocol_v07.md` | Phase 1 run protocol |
| `phase2_priming_protocol_v07.md` | Phase 2 priming protocol — start here for relational trials |
| `phase_2_field_condition.md` | Living document — theory and per-emotion predictions |
| `phase_2_field_condition_v02.pdf` | Snapshot at time of writing — read-only reference |
| `Twelve anchor emotions tuple coding/Phase1_v07/` | Phase 1 run outputs and preliminary analysis |
| `phase2_results_v07.md` | Phase 2 cross-architecture results (updated 15 April) |
| `phase2_v07_preliminary_analysis.md` | Phase 2 Sonnet-only analysis (14 April; JOY N error, see handover) |
| `Twelve anchor emotions tuple coding/Phase2_v07/` | Phase 2 run outputs |
| `handover_note_15apr2026.md` | Current handover note |

---

## Version history

| Version | Date | Changes |
|---|---|---|
| v0.5 | April 2026 | Base version |
| v0.5.1 | April 2026 | Minor fixes |
| v0.6 | 13 April 2026 | Temporal-frame convention; F closure argument (Poincaré-Bendixson); SADNESS recoded D:drifting; compound values retired; nav unified across site |
| v0.7 | 14 April 2026 | b-modifier exclusion rules; N diagnostic question; TERRIFIED/PEACEFUL answer-key footnotes removed from prompt; D-013 to D-017 added to ledger; Phase 1 run protocol created |
| v0.7.1 | 15 April 2026 | Cross-architecture Phase 2 complete (Gemini + GPT); phase2_results_v07.md updated; D-020 to D-023 added to ledger |
