# XLM-R Embeddings

The full `vectors.npz` file is stored as GitHub-friendly shards when it exceeds the normal file-size limit.

Reconstruct it from this directory with:

```bash
cat vectors.npz.part-* > vectors.npz
sha256sum -c vectors.npz.sha256
```

If `vectors.npz` is present directly, no reconstruction is needed.
