# RNA Structure Prediction for the Stanford Ribonanza Kaggle Challenge

This project explores machine learning approaches for predicting RNA chemical reactivity profiles from sequence data in the Stanford Ribonanza RNA Folding competition.

## Overview
- University group project completed as part of the AI Challenge module
- Task: predict RNA reactivity values for two chemical mapping experiments, DMS_MaP and 2A3_MaP
- Competition evaluation metric: mean absolute error (MAE)
- Team name: HSLU StableConfusion

## What this folder contains
- `01_pipeline.ipynb`: main training and experimentation workflow
- `02_transfer_learning.ipynb`: experiments with pretrained models
- `03_feature_engineering.ipynb`: feature analysis and engineering experiments
- `preprocessing.py`: preprocessing utilities
- `noise_filter.py`: filtering logic for noisy samples
- `base_model.py`: model definitions and training components
- `testing.py`: testing utilities
- `final_report.pdf`: final project report
- `requirements.txt`: Python dependencies

## Methods
- Data quality assessment and missing-value analysis
- Signal-to-noise filtering using the provided `SN_filter`
- Sequence tokenization and padding
- Structural feature engineering using predicted RNA structure and loop types
- Comparison of single-model and dual-model prediction strategies
- Model experiments with:
  - Bidirectional RNN
  - Bidirectional LSTM
  - Transformer encoder
  - Pretrained sequence models

## Key project findings
- Filtering noisy samples improved validation performance
- Structural encoding improved model quality compared with sequence-only encoding
- A single-model setup achieved similar performance to a dual-model setup while reducing training time
- Among our submissions, the RNN achieved the best private Kaggle score, while the Transformer achieved the best public score

## Competition result
**Leaderboard Scores (sorted by Private Score)**

| Team | Rank | Public Score | Private Score |
|------|------|--------------|---------------|
| vigg | 1 | 0.13499 | 0.13960 |
| Hoyeol Sohn | 2 | 0.13544 | 0.14015 |
| ap eh ka | 3 | 0.13503 | 0.14037 |
| HSLU StableConfusion | 615 | 0.19483 | 0.27650 |

## Project context
Group project for the AI Challenge module at Hochschule Luzern, based on the Kaggle competition:
[Stanford Ribonanza RNA Folding](https://www.kaggle.com/competitions/stanford-ribonanza-rna-folding)

## Notes
- This folder is kept as part of my bachelor coursework archive
- The code reflects an experimental competition workflow rather than a production-ready package
- The report contains the full methodology, results, and reflection