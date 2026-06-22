# Chapter Data

Current default dataset and embeddings are based on Maggie's preprocessed files.

## Data

- `data/maggie/unified.csv`: Maggie's unified input table.
- `data/maggie/paraphrases.csv`: Maggie's paraphrase candidate table. Reasoning and token-count columns are ignored by the embedding pipeline.
- `data/processed/unified_enriched.csv`: normalized labels, canonical paraphrases, compositionality bins, and contribution labels.
- `data/processed/all_with_splits.csv`: generated grouped 70/10/20 split in `split_701020`.
- `data/processed/unique_texts_for_embedding.csv`: unique isolated text table used for embedding extraction.

## Embeddings

Embeddings are under `embeddings/xlm-roberta-base/`.

| file | bytes | sha256 | sharded |
| --- | ---: | --- | --- |
| `unique_text_embeddings.npz` | 35500973 | `c2ef242ef3ceddffbf6d73dd27fed497491bc22952b9b52f3b3081308d99c44b` | no |
| `row_embeddings.npz` | 32568341 | `9f3b2a8cbec675fc14037e69719d6b43beee039d0fb76ee70c83690312c1b6e2` | no |

If an `.npz` file is sharded, reconstruct it in the embedding directory with:

```bash
cat row_embeddings.npz.part-* > row_embeddings.npz
sha256sum -c row_embeddings.npz.sha256
cat unique_text_embeddings.npz.part-* > unique_text_embeddings.npz
sha256sum -c unique_text_embeddings.npz.sha256
```

If the unsharded `.npz` file is present directly, no reconstruction is needed for that file.

## Reports

- `reports/data_preparation_report.md`
- `reports/embedding_report.md`

The older raw-dataset rebuild outputs are no longer the default dataset in this repository.

<!-- additional-embedding-models:start -->
## Additional Embedding Models

- `embeddings/BAAI-bge-m3/`: `BAAI/bge-m3` dense embeddings (1024 dimensions, pooling `cls`, L2 normalized `True`).
<!-- additional-embedding-models:end -->
