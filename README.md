# STNGS - Scaffold-based Transformer for Novel Generation of SMILES

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
