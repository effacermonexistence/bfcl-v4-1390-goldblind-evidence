# Written confirmation of the common frozen case set

**OmarAGI confirms that the common native-FC baseline uses exactly the 1,390 case IDs, in order, in `case_ids.txt` (SHA-256 `4baf2150174ef3343c32b2fe113f2f4466c18d5b3c4fef2bae99ffdb3cdf217c`), with original inputs in `raw_inputs.jsonl` (SHA-256 `265c9f3c325594a997b84469059f56acf70a35acf77fce7eb30265cf0335b960`), from BFCL V4/Gorilla commit `f7cf7359b7ac615a0b294831c5ba2bc95ee4a000`. No cases are added, removed, swapped, or replaced by this handoff.**

| Category | Cases |
|---|---:|
| irrelevance | 240 |
| multiple | 200 |
| parallel_multiple | 200 |
| parallel | 200 |
| simple_java | 100 |
| simple_javascript | 50 |
| simple_python | 400 |

Only the seven frozen single-turn non-live categories are included; live, agentic and multi-turn categories are not part of this 1,390-case set. Official default language preprocessing was applied before native-FC generation. The question IDs and original-input bytes were frozen by the run contract on `2026-10-10T10:59:36.511055+00:00`.

This written note, the explicit ID list, paired files and public projections were assembled later from the retained originals; their new file-creation dates are not backdated. `dataset_manifest.json` lists hashes for the seven original frozen upstream files.

For reciprocal written acknowledgement: “Agreed: our common case set is the 1,390 IDs in case_ids.txt, SHA-256 `4baf2150174ef3343c32b2fe113f2f4466c18d5b3c4fef2bae99ffdb3cdf217c`, and the common raw answer sheet is locked_outputs.jsonl, SHA-256 `4d27e611d132292d59e8121273d99ca0dc8a05b883ff5a2c4d55dd4b49fd3862`.”
