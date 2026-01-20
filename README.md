# STNGS: a deep scaffold learning-driven generation and screening framework for discovering potential novel psychoactive substances

[![Paper](https://img.shields.io/badge/Paper-Briefings%20in%20Bioinformatics-blue)](https://academic.oup.com/bib/article/26/1/bbae690/7934574)

A GPT-based deep learning model for molecular generation using SMILES notation with scaffold conditioning.

## Overview

This project implements a transformer-based model for generating novel molecular structures (SMILES) conditioned on molecular scaffolds. The model uses a GPT architecture with causal self-attention mechanisms.

## Features

- Scaffold-conditioned molecular generation
- SMILES augmentation and cleaning
- Molecular property analysis (MW, validity, uniqueness)
- Similarity and frequency analysis
- UMAP visualization
- Support for specific molecule generation (e.g., fentanyl analogs, MRTX849)

## Project Structure

```
src/
├── models/                  # Model architectures
│   ├── model.py            # GPT model implementation
│   └── otherModel.py       # Alternative models
│
├── data/                    # Data processing
│   ├── datasets.py         # Dataset classes
│   ├── augment-SMILES.py   # SMILES augmentation
│   ├── clean-SMILES.py     # SMILES cleaning
│   ├── get_scaffold.py     # Scaffold extraction
│   ├── SmilesEnumerator.py # SMILES enumeration
│   ├── split_data.py       # Data splitting
│   └── smiles_change.py    # SMILES transformation
│
├── training/                # Training scripts
│   ├── pretrain.py         # Model pretraining
│   ├── finetuning.py       # Model fine-tuning
│   └── sample.py           # Molecule generation
│
├── analysis/                # Analysis tools
│   ├── similarity.py       # Similarity metrics
│   ├── frequency.py        # Frequency analysis
│   ├── distribution.py     # Distribution analysis
│   ├── mw_valid_unique.py  # MW/validity/uniqueness
│   ├── mrtx849.py          # MRTX849 analysis
│   ├── select_fentanyl_rank.py  # Fentanyl ranking
│   └── vote.py             # Voting mechanism
│
├── visualization/           # Plotting tools
│   ├── plot.py             # General plotting
│   ├── plot_umap.py        # UMAP visualization
│   └── plot-fentanyl.py    # Fentanyl plots
│
└── utils/                   # Utilities
    ├── functions.py        # Helper functions
    ├── utils.py            # General utilities
    ├── Voc.py              # Vocabulary handling
    └── tabulate.py         # Table formatting
```
## Citation

If you use this code or model in your research, please cite the following paper:

**STNGS: a deep scaffold learning-driven generation and screening framework for discovering potential novel psychoactive substances**  
*Briefings in Bioinformatics, Volume 26, Issue 1, January 2025, bbae690*  
[https://doi.org/10.1093/bib/bbae690](https://academic.oup.com/bib/article/26/1/bbae690/7934574)

```bibtex
@article{STNGS2025,
  title={STNGS: a deep scaffold learning-driven generation and screening framework for discovering potential novel psychoactive substances},
  journal={Briefings in Bioinformatics},
  volume={26},
  number={1},
  pages={bbae690},
  year={2025},
  doi={10.1093/bib/bbae690},
  url={https://academic.oup.com/bib/article/26/1/bbae690/7934574}
}
