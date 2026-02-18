# GenAI Lab Week 5: Image-to-Image Translation & Editing

This lab explores two distinct approaches to Generative AI for images: training a baseline Convolutional Neural Network (CNN) for image reconstruction and utilizing a pre-trained Stable Diffusion model for text-guided image editing.

---

## 📋 Prerequisites
* **Environment:** Google Colab (Recommended) or Local Python Environment with GPU support.
* **Hardware:** NVIDIA GPU (T4 or better recommended).
* **Key Libraries:**
    * `torch`, `torchvision` (for Task 1)
    * `diffusers`, `transformers`, `accelerate`, `PIL` (for Task 2)

---

## 🛠️ Task 1: Baseline CNN for Image-to-Image Translation
**Objective:** Implement a non-adversarial Encoder-Decoder CNN to learn a mapping from input images to target images.
**Dataset:** CIFAR-10 (Grayscale Inputs $\rightarrow$ Color Targets)

### Workflow Steps:
1.  **Data Loading & Preprocessing:**
    * Download CIFAR-10 dataset.
    * Normalize images to the range `[-1, 1]` (crucial for Tanh activation).
    * Create pairs: `Input = Grayscale Image`, `Target = Original Color Image`.
2.  **Model Architecture (Encoder-Decoder):**
    * **Encoder:** Compresses the 32x32 input into a lower-dimensional latent representation using Conv2d layers and ReLU.
    * **Decoder:** Upsamples the latent features back to 32x32 RGB images using ConvTranspose2d layers.
    * **Output Activation:** `Tanh` is used to ensure output pixel values match the normalized range `[-1, 1]`.
3.  **Training:**
    * **Loss Function:** Mean Squared Error (MSE) to minimize pixel-level differences.
    * **Optimizer:** Adam (`lr=0.001`).
    * **Epochs:** 10 (Demonstration).
4.  **Visualization:**
    * Compare **Input (Grayscale)** vs. **Generated (Reconstructed)** vs. **Ground Truth**.
    * *Expected Result:* generated images will be recognizable but slightly blurry compared to GANs.

---

## 🎨 Task 2: Text-Guided Image Editing (InstructPix2Pix)
**Objective:** Use a state-of-the-art Latent Diffusion Model to edit a real image based on natural language instructions.
**Model:** `timbrooks/instruct-pix2pix`

### Workflow Steps:
1.  **Environment Setup:**
    * Install Hugging Face `diffusers` and dependencies.
2.  **Input Preparation:**
    * Upload a source image (saved as `input.jpg`).
    * Resize image to 512x512 for optimal model performance.
3.  **Prompt Definition:**
    * Define a list of "Instruction Prompts" (e.g., *"Make him a cyborg"*, *"Turn background to cyberpunk city"*).
4.  **Inference Pipeline:**
    * Load the `StableDiffusionInstructPix2PixPipeline`.
    * Run the pipeline on the input image for each prompt in the list.
    * **Parameters:**
        * `image_guidance_scale`: Controls how much the original image structure is preserved.
        * `guidance_scale`: Controls how strongly the text prompt is followed.
5.  **Output Generation:**
    * Display the Original Image side-by-side with the Edited Result for qualitative evaluation.

---

## 🚀 How to Run
1.  Open the provided **Google Colab Notebook**.
2.  **Run Task 1 Cell:** Observe the loss decreasing and view the reconstruction plots at the end.
3.  **Run Task 2 Cell:**
    * The script will ask you to upload an image.
    * Select a clear `.jpg` or `.png` from your computer.
    * Watch as the model generates variations based on the provided prompts.
