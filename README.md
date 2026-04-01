# CSET419 – Introduction to Generative AI Labs
Workflows for all Generative AI labs. Each lab focuses on implementing a different generative model or technique.

---

# Lab 1 – Synthetic Data Generation
## Objective
Generate synthetic data using a pre-trained generative model.
## Workflow
1. Select domain and pre-trained model (e.g., Stable Diffusion).
2. Provide text prompts and generate samples.
3. Store and verify outputs.
## Output
- Synthetic dataset. 

---

# Lab 2 – GAN for Image Generation
## Objective
Train a basic Generative Adversarial Network (GAN) to generate synthetic images.
## Workflow
1. Load and normalize dataset.
2. Define Generator and Discriminator networks.
3. Train GAN using adversarial loss.
4. Save and predict labels of generated images.
## Output
- Training logs and generated image samples.

---

# Lab 3 – Variational Autoencoder (VAE)
## Objective
Implement a VAE to learn latent representations and generate new samples.
## Workflow
1. Load dataset and build Encoder/Decoder networks.
2. Apply reparameterization trick.
3. Train using Reconstruction loss and KL Divergence.
4. Generate new samples from latent space.
## Output
- Trained model, reconstructed, and generated images.

---

# Lab 4 – Text Generation Model
## Objective
Train a neural network to generate new text sequences from a corpus.
## Workflow
1. Load, preprocess, and tokenize text data.
2. Design sequence model (RNN/LSTM/GRU or Transformer).
3. Train model and generate sequences using seed text.
## Output
- Generated text samples.

---

# Lab 5 – Image-to-Image Translation (Baseline CNN)
## Objective
Implement an encoder–decoder CNN for image translation.
## Workflow
1. Load paired dataset (CIFAR10) and build CNN architecture.
2. Train using MSE/L1 loss.
3. Generate translated images.
## Output
- Translated images (often blurry).

---

# Lab 6 – Pix2Pix GAN
## Objective
Implement Pix2Pix GAN for image-to-image translation.
## Workflow
1. Prepare paired dataset and implement U-Net generator.
2. Implement PatchGAN discriminator.
3. Train with Adversarial and L1 loss.
## Output
- Sharper translated images.

---

# Lab 7 – Neural Style Transfer
## Objective
Generate a stylized image combining content and style from different images.
## Workflow
1. Load content/style images and pre-trained VGG19.
2. Extract layers and define content/style/total loss.
3. Optimize generated image iteratively.
## Output
- Stylized image.

---

# Lab 8 – Artistic Outputs via Neural Art
## Objective
Generate artistic images using GAN latent space exploration.
## Workflow
1. Load pre-trained basic and advanced GAN models.
2. Generate random samples.
3. Perform latent vector interpolation to observe transitions.
## Output
- Generated samples and interpolated transition sequences.

---

# Lab 9 – Sequence Generation
## Objective
Apply generative models to sequential data.
## Workflow
1. Component I: Train an RNN/LSTM model to generate sequences.
2. Component II: Train a Transformer model with positional encoding for sequence generation.
## Output
- Generated sequences.

---

# Lab 10 – Sequential Data Generation
## Objective
Implement a generative model capable of learning patterns from sequential data and generating new sequences.
## Workflow
1. Preprocess and tokenize the sequence dataset.
2. Design and train an RNN/LSTM-based model.
3. Design and train a Transformer encoder architecture with positional encoding.
## Output
- Generated text sequences.

---

# Lab 11 – Fine-Tuning for Real-World Applications
## Objective
Fine-tune a pre-trained generative model (GPT-2) for real-world applications.
## Workflow
1. Component I: Fine-tune GPT-2 on e-commerce data to generate product reviews.
2. Component II: Fine-tune GPT-2 on food-tech data to generate recipe instructions.
3. Compare the baseline outputs with fine-tuned outputs for both tasks.
## Output
- Realistic product review language.
- Step-by-step cooking instructions.

---

# Summary of Labs
| Lab | Topic | Model Used |
|----|----|----|
| Lab 1 | Synthetic Data Generation | Pretrained Diffusion Model |
| Lab 2 | Image Generation | GAN |
| Lab 3 | Latent Representation | VAE |
| Lab 4 | Text Generation | RNN / Transformer |
| Lab 5 | Image Translation | CNN Encoder–Decoder |
| Lab 6 | Image Translation | Pix2Pix GAN |
| Lab 7 | Artistic Style Transfer | Neural Style Transfer |
| Lab 8 | Artistic Outputs via Latent Space | DCGAN & PGAN |
| Lab 9 | Sequence Generation | RNN / LSTM & Transformer |
| Lab 10 | Sequential Data Generation | RNN / LSTM & Transformer |
| Lab 11 | Fine-Tuning GPT-2 | GPT-2 |
