# CIFAR-10 Image Classification — ANN vs CNN

**CEI Internship Program 2026 | Week 4 Assignment**
**Author:** Sankalp Tamboli

---

## Overview

This project implements and compares two deep learning architectures — **Artificial Neural Network (ANN)** and **Convolutional Neural Network (CNN)** — on the CIFAR-10 dataset. The goal is to understand why CNNs outperform ANNs for image classification tasks, and to explore techniques like data augmentation and early stopping to improve model performance.

---

## Dataset

**CIFAR-10** is a benchmark image classification dataset containing:

| Split | Images | Shape |
|-------|--------|-------|
| Training | 50,000 | 32 × 32 × 3 |
| Testing | 10,000 | 32 × 32 × 3 |

**10 Classes:** airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

---

## Tasks Completed

| # | Task | Description |
|---|------|-------------|
| 1 | Deeper ANN | Added `Dense(256)` + `Dense(128)` layers with Dropout |
| 2 | CNN Filter Upgrade | Changed filters from `32→64→128` |
| 3 | More Epochs | Increased training from 10 → 20 epochs |
| 4 | EarlyStopping | Added callback with `patience=5`, monitors `val_loss` |
| 5 | Data Augmentation | Random flip, rotation, and zoom on training images |

---

## Model Architectures

### ANN

Input (3072,) → Dense(512) → Dropout(0.3)
             → Dense(256) → Dropout(0.3)
             → Dense(128) → Dropout(0.2)
             → Dense(10, softmax)

> ANN flattens images into vectors — it cannot capture spatial features, which limits accuracy on image tasks.

### CNN

Input (32,32,3) → Conv2D(64) → BatchNorm → MaxPool
               → Conv2D(128) → BatchNorm → MaxPool
               → Conv2D(256) → BatchNorm → MaxPool
               → Flatten → Dense(128) → Dropout(0.4)
               → Dense(10, softmax)

> CNN preserves spatial relationships through convolution, making it far more effective for images.

### CNN + Data Augmentation

Adds a preprocessing layer before the CNN:

RandomFlip("horizontal") → RandomRotation(0.1) → RandomZoom(0.1)

---

## Results

| Model | Test Accuracy |
|-------|--------------|
| ANN | 42.64% |
| CNN | 73.43% |
| CNN + Augmentation | 49.60% |

**Key observation:** CNN significantly outperforms ANN because it preserves spatial features. The augmented CNN scored lower due to a smaller architecture and fewer epochs — it needs more training time to converge.

---

## Requirements

tensorflow >= 2.x
numpy
matplotlib
pandas

Install via:

pip install tensorflow numpy matplotlib pandas

---

## How to Run

1. Clone or download this repository
2. Open `Week4_Sankalp_Tamboli.ipynb` in Jupyter Notebook or Google Colab
3. Run all cells in order — the CIFAR-10 dataset will download automatically

---

## Project Structure

Week4_Sankalp_Tamboli.ipynb   ← main notebook
README.md                      ← this file

---

## Key Concepts

- **Normalization** — pixel values scaled from 0–255 to 0–1 for stable training
- **Dropout** — randomly disables neurons during training to prevent overfitting
- **BatchNormalization** — normalizes layer outputs for faster, more stable convergence
- **EarlyStopping** — halts training when validation loss stops improving, saving time and preventing overfitting
- **Data Augmentation** — artificially expands training data by applying random transformations
