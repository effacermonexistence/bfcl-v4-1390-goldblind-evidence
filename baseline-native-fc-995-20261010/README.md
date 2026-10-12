# Shared native-FC baseline — 995/1,390 (71.58%)

Run: `bfcl1390-baseline-official-default-20261010`. Model: `gpt-5-nano-2025-08-07`, Responses API/native FC; official BFCL default language preprocessing.

**This directory is the 995 raw baseline only. Repository-root 961→1007 ARM-A results remain an earlier, separate run. No new ARM-A result on 995 is claimed.**

## Start here

1. [Exact frozen answer sheet](locked_outputs.jsonl) — 1,390 rows, original bytes/SHA preserved.
2. [Case-level input/output pairs](input_output_pairs.jsonl) — what ARM-B should consume, not scores.
3. [Written frozen-case confirmation](FROZEN_CASE_SET.md), [explicit case IDs](case_ids.txt), [case/hash manifest](case_manifest.jsonl) and [dataset snapshot hashes](dataset_manifest.json).
4. [Input/output contract](INPUT_CONTRACT.md), [as-sent requests](requests.jsonl), [prepared inputs](prepared_inputs.jsonl) and [execution settings](execution_config.json).
5. [BFCL id/result projection](bfcl_outputs.jsonl), or the seven files in `bfcl_results/`.
6. [Visible provider response projections](provider_outputs.jsonl), [usage/latency](usage_latency.jsonl) and [pre-grading lock evidence](freeze_receipt.json).

[Download the data/document handoff ZIP](KIEL_NATIVE_FC_995_HANDOFF.zip?raw=true). Check [SHA256SUMS.txt](SHA256SUMS.txt) and the ZIP's adjacent SHA-256 file. Large JSONL files may need Raw/Download.

The whole answer sheet was locked at `2026-10-10T11:13:32.917298+00:00`, before the first scoring attempt at `2026-10-10T11:13:46.827729+00:00`. All 1,390 provider responses completed. These are preserved original outputs, not a new model run. The cohort had prior development exposure; the source proof-mode label is retained in execution_config.json.

No gold answers, row-level grades, private implementation or credentials are included. Provider envelopes are redacted derivatives, not unredacted byte-original responses. Original locked_outputs.jsonl/request/input files remain byte-identical. See [publication policy](PUBLICATION_POLICY.json) and [request coverage](REQUIREMENTS_COVERAGE.json).
