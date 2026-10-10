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
