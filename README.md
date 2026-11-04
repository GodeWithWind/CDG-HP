# GNN-Enabled Robust Hybrid Precoding with Score-Based CSI Generation and Denoising

This repository provides supplementary statistical results and six CSI datasets associated with the above manuscript.

## Overview

The paper proposes a channel-distribution-guided hybrid precoding (CDG-HP) framework comprising three modules:

- **DMP-GAT:** Hybrid precoding through node-level and edge-level message passing.
- **CDSNet:** Score-based CSI generation for offline data augmentation.
- **ECRNet:** Error-conditioned refinement of imperfect CSI before online hybrid precoding.

## Release Status

This release contains supplementary statistical results and six DeepMIMO-based CSI datasets from New York (NY), Los Angeles (LA), and Chicago (CHI). The complete implementation code will be released upon acceptance.

## Supplementary Statistical Results

See [supplementary_results.md](supplementary_results.md) for the four statistical tables corresponding to Tables IV–VII in the response letter:

1. High-resolution CSI: means and sample standard deviations.
2. Imperfect CSI: representative means and sample standard deviations.
3. High-resolution CSI: individual-run results.
4. Imperfect CSI: individual-run results.

All sum rates are reported in bit/s/Hz. Summary statistics are presented as mean ± sample standard deviation over three independent runs.

## CSI Datasets

Six MATLAB `.mat` files are provided in [datasets/](datasets/). Each city has two configurations: `(K, N_T) = (8, 16)` and `(16, 32)`. Each file contains 10,000 complex-valued CSI samples in the variable `H_gather`.

See [datasets/README.md](datasets/README.md) for file descriptions, array dimensions, sample selection, and MATLAB/Python loading examples. Dataset provenance and SHA-256 checksums are recorded in [datasets/manifest.json](datasets/manifest.json).

The urban channel data are derived from [DeepMIMO](https://www.deepmimo.net/).

## Repository Structure

```text
.
├── README.md
├── supplementary_results.md
└── datasets/
    ├── README.md
    ├── manifest.json
    ├── NY_ant16_user8.mat
    ├── NY_ant32_user16.mat
    ├── LA_ant16_user8.mat
    ├── LA_ant32_user16.mat
    ├── CHI_ant16_user8.mat
    └── CHI_ant32_user16.mat
```
