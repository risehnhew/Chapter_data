# Normalization Report

## Assumptions

- NC rows come from filtered averaged annotation files.
- NC example sentences are joined from compounds-list files when possible.
- Generic parsers keep rows with any usable expression, target span, or sentence.
- Binary labels are conservative; uncertain derivations remain `UNKNOWN`.
- NC LOW/HIGH compositionality bins derive `IDIOMATIC`/`LITERAL` labels and are marked in notes.
- Head/mod fields are marked explicit only when source columns exist; inferred components set `has_head_mod=false`.

## Row Counts

| dataset | rows |
| --- | ---: |
| nc | 550 |
| nctti_ncs | 1383 |
| semeval2022_task2 | 26965 |
| ncimp | 1844 |
| dice | 2066 |

## Labels

dataset            label_binary
dice               IDIOMATIC        1033
                   LITERAL          1033
nc                 IDIOMATIC         183
                   LITERAL           183
                   UNKNOWN           184
ncimp              UNKNOWN          1844
nctti_ncs          UNKNOWN          1383
semeval2022_task2  UNKNOWN         26965
