# Current handoff to Kiel — shared native-FC 995 baseline

The latest request is covered by the [baseline-native-fc-995-20261010](baseline-native-fc-995-20261010/) packet:

1. [Original file actually graded](baseline-native-fc-995-20261010/locked_outputs.jsonl): 1,390 unchanged raw outputs, not just scores.
2. [Case-level input/output pairs](baseline-native-fc-995-20261010/input_output_pairs.jsonl), [actual as-sent requests](baseline-native-fc-995-20261010/requests.jsonl), [raw inputs](baseline-native-fc-995-20261010/raw_inputs.jsonl), [prepared inputs](baseline-native-fc-995-20261010/prepared_inputs.jsonl) and [execution configuration](baseline-native-fc-995-20261010/execution_config.json).
3. [Written case-set confirmation](baseline-native-fc-995-20261010/FROZEN_CASE_SET.md), [case IDs](baseline-native-fc-995-20261010/case_ids.txt), [case/hash manifest](baseline-native-fc-995-20261010/case_manifest.jsonl) and [BFCL snapshot hashes](baseline-native-fc-995-20261010/dataset_manifest.json).
4. [Lossless BFCL id/result projection](baseline-native-fc-995-20261010/bfcl_outputs.jsonl), [format contract](baseline-native-fc-995-20261010/INPUT_CONTRACT.md), [visible provider outputs](baseline-native-fc-995-20261010/provider_outputs.jsonl), [usage/latency](baseline-native-fc-995-20261010/usage_latency.jsonl) and [pre-grading lock receipt](baseline-native-fc-995-20261010/freeze_receipt.json).
5. [Download the complete public data/document ZIP](baseline-native-fc-995-20261010/KIEL_NATIVE_FC_995_HANDOFF.zip?raw=true) and [checksums](baseline-native-fc-995-20261010/SHA256SUMS.txt).

Use this exact frozen sheet for ARM-B; do not regenerate model answers. The raw answers contain 996 call-list outputs and 394 preserved text/no-call strings. The input contract explains these without altering them.

Kiel confirmed on October 10 that his 1,085/1,390 run used Prompt mode. On October 11 he agreed to the native-FC 995/1,390 sheet as the shared baseline. The old mode questions below are historical and superseded; no need to ask them again. Private logic, credentials and hidden reasoning are excluded from the new packet.

No ARM-A result against the 995 sheet is included. The existing ARM-A interface evidence below remains available as a separate earlier run for interface inspection, not a matched current four-arm comparison.

---

## Historical ARM-A handoff — earlier 961 baseline (mode questions superseded)

# Kiel handoff — ARM-A function-calling evidence

Current ARM-A: **961 → 1,007 / 1,390; 46 improvements, zero regressions**.
This is post-development gold-blind semantic selection replay using the original
local baseline. All finals were locked before scoring. It is not an already
matched comparison against the 1,085-case-correct ARM-B baseline.

## Read in this order

1. [Output contract](OUTPUT_CONTRACT.md): actual call/message union, native versus
   Java/JavaScript checker representation, and the ARM-C boundary.
2. [Execution configuration](execution_config.json): actual request settings,
   provider-reported defaults, original baseline usage/cost/latency and the
   deterministic ARM-A condition.
3. [Baseline alignment](BASELINE_ALIGNMENT.md): established difference, leading
   Prompt/FC hypothesis, exact missing counterpart data and matching plan.
4. [Evidence coverage](EVIDENCE_COVERAGE.json): verified public data, deliberately
   withheld private material, non-applicable artifacts and external dependencies.

## Case-level files

- [Final answers](answers.jsonl): 1,390 baseline/final pairs.
- [Native/final ARM-A I-O](arm_a_output_envelopes.jsonl): actual emitted plans and
  source/adoption status; no private verifier trace.
- [Post-lock grades](grades.jsonl): outcome flags, for scoring only.
- [Frozen inputs](input_cases.jsonl): exact questions and offered functions.
- [As-sent baseline requests](baseline_requests.jsonl): no auth headers.
- [Provider response projections](baseline_provider_responses.jsonl): unedited
  visible outputs plus settings/status/usage; hidden reasoning/account fields
  withheld under [publication policy](RAW_PUBLICATION_POLICY.json).
- [Per-call usage/latency](baseline_usage_latency.jsonl): original measurements,
  not inferred ARM-A processing times.

Large JSONL files may require GitHub's **Raw/Download** option.
`SHA256SUMS.txt`, `manifest.json`, `receipt.json` and `final_lock.json` identify
all files and the pre-score final answer lock. The public handoff ZIP contains
only these evidence documents/data, not private implementation.

## Specific alignment questions

- Does the Oct 8 Baseline/ARM-B sheet use Prompt or native FC? All seven category
  percentages match the Oct 3 Prompt column; please confirm using actual requests.
- Can the ungraded 1,085 baseline sheet, request/config artifacts and input hashes
  be shared so both sides can lock one common baseline?
- Given `native_output` and `final_output`, which representation and stage order
  does Section 7.3 need for faithful BFCL ARM-C composition?
- What pre-decision state does Evolve Edge require, and what is returned on
  ADOPT/HOLD/REJECT? Neither post-lock grades nor score deltas may drive adoption.

No request is made here for Evolve Edge's private source or credentials, and no
RCC private source or prompts are disclosed. The data describes the integration
surface without reconstructing either system's internal logic.
