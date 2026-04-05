# ARC Multiple-Choice Reasoning with Word Embeddings, BERT, and LLM Evaluation

This project explores different NLP approaches for solving grade-school science multiple-choice questions from the AI2 Reasoning Challenge (ARC), including baselines, transformer models, and LLM evaluation.

## Overview
- University group project for an NLP course
- Task: predict the correct answer for multiple-choice science questions from the ARC dataset
- Focused mainly on the `arc-easy` split for training and evaluation
- Final work includes data analysis, model training, evaluation, and error analysis

## What this folder contains
- `2_data_analysis/`: dataset exploration and preprocessing analysis
- `3_word_embedding/`: baseline word-embedding classifier and evaluation code
- `5_transfer_learning/`: randomly initialized and pretrained BERT experiments
- `6_evaluate_LLM/`: LLM-based evaluation on ARC question samples
- `1_Documentation/Visualisations/`: plots used in the report
- `Stableconfusion_Team1_Canvas.pdf`: final project report
- `requirements.txt`: Python dependencies

## Methods
- Data analysis and topic modeling on ARC questions
- Filtering to standard 4-choice multiple-choice questions
- Word-embedding baseline using Word2Vec, GloVe, and FastText variants
- Custom neural network classifier on embedding-based inputs
- Randomly initialized BERT for multiple-choice classification
- Finetuned pretrained BERT models with regularization and dropout tuning
- Ensemble experiments with BERT-based models
- LLM evaluation on a sample of ARC-Easy test questions
- Error analysis using confusion matrices and Captum saliency maps

## Dataset
- Source: AI2 Reasoning Challenge (ARC)
- Domain: grade-school science multiple-choice questions
- Training mainly used the `arc-easy` subset
- Evaluation metric: accuracy

## Key findings
- The simple “always answer B” baseline performed near random guessing
- Word-embedding models slightly improved over the naive baseline
- Finetuned BERT models outperformed simpler baselines but remained below leaderboard models
- LLM evaluation showed much stronger results than the trained course models on the sampled questions
- Error analysis suggested that the models struggled with deeper scientific reasoning and nuanced contextual understanding

## My contribution
- Data analysis
- Training a randomly initialized Transformer
- Finetuning a pretrained Transformer

## Tech stack
Python, PyTorch, Hugging Face Transformers, Optuna, Captum, Jupyter

## Notes
- This folder is kept as part of my bachelor coursework archive
- The code reflects an experimental course workflow with multiple tasks and notebooks
- The final report contains the full methodology, results, and team contribution breakdown

## Project context
Group project for the NLP course during my bachelor studies.