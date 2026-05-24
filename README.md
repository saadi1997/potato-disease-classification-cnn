# Potato Leaf Disease Classification Using CNN

**Authors:** Muhammad Saad Bin Zahid (24K-8046), Muhammad Owais (24K-8049)  
**Course:** Deep Learning (Spring 2026)

## Overview
This project trains a Convolutional Neural Network (CNN) from scratch to classify potato leaf images into:
- Healthy
- Early blight
- Late blight

The goal is to demonstrate an end-to-end deep learning workflow: dataset loading, preprocessing, augmentation, CNN training, and evaluation.

## Dataset
We use the PlantVillage dataset from Kaggle (potato-only subset: 3 classes, 2,152 images).
- Dataset link: https://www.kaggle.com/datasets/arjuntejaswi/plant-village/data  
**Note:** The dataset is not uploaded to this repo due to size. Please download it separately and keep only the potato folders:
- `Potato___Early_blight`
- `Potato___Late_blight`
- `Potato___healthy`

## Method
- Image size: 256×256
- Train/Val/Test split: 80/10/10
- Data augmentation: random flips and small rotations (train only)
- Model: CNN (Conv2D + MaxPool blocks → Dense → Softmax)
- Optimizer: Adam
- Loss: Sparse Categorical Cross-Entropy
- Epochs: 50

## Results (Test Set)
- Test Accuracy: ~97%
- Confusion matrix and per-class metrics are included in the report.

## How to Run (Colab)
1. Upload the potato-only dataset ZIP to Colab and unzip.
2. Open the notebook in `/notebook/`.
3. Set `DATA_DIR` to the extracted dataset folder.
4. Run all cells.

## Repository Contents
- `notebook/` → training and evaluation notebook
- `report/` → final project report (PDF)
- `slides/` → project presentation
- `models/` → saved model (`.keras`) (optional)
- `assets/` → figures used in report/slides (optional)

## Acknowledgements
Tutorial inspiration: Codebasics (Potato Disease Classification series).  
Dataset credit: PlantVillage (Kaggle source above).
