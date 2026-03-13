# CSET419 – Introduction to Generative AI Labs
Workflows for all Generative AI labs. Each lab focuses on implementing a different generative model or technique used in modern AI systems.

---

# Lab 1 – Synthetic Data Generation
## Objective
Generate synthetic data using a pre-trained generative model.

## Workflow
1. Select a domain for data generation (e.g., images).
2. Choose a pre-trained generative model (e.g., Stable Diffusion).
3. Provide multiple text prompts.
4. Generate synthetic samples using the model.
5. Store generated outputs in a dataset folder.
6. Display and verify sample outputs.

## Output
- Synthetic dataset generated from prompts. 

---

# Lab 2 – GAN for Image Generation
## Objective
Train a basic Generative Adversarial Network (GAN) to generate synthetic images.



[Image of Generative Adversarial Network architecture diagram]


## Workflow
1. Load dataset (MNIST or Fashion-MNIST).
2. Normalize dataset images.
3. Define Generator network.
4. Define Discriminator network.
5. Initialize hyperparameters:
   - epochs
   - batch_size
   - noise_dim
   - learning_rate
6. Train GAN:
   - Train discriminator on real and fake images.
   - Train generator using adversarial loss.
7. Save generated image samples during training.
8. Generate final synthetic images.
9. Use a pretrained classifier to predict labels of generated images.

## Output
- Training logs
- Generated image samples
- Final generated images
- Predicted labels of generated images. 

---

# Lab 3 – Variational Autoencoder (VAE)
## Objective
Implement a Variational Autoencoder to learn latent representations and generate new samples.



## Workflow
1. Load dataset (MNIST / Fashion-MNIST).
2. Normalize input data.
3. Split dataset into training and testing sets.
4. Build Encoder network.
5. Compute latent mean and variance.
6. Apply reparameterization trick.
7. Build Decoder network.
8. Define loss function:
   - Reconstruction loss
   - KL Divergence
9. Train the VAE model.
10. Generate new samples from latent space.
11. Visualize latent space (optional).

## Output
- Trained VAE model
- Reconstructed images
- Generated images
- Loss curves. 

---

# Lab 4 – Text Generation Model
## Objective
Train a neural network to generate new text sequences from a text corpus.

## Workflow
1. Load text dataset.
2. Preprocess text data.
3. Perform tokenization (character-level or word-level).
4. Create input-output training sequences.
5. Design sequence model:
   - RNN / LSTM / GRU.
6. Train the model.
7. Provide a seed text.
8. Generate new text sequences.

### Transformer Extension
1. Tokenize text using subword or word-level tokenization.
2. Add positional encoding.
3. Implement Transformer encoder blocks.
4. Train the transformer model.
5. Generate text samples.

## Output
- Generated text samples. 

---

# Lab 5 – Image-to-Image Translation (Baseline CNN)
## Objective
Implement an encoder–decoder CNN for image-to-image translation.

## Workflow
1. Load paired image dataset (CIFAR10).
2. Normalize images to range [-1, 1].
3. Build encoder-decoder CNN architecture.
4. Train model using reconstruction loss:
   - MSE
   - L1 loss
5. Generate translated images.
6. Visualize outputs.

## Output
- Translated images (often blurry due to lack of GAN training). 

---

# Lab 6 – Pix2Pix GAN
## Objective
Implement Pix2Pix GAN for image-to-image translation.



## Workflow
1. Prepare paired dataset (Edges → Real images).
2. Split dataset into training and testing sets.
3. Implement U-Net generator:
   - Downsampling layers
   - Upsampling layers
   - Skip connections
4. Implement PatchGAN discriminator.
5. Define losses:
   - Adversarial loss
   - L1 reconstruction loss
6. Train GAN with alternating generator and discriminator updates.
7. Generate translated images.
8. Compare results with baseline CNN.

## Output
- Sharper translated images compared to CNN model. 

---

# Lab 7 – Neural Style Transfer
## Objective
Generate a stylized image by combining content from one image and style from another.



## Workflow
1. Load content image.
2. Load style image.
3. Load pretrained VGG19 model.
4. Extract content and style layers.
5. Define loss functions:
   - Content loss
   - Style loss
   - Total loss
6. Perform iterative optimization on the generated image.
7. Update image to minimize total loss.

## Output
- Stylized image with preserved content and transferred artistic style. 

---

# Lab 8 – Create Artistic Outputs using Neural Art Concepts
## Objective
Generate artistic images using Generative Adversarial Networks (GANs) by exploring the latent space of the generator. Investigate how different architectures produce varied outputs and how latent space interpolation behaves.



## Workflow
1. Apply environment patches for modern Python and SSL compatibility.
2. Load a pre-trained basic GAN model (e.g., DCGAN on CelebA).
3. Generate 5-10 random samples using the basic GAN to visualize artistic diversity.
4. Perform mathematical interpolation between two random latent vectors to observe smooth visual transitions.
5. Load a pre-trained advanced GAN model (e.g., PGAN on CelebA-HQ).
6. Generate 5-10 high-resolution random samples using the advanced GAN.
7. Perform latent vector interpolation on the advanced GAN model.
8. Display and locally save the generated grids for comparison.

## Output
- Generated basic GAN image samples.
- Interpolated basic GAN transition sequences.
- Generated high-resolution advanced GAN image samples.
- Interpolated advanced GAN transition sequences.

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
| Lab 8 | Artistic Outputs via Latent Space | DCGAN & PGAN (Pre-trained) |
