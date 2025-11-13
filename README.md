# DDoS-Detection-using-Python-and-ML
ACKTransformer is a Transformer-based deep learning model for detecting ACK Fragmentation DDoS attacks using Python. It provides a full pipeline for preprocessing, training, cross-validation, and generating evaluation reports and visualizations using PyTorch and Scikit-learn.
# ACKTransformer – DDoS Attack Detection using Python and Transformers

This project implements a Transformer-based deep learning model to detect ACK Fragmentation DDoS attacks from network traffic data. It provides a complete workflow for data preprocessing, model training, cross-validation, evaluation, and report generation using Python.

## Overview

`ACKTransformer` is a custom Transformer model built for tabular data classification. The system includes:

- Data loading and preprocessing  
- Transformer model training using PyTorch  
- Stratified 5-fold cross-validation  
- Performance evaluation and visualization  
- Automatic saving of models, metrics, and plots  

## Project Workflow

### 1. Data Preprocessing
- Loads `shuffled_merged_data.csv`  
- Handles missing values  
- Replaces label values  
- Scales features using StandardScaler  

### 2. Model Architecture
The model includes:
- Input projection  
- Transformer encoder layers  
- Fully connected output layers  
- Softmax classification  

### 3. Training and Validation
- Uses StratifiedKFold for 5-fold cross-validation  
- Tracks loss, accuracy, precision, recall, and F1-score  
- Applies early stopping  
- Saves best model for each fold  

### 4. Visualization and Reporting
Generates:
- Loss and accuracy curves  
- Confusion matrices  
- ROC curves  
- UMAP visualizations  
- Classification reports (CSV)  

### 5. Output Structure

ddos_results/
│
├── models/        # Saved Transformer model checkpoints (.pth)
├── plots/         # Loss/Accuracy, ROC, CM, UMAP images
└── reports/       # Classification reports for each fold (CSV)


## Python Libraries Used

| Purpose          | Libraries                         |
| ---------------- | --------------------------------- |
| Data Handling    | pandas, numpy                     |
| Visualization    | matplotlib, umap-learn            |
| Machine Learning | scikit-learn                      |
| Deep Learning    | torch, torch.nn, torch.utils.data |
| File Management  | os, pathlib                       |


## Summary

This project provides a complete and reproducible Python pipeline for DDoS attack detection using Transformer architectures. It integrates data preprocessing, deep learning, evaluation, and visualization in a modular and efficient framework.
