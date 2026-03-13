# CSET419 Lab 8: Create Artistic Outputs using Neural Art Concepts

## Objective
This lab explores the latent space of Generative Adversarial Networks (GANs) to generate artistic and photorealistic images. By loading pre-trained GAN models and manipulating their latent vectors, we investigate how different architectures produce diverse visual outputs and how interpolating between vectors creates smooth, continuous transitions between generated images.



[Image of Generative Adversarial Network architecture diagram]


## Lab Workflow & Tasks

This implementation fulfills the lab requirements by exploring one Basic GAN (DCGAN) and one Advanced GAN (PGAN, used as a robust alternative to StyleGAN2 for the CelebA-HQ dataset).

### 1. Environment Setup & Patches
The code is designed to run seamlessly in modern Google Colab environments. It includes built-in patches to ensure compatibility with older PyTorch Hub repositories:
* **Iterable Patch:** Fixes Python 3.10+ compatibility issues with `collections.abc`.
* **SSL Bypass:** Resolves outdated Facebook SSL certificate blocks when downloading weights.

### 2. Model Loading
The script fetches pre-trained models directly from the `facebookresearch/pytorch_GAN_zoo` hub.
* **Basic Model (DCGAN):** Trained on the standard CelebA dataset.
* **Advanced Model (PGAN - Progressive GAN):** Trained on the high-resolution CelebA-HQ 256x256 dataset. 

### 3. Latent Space Exploration
For each model, the script performs two distinct explorations:
* **Random Sampling:** Generates a grid of 10 distinct images using random noise vectors to showcase the diversity of the generator.
* **Latent Vector Interpolation:** Takes two random latent vectors ($z_1$ and $z_2$) and mathematically interpolates between them over 10 steps using the formula: 
    $$v = (1 - \alpha) \cdot z_1 + \alpha \cdot z_2$$
    This demonstrates how the GAN maps continuous mathematical changes to smooth visual transitions.

### 4. Output Generation & Visualization
All generated outputs are processed using `torchvision.utils.make_grid` and `matplotlib`, then saved locally into an automatically generated `lab8_results` directory.

---

## Dependencies
To run this notebook, ensure you have the following installed (standard in Google Colab):
* `torch`
* `torchvision`
* `numpy`
* `matplotlib`

---

## How to Run
1. Open the `Gen_AI_Week_8.ipynb` file in **Google Colab**.
2. Go to **Runtime > Change runtime type** and ensure **Hardware accelerator** is set to **T4 GPU** (or any available GPU) for faster inference.
3. Run all cells. 
4. The models will download their pre-trained weights automatically. 
5. Once execution finishes, click the **Files** folder icon on the left sidebar in Colab to view and download your output images from the `lab8_results/` folder.

---

## Expected Outputs
Upon successful execution, the `lab8_results/` directory will contain four files:
1.  `dcgan_samples.png`: Randomly generated faces from DCGAN.
2.  `dcgan_interpolation.png`: A sequence of DCGAN faces morphing from one identity to another.
3.  `pgan_samples.png`: High-resolution, randomly generated faces from PGAN.
4.  `pgan_interpolation.png`: A smooth, high-resolution morphing sequence from PGAN.
