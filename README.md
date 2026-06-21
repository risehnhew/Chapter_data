# Chapter Data

Processed datasets and split files for the Chapter V noun-compound and idiom embedding pipeline.

## Contents

- `data/processed/all_datasets_unified.csv`: normalized unified table before generated splits.
- `data/processed/all_datasets_unified.parquet`: parquet copy of the normalized unified table.
- `data/processed/all_datasets_unified_with_splits.csv`: normalized table with generated `split` assignments.
- `data/splits/`: per-dataset and all-dataset train/dev/test CSV files.
- `reports/`: download, normalization, split, inventory, and validation reports.

## Dataset Counts

| dataset | rows | train | dev | test |
| --- | ---: | ---: | ---: | ---: |
| nc | 550 | 385 | 55 | 110 |
| nctti_ncs | 1,383 | 968 | 138 | 277 |
| semeval2022_task2 | 26,965 | 18,875 | 2,696 | 5,394 |
| ncimp | 1,844 | 1,290 | 184 | 370 |
| dice | 2,066 | 1,446 | 206 | 414 |
| all | 32,808 | 22,964 | 3,279 | 6,565 |

## Notes

- AdMIRe is intentionally excluded.
- Raw source data is not included in this repository.
- Full XLM-R embeddings are not included here yet. The GPU extraction job was submitted separately and will write to `embeddings/xlm-roberta-base/all/` in the pipeline workspace when it completes.
- The latest validation report is in `reports/final_validation_report.md`.
