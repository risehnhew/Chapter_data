# Data Preparation Report

## Inputs

- Main input: `data/maggie/unified.csv`
- Paraphrase input: `data/maggie/paraphrases.csv`
- Raw dataset downloading was not used.

## Summary

- Rows: 16429
- Unique `(source, lang, expression)` groups: 2686
- Unique expressions: 1122
- Paraphrase coverage: 99.99%
- Missing head rows: 14581
- Missing modifier rows: 14581

## Rows By Source

| value | rows |
| --- | ---: |
| semeval_a | 7712 |
| semeval_b | 4263 |
| dice | 2066 |
| ncimp | 1377 |
| nc | 550 |
| nctti | 461 |

## Rows By Language

| value | rows |
| --- | ---: |
| eng | 11219 |
| pt | 4317 |
| gl | 713 |
| fr | 180 |

## Label Distribution

| value | rows |
| --- | ---: |
| UNKNOWN | 6651 |
| LITERAL | 5452 |
| IDIOMATIC | 4326 |

## Contribution Labels

| value | rows |
| --- | ---: |
| UNKNOWN | 16429 |

## Compositionality Bins

| value | rows |
| --- | ---: |
| unknown | 15419 |
| high | 382 |
| low | 351 |
| mid | 277 |

## Warnings

- Ignored non-input paraphrase metadata columns: input_tokens_gpt55pro20260423, input_tokens_gpt5nano20250807, output_tokens_gpt55pro20260423, output_tokens_gpt5nano20250807, reasoning1_gpt55pro20260423, reasoning1_gpt5nano20250807, reasoning_tokens_gpt55pro20260423, reasoning_tokens_gpt5nano20250807, total_tokens_gpt55pro20260423, total_tokens_gpt5nano20250807
- No head/modifier contribution score columns detected; contribution_label is heuristic UNKNOWN.


## Split Generation

Split column: `split_701020`

Split source: generated grouped 70/10/20 split. `original_split` is preserved separately.

### Overall Split Counts

| split_701020 | rows |
| --- | --- |
| dev | 1639 |
| test | 3313 |
| train | 11477 |

### Split Counts By Source

| source | split_701020 | rows |
| --- | --- | --- |
| dice | dev | 202 |
| dice | test | 418 |
| dice | train | 1446 |
| nc | dev | 55 |
| nc | test | 110 |
| nc | train | 385 |
| ncimp | dev | 138 |
| ncimp | test | 276 |
| ncimp | train | 963 |
| nctti | dev | 46 |
| nctti | test | 93 |
| nctti | train | 322 |
| semeval_a | dev | 760 |
| semeval_a | test | 1523 |
| semeval_a | train | 5429 |
| semeval_b | dev | 438 |
| semeval_b | test | 893 |
| semeval_b | train | 2932 |

### Split Counts By Language

| lang | split_701020 | rows |
| --- | --- | --- |
| eng | dev | 1106 |
| eng | test | 2223 |
| eng | train | 7890 |
| fr | dev | 18 |
| fr | test | 35 |
| fr | train | 127 |
| gl | dev | 72 |
| gl | test | 149 |
| gl | train | 492 |
| pt | dev | 443 |
| pt | test | 906 |
| pt | train | 2968 |

### Split Counts By Label

| label_norm | split_701020 | rows |
| --- | --- | --- |
| IDIOMATIC | dev | 401 |
| IDIOMATIC | test | 868 |
| IDIOMATIC | train | 3057 |
| LITERAL | dev | 561 |
| LITERAL | test | 1073 |
| LITERAL | train | 3818 |
| UNKNOWN | dev | 677 |
| UNKNOWN | test | 1372 |
| UNKNOWN | train | 4602 |

### Split Warnings

- None.
