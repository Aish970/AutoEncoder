# 🔍 Supervised vs Unsupervised Autoencoders — MNIST Dimensionality Reduction

This repository contains the implementation of a **Supervised Autoencoder** and a standard **Unsupervised Autoencoder** applied to the MNIST dataset. The goal is to compare their ability to generate **discriminative low-dimensional features**.

🧑‍💻 Author: Aishwarya Bhethanabotla  
📅 CS 584 — Deep Learning Assignment 4 (Spring 2025)

---

## 🎯 Objective

Traditional Autoencoders and PCA learn compact representations but are **unsupervised** and often **non-discriminative**. This project explores how incorporating label supervision improves:

- Feature separability in latent space
- Classification performance using compressed features
- Reconstruction quality

---

## 🧠 What’s Implemented

| Component | Description |
|----------|-------------|
| `AE` | Fully connected autoencoder (unsupervised) |
| `SAE` | Supervised autoencoder with joint label + image reconstruction loss |
| `to_one_hot()` | One-hot encoding for MNIST labels |
| `encoder_visualization()` | 2D scatter plot of latent features |
| `reconstruction_plot()` | Image reconstruction comparison |
| `classifier_on_latent()` | Train a softmax classifier on latent space |

---

## 📂 File Structure


---

## 📊 Dataset

- **MNIST**: Handwritten digit dataset (70,000 samples, 28×28 pixels)
- Preprocessed and flattened to 784-dimensional vectors
- 10K training samples, 50K validation samples, 10K test samples

---

## 🧪 Evaluation

- **Validation loss** (MSE) on reconstruction
- **Visualization** of 2D latent space
- **Classification accuracy** on compressed features
- **Reconstruction quality**

| Metric              | Unsupervised AE | Supervised AE |
|---------------------|-----------------|----------------|
| Feature separability| ❌ Mixed classes | ✅ Distinct clusters |
| Classification Acc. | ❌ Poor          | ✅ High        |
| Reconstruction Loss | ✅ Low           | ✅ Low         |

---

## 🧰 How to Run

1. Open `Assignment4_Aishwarya_B-2.ipynb` in Jupyter or Colab
2. Install dependencies:
   ```bash
   pip install tensorflow numpy matplotlib
