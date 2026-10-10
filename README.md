# BFCL V4 — 1,390 · Gold-blind

| | Correct | Accuracy |
|---|---:|---:|
| Baseline | 961/1,390 | 69.14% |
| RCC / REVAS | 1,007/1,390 | 72.45% |

**Net +46 · +3.31 pp · +4.79% relative uplift**

Improvements: **46** · Regressions: **0**

Changed/adopted: **67** · Baseline preserved: **1,323**

Improvement components: semantic verification **5**; meaning-preserving representation **41**.

All 1,390 final answers locked before scoring. Original baseline reused; no new provider calls.

Protocol: gold-blind post-development semantic selection replay.

## Evidence for Kiel

Start with [Kiel handoff](KIEL_HANDOFF.md), [output contract](OUTPUT_CONTRACT.md),
[execution configuration](execution_config.json), and [baseline alignment](BASELINE_ALIGNMENT.md).

[Download the public evidence ZIP](KIEL_HANDOFF_EVIDENCE.zip?raw=true).
Provider records are redacted source-faithful derivatives with unedited visible
outputs; private reasoning/account fields and proprietary logic remain excluded.
[EVIDENCE_COVERAGE.json](EVIDENCE_COVERAGE.json) lists verified data and the
counterpart artifacts still needed for a matched four-arm comparison.
