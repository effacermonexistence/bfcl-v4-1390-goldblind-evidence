# BFCL V4 shared native-FC baseline — 995/1,390 (71.58%)

The current common baseline agreed in Kiel's October 11 correspondence is available in [baseline-native-fc-995-20261010](baseline-native-fc-995-20261010/).

- [Exact frozen raw answer sheet](baseline-native-fc-995-20261010/locked_outputs.jsonl) and [1,390 case-level input/output pairs](baseline-native-fc-995-20261010/input_output_pairs.jsonl)
- [Written frozen-case-set confirmation](baseline-native-fc-995-20261010/FROZEN_CASE_SET.md), [case IDs](baseline-native-fc-995-20261010/case_ids.txt) and [snapshot hashes](baseline-native-fc-995-20261010/dataset_manifest.json)
- [Request settings and freeze evidence](baseline-native-fc-995-20261010/execution_config.json), [input contract](baseline-native-fc-995-20261010/INPUT_CONTRACT.md) and [downloadable handoff ZIP](baseline-native-fc-995-20261010/KIEL_NATIVE_FC_995_HANDOFF.zip?raw=true)

This new directory preserves the original 995 answer sheet byte-for-byte. No model rerun or new ARM-A run was performed for this handoff. The repository-root 961 → 1,007 ARM-A packet below is a separate earlier run; do not pair it with the 995 baseline.

Historical root checksums and the root handoff ZIP describe the [earlier ff2ea3f snapshot](https://github.com/effacermonexistence/bfcl-v4-1390-goldblind-evidence/tree/ff2ea3ff11f700c2943e328bebf9e4e01c4c640a); root navigation documents have since been extended. Verify the new 995 packet using its own [SHA256SUMS.txt](baseline-native-fc-995-20261010/SHA256SUMS.txt). Historical data and ZIP bytes are unchanged.

---

## Historical ARM-A evidence — earlier 961 baseline

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
