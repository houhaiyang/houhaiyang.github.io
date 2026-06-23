---
layout: page
title: ESM-C-Seq-Embedding
description: A lightweight pipeline for extracting CLS-level sequence embeddings from ESM-C 600M for large-scale protein datasets.
img: https://raw.githubusercontent.com/houhaiyang/RepGene/main/docs/logo/RepGeneLOGO-1.png
importance: 4
category: tools
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/ESM-C-Seq-Embedding" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

**ESM-C-Seq-Embedding** is a practical pipeline for generating protein sequence-level embeddings
using the **ESM-C 600M** foundation model. It extracts the CLS token as a compact fixed-length
representation for each protein sequence, enabling efficient downstream analysis such as PPI
prediction and functional annotation.

For a protein sequence of length L, ESM-C outputs a tensor of shape (L+2) × d (including CLS
and EOS tokens). This pipeline extracts only the **CLS token** as the sequence-level embedding.

## Pipeline

1. **`faa2emb_CLS.py`** — batch-generates per-sequence `.csv.gz` embedding files from a `.faa` input
2. **`merge_emb.py`** — merges all per-sequence embeddings into a single compressed matrix

## Usage

```bash
# Step 1: Generate embeddings
python faa2emb_CLS.py --input test_proteins.faa --outdir embeddings/test/

# Step 2: Merge
python merge_emb.py --input test_proteins.faa \
  --embeddings_dir ./embeddings/test/ \
  --output ./embeddings/test_proteins_merged_embeddings.csv.gz
```

## Requirements

- Python 3.10, PyTorch 2.4.1, CUDA 11.8
- ESM-C 600M weights (`esmc-600m-2024-12`)