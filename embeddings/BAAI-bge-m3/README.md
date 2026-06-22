# BAAI/bge-m3 Embeddings

Dense embeddings generated from Maggie's preprocessed chapter data.

## Configuration

- Model: `BAAI/bge-m3`
- Pooling: `cls`
- L2 normalized: `True`
- Max token length: `128`
- Rows: `16429`
- Unique texts: `19488`
- Embedding dimension: `1024`

## Files

- `unique_text_metadata.csv`
- `row_embedding_metadata.csv`
- `embedding_config.json`
- `embedding_report.md` when validation was run before upload

| file | bytes | sha256 | sharded |
| --- | ---: | --- | --- |
| `unique_text_embeddings.npz` | 73677509 | `7f41ceefe0c7d54aa680a35505cc90e85dc6c43135fe3ee9f28b327ea25f628a` | yes |
| `row_embeddings.npz` | 62030315 | `a6d7f3c094300b4bb411c9bb6c5c6edc1a58cb054dbb11dd8e747c2b2d569444` | yes |

If an `.npz` file is sharded, reconstruct it in this directory with:

```bash
cat row_embeddings.npz.part-* > row_embeddings.npz
sha256sum -c row_embeddings.npz.sha256
cat unique_text_embeddings.npz.part-* > unique_text_embeddings.npz
sha256sum -c unique_text_embeddings.npz.sha256
```
