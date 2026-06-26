# 🧠 Denoising Autoencoder on MNIST

A deep learning project that removes Gaussian noise from handwritten digit images using three different Autoencoder architectures, built with PyTorch.

---

## 📌 Objective

Build and compare three Denoising Autoencoders that take **noisy images as input** and reconstruct **clean images as output**, trained on the MNIST dataset.

---

## 🏗️ Model Architectures

| Model | Type | Description |
|-------|------|-------------|
| Model 1 | Fully-Connected (FFNN) | 784→256→32 encoder, 32→256→784 decoder |
| Model 2 | Transpose CNN | Conv+MaxPool encoder, ConvTranspose2d decoder |
| Model 3 | Upsampled CNN | Conv+MaxPool encoder, Interpolation+Conv decoder |

---

## 📊 Results

| Model | Test MSE |
|-------|----------|
| FFNN | **0.0360** ✅ Best |
| Transpose CNN | 0.0865 |
| Upsampled CNN | 0.1005 |

---

## 🖼️ Sample Output

Each model produces a 3-row visualization:
- **Row 1:** Original clean image
- **Row 2:** Noisy image (Gaussian noise, factor=0.5)
- **Row 3:** Denoised reconstruction

---

## 🚀 How to Run

1. Open `autoencoder_mnist.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Click **Runtime → Run All**
3. MNIST dataset downloads automatically
4. Training runs for 20 epochs per model

---

## 🛠️ Requirements

```
torch
torchvision
numpy
matplotlib
```

All pre-installed in Google Colab — no setup needed.

---

## 📁 Project Structure

```
├── autoencoder_mnist.ipynb   # Main notebook with all code and results
└── README.md                 # Project documentation
```

---

## 🔑 Key Concepts

- **Denoising Autoencoder:** Learns to reconstruct clean images from corrupted inputs
- **Gaussian Noise:** Added with factor=0.5, clamped to [0,1]
- **Loss Function:** MSELoss (pixel-wise reconstruction error)
- **Optimizer:** Adam (lr=0.01)
- **Bottleneck:** Compresses input to discard noise, retain digit features

---

## 👤 Author

**Sankalp Tamboli**  
CEI Internship Program 2026  
Poornima Institute of Engineering & Technology
