---
layout: page
title: PPI-Sifter
description: Residue-level interpretable protein–protein interaction prediction via bidirectional cross-attention on frozen ESM-C embeddings.
img: https://raw.githubusercontent.com/houhaiyang/PPI-Sifter/main/docs/PPI-Sifter-Model-Architecture/PPI-Sifter-Model-Architecture.png
importance: 3
category: research
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/PPI-Sifter" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

**PPI-Sifter** is a proteome-scale, residue-level interpretable protein–protein interaction (PPI) predictor.
It encodes each residue using a **frozen ESM-C 600M** foundation model and models inter-protein residue
dependencies through a **bidirectional cross-attention** mechanism, predicting whether two proteins
physically interact while providing residue-level interpretability.

## Model Architecture

<div class="text-center">
  <img src="https://raw.githubusercontent.com/houhaiyang/PPI-Sifter/main/docs/PPI-Sifter-Model-Architecture/PPI-Sifter-Model-Architecture.png"
       alt="PPI-Sifter Model Architecture"
       style="max-width:100%; border-radius:6px;" />
  <p class="caption mt-1" style="font-size:0.85em; color:gray;">PPI-Sifter model architecture</p>
</div>

## Key Features

- **Frozen ESM-C 600M backbone** — only ~3M classification parameters trained
- **Bidirectional cross-attention** — protein A attends to B *and* B attends to A symmetrically
- **Residue-level attention map** — outputs an L_A × L_B matrix of binding-site candidates
- **Protein-disjoint evaluation** — rigorously benchmarked to prevent data leakage

## Performance (BioGRID, protein-disjoint split, 58,096 pairs)

| Metric | Value |
|--------|-------|
| AUPRC  | **0.8617** |
| AUROC  | 0.8810 |
| F1     | 0.8162 |
| MCC    | 0.6059 |