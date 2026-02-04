# GenAI Lab 3 – Variational Autoencoder (VAE) with KL Divergence Analysis

## Objective
The objective of this lab is to understand and implement a **Variational Autoencoder (VAE)** using PyTorch and analyze the importance of **KL Divergence** in learning a structured latent space.  
The experiment compares model behavior **with KL Divergence** and **without KL Divergence** on the Fashion-MNIST dataset.

---

## Dataset Used
- **Fashion-MNIST**
- 28×28 grayscale images of clothing items
- Training set: 60,000 images  
- Test set: 10,000 images

---

## What We Do in This Lab
1. Load and preprocess the Fashion-MNIST dataset  
2. Build a Variational Autoencoder (Encoder + Decoder)  
3. Train two models:
   - **VAE without KL Divergence**
   - **VAE with KL Divergence**
4. Compare:
   - Reconstruction loss (Binary Cross Entropy)
   - Latent space distribution
   - Generated samples
5. Visualize how KL Divergence affects:
   - Latent space structure
   - Quality of generated images

---

## Model Architecture

### Encoder
- Input layer: 784 neurons (28×28 image)
- Hidden layer: 400 neurons (ReLU)
- Output:
  - Mean (μ)
  - Log variance (log σ²)

### Decoder
- Input: Latent vector
- Hidden layer: 400 neurons (ReLU)
- Output layer: 784 neurons (Sigmoid)

