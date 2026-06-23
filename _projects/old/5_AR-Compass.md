---
layout: page
title: AR-Compass
description: Navigating antibiotic resistance in the sequences ocean — a three-stage deep learning pipeline for ARG identification and classification.
img: https://raw.githubusercontent.com/houhaiyang/AR-Compass/main/docs/logo-05-1.png
importance: 5
category: research
related_publications: false
---

<div class="text-center mb-3">
  <a href="https://github.com/houhaiyang/AR-Compass" class="btn btn-sm z-depth-0" role="button" target="_blank"
     style="font-size:12px; background-color:#24292e; color:white;">
    <i class="fab fa-github"></i> GitHub
  </a>
</div>

**AR-Compass** is a three-stage deep learning pipeline for antibiotic resistance gene (ARG)
identification and classification from raw protein sequences.
Following the motto *"Navigating Antibiotic Resistance in the Sequences Ocean"*,
it progressively narrows prediction from binary ARG detection to fine-grained subclass assignment.

## Workflow

<div class="text-center">
  <img src="https://raw.githubusercontent.com/houhaiyang/AR-Compass/main/docs/FlowChart.png"
       alt="AR-Compass Workflow"
       style="max-width:100%; border-radius:6px;" />
  <p class="caption mt-1" style="font-size:0.85em; color:gray;">AR-Compass three-stage prediction pipeline</p>
</div>

## Three-Stage Design

| Stage | Task | Output |
|-------|------|--------|
| Stage 1 | Binary ARG detection | ARG / non-ARG |
| Stage 2 | 15-class ARG classification | Resistance category |
| Stage 3 | 6-subclass β-lactam prediction | β-lactam subtype |

## Usage

```bash
# Stage 1: ARG detection
python ARCompassStage1.py -i data/test01.Stage1.fasta -o result/test01/ -p 0.9

# Stage 2: ARG classification (15 classes)
python ARCompassStage2.py -i data/test01.Stage2.fasta -o result/test01/ -p 0.9

# Stage 3: β-lactam subclass prediction
python ARCompassStage3.py -i data/test01.Stage3.fasta -o result/test01/
```

## Requirements

- Python ≥ 3.7, PyTorch ≥ 1.6.0, NVIDIA GPU