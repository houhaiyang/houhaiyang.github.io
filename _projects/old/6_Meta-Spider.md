---
layout: page
title: Meta-Spider
description: A powerful method for constructing sample-individual networks via outlier-aware clustering, indirect interaction exclusion, and linear interpolation.
img: https://raw.githubusercontent.com/houhaiyang/Meta-Spider/main/docs/MSlogo2.png
importance: 6
category: tools
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/Meta-Spider" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

**Meta-Spider** is a Python package for estimating **sample-specific networks** from omics data.
It combines outlier-aware clustering, partial correlation-based indirect interaction exclusion,
and linear interpolation to build personalized interaction networks at the individual sample level.

## Key Features

- **Outlier-aware clustering** — builds a core sample set and assigns category labels to each sample
- **Indirect interaction exclusion** — retains only direct feature–feature interactions via partial correlation
- **Linear interpolation** — estimates a continuous, sample-specific network for each individual

## Usage

```python
from metaspider import metaspider

metaspider(
    data=exp_df,
    outdir='result',
    N_cluster=50,
    th_occ_feature=0.5,
    th_occ_sample=0.50,
    ptcc_corr_th=0.35,
    top=5,
    n_jobs=16,
    quantile=0.25
)
```

## Input Format

A sample × feature expression matrix (rows = samples, columns = nodes/genes):

| | node_1 | node_2 | ... | node_n |
|---|---|---|---|---|
| sample_1 | 0.01 | 0.009 | ... | 0.02 |
| sample_2 | 0.0002 | 0.0003 | ... | 0.0004 |

## Installation

```bash
pip install dist/metaspider-0.9.3-py3-none-any.whl
```