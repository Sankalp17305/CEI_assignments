# 🧠 Text Generation using RNN, LSTM & GRU

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)
![Colab](https://img.shields.io/badge/Google%20Colab-Ready-yellow?logo=googlecolab)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A Deep Learning project comparing **Vanilla RNN, LSTM, and GRU** for next-word prediction and text generation — built as part of a university learning assignment.

---

## 📌 Overview

This project trains three sequence models on a text corpus and compares:
- Training loss convergence
- Text generation quality
- Memory handling ability
- Long-term dependency learning

---

## 🗂️ Project Structure

```
📦 Text-Generation-RNN-LSTM-GRU
 ┣ 📓 Text_Generation_RNN_LSTM_GRU_Learning_Project.ipynb
 ┗ 📄 README.md
```

---

## ⚙️ Models

| Model | Architecture | Hidden Units | Embedding Dim | Epochs |
|-------|-------------|-------------|---------------|--------|
| Vanilla RNN | SimpleRNN | 128 | 64 | 200 |
| LSTM | Long Short-Term Memory | 128 | 64 | 200 |
| GRU | Gated Recurrent Unit | 128 | 64 | 200 |

---

## ✅ Tasks Completed

- [x] Task 1 — Replaced corpus with custom paragraph
- [x] Task 2 — Increased embedding dimension (32 → 64)
- [x] Task 3 — Increased epochs (100 → 200)
- [x] Task 4 — Increased hidden units (64 → 128)
- [x] Task 5 — Generated 10 words instead of 5

---

## 📊 Results

### Text Generation (Seed: `"deep learning"`)

| Model | Output |
|-------|--------|
| RNN | `deep learning models can generate meaningful sentences...` |
| LSTM | `deep learning is transforming artificial intelligence...` |
| GRU | `deep learning models can generate meaningful sentences...` |

### Training Loss Comparison

- 🔵 **RNN** — Converged fastest, lowest final loss
- 🟢 **GRU** — Close second, stable convergence  
- 🟠 **LSTM** — Slowest but steady decrease over 200 epochs

---

## 🛠️ Installation

```bash
pip install tensorflow numpy matplotlib
```

---

## 🚀 How to Run

**Option 1 — Google Colab (Recommended)**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

1. Upload the `.ipynb` file to Colab
2. Click `Runtime → Run All`

**Option 2 — Jupyter Notebook**

```bash
git clone https://github.com/your-username/Text-Generation-RNN-LSTM-GRU.git
cd Text-Generation-RNN-LSTM-GRU
jupyter notebook
```

---

## 📌 Key Takeaway

> For small datasets, all three models perform similarly.
> For larger and complex text, **LSTM and GRU outperform Vanilla RNN**
> due to their ability to retain long-term dependencies.

---

## 👤 Author

**Sam**  
B.Tech — Data Science  
Poornima Institute  

---

## 📄 License

This project is for educational purposes only.
