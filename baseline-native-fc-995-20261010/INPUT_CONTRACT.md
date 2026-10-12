# Frozen native-FC baseline input contract

`locked_outputs.jsonl` is the exact file the 995 baseline grader read. Its SHA-256 is in `freeze_receipt.json`; it is not regenerated or rewritten. Each row has `case_id`, `category`, `baseline_output`, and the original `locked_utc`.

`input_output_pairs.jsonl` pairs each unchanged output with the original BFCL input. Join `prepared_inputs.jsonl` and `requests.jsonl` by the same ID to inspect the actual language-prepared generation input and sent tool schemas. Original/scorer schemas and provider-request schemas are distinct; Java/JavaScript preparation can use string/literal representations.

`baseline_output` is a union: 996 rows are native call lists, 394 rows are preserved text/no-call strings. A call-list element has one function-name key and its raw JSON argument string as the value. Preserve names, argument strings, call count/order, and text exactly. Do not convert every text string to an empty call list or infer calls from text. Function plans were not executed.

`bfcl_outputs.jsonl` and seven `bfcl_results/*_result.json` files provide the official BFCL per-case `id`/`result` field shape. They are lossless field projections of the original answers, not new provider generations and not the file originally used for grading. `provider_outputs.jsonl` includes the unaltered visible provider function-call/message objects; hidden reasoning/account data is withheld.

Run ARM-B on these frozen outputs, not by calling the model again. A new call would not be this identical answer sheet. Record each gate decision and its returned output, preserving the original baseline separately. Do not feed gold, per-case grades or score deltas into adoption. The packet does not expose either party's private governance logic or certify the ARM-B adapter as already executed.

The repository-root ARM-A files use the earlier 961 baseline. They are not paired with this 995 sheet.
