# Baseline difference and matching plan

## Established facts

- Local raw native-FC baseline: **961/1,390 (69.14%)**.
- Local ARM-A: **1,007/1,390 (72.45%), C=46, B=0** against that exact baseline.
- Kiel's delivered Oct 8 manifest: **1,085/1,390 (78.06%)** for both his Baseline
  and ARM-B.
- The case IDs and seven category counts match. Kiel's attachment has outcome
  flags and governance fields, not ungraded raw model outputs or full requests.
  Identical input bytes and request conditions are therefore not yet established.
- The local baseline was separately generated, not copied from Kiel's answer
  sheet. The difference is already present **before** the local ARM-A treatment;
  it cannot be attributed to RCC improving or degrading that baseline.

## Strongest supported explanation — not a confirmed cause

All seven Oct 8 baseline percentages match the **Prompt** column in Kiel's
Oct 3 Prompt-versus-FC message. Local execution used native function calling
through the Responses API. This makes a Prompt/FC or associated handler/output-
representation mismatch the leading hypothesis. The delivered ARM-B manifest
alone does not identify which generation handler actually ran. This document
asks for confirmation; it does not assert that Kiel necessarily ran Prompt.

| Category | Local native baseline | Kiel Oct 8 baseline | Kiel Oct 3 Prompt | Kiel Oct 3 FC |
|---|---:|---:|---:|---:|
| Simple Python | 72.75% | 89.25% | 89.25% | 74.50% |
| Multiple | 65.50% | 89.00% | 89.00% | 70.50% |
| Parallel | 71.00% | 85.00% | 85.00% | 76.00% |
| Parallel Multiple | 66.00% | 78.00% | 78.00% | 66.50% |
| Simple JavaScript | 26.00% | 66.00% | 66.00% | 38.00% |
| Simple Java | 32.00% | 56.00% | 56.00% | 47.00% |
| Irrelevance | 91.67% | 56.25% | 56.25% | 91.25% |

The Oct 3 message reported 1,378 Prompt cases and 1,390 FC cases. Its reported
aggregate must not be silently substituted for the Oct 8 1,390-case aggregate;
the row/count transition also needs clarification. Even his earlier FC column
is not identical to the separately generated local baseline. Request settings,
serialization, evaluator normalization and stochastic generation remain
additional possible contributors, not proven causes.

### Actual local settings are now available

`baseline_requests.jsonl` is the as-sent request body. Effort, temperature,
tool choice and parallel-tool setting were not explicitly sent. The responses
report **medium** effort, temperature **1.0**, `auto` tool choice and parallel
calls enabled in all 1,390 rows. Requested versus response-reported settings
are separated in `execution_config.json`; reported values are not claimed to
expose hidden compute or every provider-side condition. Two incomplete
responses are retained, not removed or silently regenerated.

## Minimum data requested from Kiel

1. Ungraded case-level baseline outputs and original visible provider responses
   for the exact answer sheet that scored 1,085.
2. Exact per-case request bodies, including model snapshot, endpoint, prompt
   roles, offered tool schema, Prompt/FC mode and handler identity.
3. Case/ input hashes and per-category counts, including how the 1,378-to-1,390
   transition was handled.
4. Explicitly requested and observed provider settings: reasoning, token cap,
   temperature/top-p, tool choice, parallel calls, seed if exposed, retries and
   incomplete-response treatment. Unknown settings should remain unknown.
5. Scorer version/commit, output projection and type conversion, answer-shape
   normalization and relevance handling. Aggregate accuracy alone is insufficient.
6. ARM-B's pre-score I/O and decision timestamps. Correctness flags must never
   become inputs to ARM-C adoption.

No private source code or authentication key is needed to supply these items.

## Cheapest valid condition-matching route

For the current **post-generation** experiment, agree on one immutable,
ungraded baseline answer sheet. Use the same exact sheet as the shared model
output for Baseline, ARM-A and ARM-B, then run ARM-C through the agreed actual
composition interface. Select the common sheet before grading/comparing it;
do not choose the sheet with the better score. Reprocessing cached outputs
avoids new stochastic model calls and unnecessary cost.

If the intended treatment instead changes model generation itself, preregister
that as a separate experiment: identical source cases, snapshot, endpoint,
non-treatment request settings, candidate budget, retry policy and scorer.
Log generation, usage and final-lock separately. Setting the same seed where
available does not guarantee identical provider execution; disclose that limit.

For ARM-C, specify stage order, native/checker representation and fallback
semantics before execution. Freeze every final result before scoring. Do not
compute ARM-C by taking row-wise score winners or averaging ARM-A/ARM-B scores.

**Current comparison status:** the local +46/zero-regression result is paired
with its own baseline. A matched four-arm comparison and the exact cause of
Kiel's different baseline remain open pending his raw/config artifacts.

## Source coverage

The comparison uses directly inspected Oct 3/Oct 8 messages, Kiel's original
Oct 8 attachment, and hash-checked local generation artifacts. The original
attachment SHA-256 is recorded in `baseline_comparison.json`. Private mail,
Evolve Edge gate internals and correspondence identifiers are not published.
