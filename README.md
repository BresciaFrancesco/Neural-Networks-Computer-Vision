# FinalAssignment-FrancescoBrescia

# Attention U-Net for Semantic Image Segmentation on Cityscapes

This project implements a semantic segmentation pipeline using an **Attention U-Net** architecture trained on the **Cityscapes dataset**, optimized with **Focal Loss** to handle class imbalance. The goal is to accurately segment urban street scenes by predicting a class label for each pixel in high-resolution images.

---

## Overview

- **Architecture:** Attention-based U-Net for enhanced skip-connection modulation
- **Loss Function:** Focal Loss
- **Dataset:** Cityscapes – fine-labeled pixel annotations of urban street scenes
- **Evaluation Metric:** Jaccard Index (IoU) per class
- **Logging:** Integrated with [Weights & Biases (wandb)](https://wandb.ai) for experiment tracking
- **Inference & Visualization:** Real-time comparison between baseline and improved models with color-coded masks

---

## Project Structure

```
├── model.py               # Model architecture with attention U-Net
├── train.py               # Training loop with data pipeline, loss, and metrics
├── loss.py                # Custom implementation of Focal Loss
├── utils.py               # Label ID mapping and dataset-specific utilities
├── visualization.py       # Inference and visual comparison of predictions
├── requirements.txt       # (To be added) Python dependencies
└── README.md              # Project documentation
```

## 🧪 Training Details

| Parameter        | Value              |
|------------------|--------------------|
| Epochs           | 250                |
| Batch size       | 16                 |
| Learning rate    | 0.001              |
| Optimizer        | Adam               |
| Loss             | Focal Loss (γ = 2) |
| Metric           | Mean IoU (Jaccard) |
| Hardware         | CUDA / CPU         |