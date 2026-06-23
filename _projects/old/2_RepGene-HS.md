---
layout: page
title: RepGene-HS
description: You Only Need One Gene Representation — high-speed variant of RepGene optimized for efficient single-cell gene embedding.
img: https://raw.githubusercontent.com/houhaiyang/RepGene-HS/main/docs/logo/RepGene-LOGO-3.png
importance: 2
category: research
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/RepGene-HS" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

**RepGene-HS** is a high-speed variant of [RepGene](https://github.com/houhaiyang/RepGene),
designed to deliver unified gene representations for single-cell omics with improved inference efficiency.
Following the same philosophy of *"You Only Need One Gene Representation"*, RepGene-HS targets
scalable deployment scenarios across large single-cell datasets.

## Model Architecture

<div class="text-center">
  <img src="https://raw.githubusercontent.com/houhaiyang/RepGene-HS/main/docs/Repgene-model-sketch-map/Repgene-model-sketch-map-2025-11-1.png"
       alt="RepGene-HS Model Architecture"
       style="max-width:100%; border-radius:6px;" />
  <p class="caption mt-1" style="font-size:0.85em; color:gray;">RepGene-HS model architecture and data flow</p>
</div>

## Key Features

- **High-speed inference**: optimized architecture for faster embedding extraction
- **Unified gene space**: same representation paradigm as RepGene, fully compatible
- **Lightweight footprint**: efficient on consumer-grade GPUs (RTX 4070 Super 12GB)
- **Easy integration**: drop-in compatible with downstream scFM pipelines

## Requirements

- Python 3.11, PyTorch 2.1.0, CUDA 12.1, NVIDIA GPU
- See [`requirements.txt`](https://github.com/houhaiyang/RepGene-HS/blob/main/requirements.txt) for full dependencies
