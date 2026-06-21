# Split Report

Random seed: 42

| dataset | rows | train | dev | test | strategy | leakage_note |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| dice | 2066 | 1446 | 206 | 414 | stratify_key | possible expression leakage |
| nc | 550 | 385 | 55 | 110 | lang_label_binary_label_contribution |  |
| ncimp | 1844 | 1290 | 184 | 370 | stratify_key | possible expression leakage |
| nctti_ncs | 1383 | 968 | 138 | 277 | stratify_key | possible expression leakage |
| semeval2022_task2 | 26965 | 18875 | 2696 | 5394 | stratify_key | possible expression leakage |

## Strategy Attempts

```json
[
  {
    "dataset": "dice",
    "rows": 2066,
    "strategy": "stratify_key",
    "attempts": [
      {
        "strategy": "stratify_key",
        "status": "ok"
      }
    ],
    "train": 1446,
    "dev": 206,
    "test": 414,
    "unique_row_group_id": 402,
    "possible_expression_leakage": true
  },
  {
    "dataset": "nc",
    "rows": 550,
    "strategy": "lang_label_binary_label_contribution",
    "attempts": [
      {
        "strategy": "stratify_key",
        "status": "failed",
        "error": "ValueError('full stratify_key has strata with fewer than 3 rows')"
      },
      {
        "strategy": "lang_label_binary_label_contribution",
        "status": "ok"
      }
    ],
    "train": 385,
    "dev": 55,
    "test": 110,
    "unique_row_group_id": 550,
    "possible_expression_leakage": false
  },
  {
    "dataset": "ncimp",
    "rows": 1844,
    "strategy": "stratify_key",
    "attempts": [
      {
        "strategy": "stratify_key",
        "status": "ok"
      }
    ],
    "train": 1290,
    "dev": 184,
    "test": 370,
    "unique_row_group_id": 461,
    "possible_expression_leakage": true
  },
  {
    "dataset": "nctti_ncs",
    "rows": 1383,
    "strategy": "stratify_key",
    "attempts": [
      {
        "strategy": "stratify_key",
        "status": "ok"
      }
    ],
    "train": 968,
    "dev": 138,
    "test": 277,
    "unique_row_group_id": 461,
    "possible_expression_leakage": true
  },
  {
    "dataset": "semeval2022_task2",
    "rows": 26965,
    "strategy": "stratify_key",
    "attempts": [
      {
        "strategy": "stratify_key",
        "status": "ok"
      }
    ],
    "train": 18875,
    "dev": 2696,
    "test": 5394,
    "unique_row_group_id": 489,
    "possible_expression_leakage": true
  }
]
```
