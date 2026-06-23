---
layout: page
title: RepGene
description: You Only Need One Gene Representation — a unified gene embedding framework for single-cell foundation models.
img: https://raw.githubusercontent.com/houhaiyang/RepGene/main/docs/logo/RepGeneLOGO-1.png
importance: 1
category: research
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/RepGene" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
  <a href="https://www.biorxiv.org/content/10.64898/2026.06.11.731512v1" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#b31b1b; color:white;">
    📄 Preprint
  </a>
</div>

**RepGene** is a unified gene representation framework designed for single-cell omics analysis.
Built on the principle of *"You Only Need One Gene Representation"*, it provides compact,
transferable gene embeddings that can power diverse downstream tasks across single-cell foundation models (scFMs).

## Model Architecture

<div class="text-center">
  <img src="https://raw.githubusercontent.com/houhaiyang/RepGene/main/docs/Repgene-sketch-map.png"
       alt="RepGene Architecture"
       style="max-width:100%; border-radius:6px;" />
  <p class="caption mt-1" style="font-size:0.85em; color:gray;">RepGene model architecture and data flow</p>
</div>

## Key Features

- **Unified representation**: a single gene embedding space shared across cell types and datasets
- **Scalable pre-training**: developed on large-scale single-cell transcriptomics corpora
- **Flexible downstream use**: supports cell-type annotation, gene function prediction, and cross-dataset transfer
- **Lightweight inference**: runs efficiently on consumer-grade GPUs (tested on RTX 4070 Super)

## Citation

If you use RepGene, please cite our preprint:

> Hou H. et al. *RepGene: You Only Need One Gene Representation.* bioRxiv (2026).
> doi: [10.64898/2026.06.11.731512](https://doi.org/10.64898/2026.06.11.731512)

