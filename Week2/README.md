# GAN for Handwritten Digit Generation (MNIST)

## Overview
This project implements a **Generative Adversarial Network (GAN)** to generate synthetic handwritten digit images resembling the MNIST dataset. A pre-trained **LeNet-5** classifier is used to evaluate the quality of the generated images.

## Key Features

### Dynamic GAN Configuration
The GAN supports configurable hyperparameters such as:
- Number of training epochs  
- Batch size  
- Noise vector dimension  

This flexibility allows for easy experimentation and fine-tuning.

### Data Loading and Preprocessing
- Uses the MNIST dataset
- Images are normalized to the range **[-1, 1]**
- Normalization matches the generator’s `tanh` activation function

### Model Architecture

#### Generator
- Built using `Conv2DTranspose` layers
- Upsamples random noise vectors into **28×28 grayscale images**

#### Discriminator
- A Convolutional Neural Network (CNN)
- Classifies images as **real** or **fake**

### GAN Training
- Generator and discriminator are trained in an adversarial loop
- The generator improves image realism
- The discriminator improves its ability to detect fake images

### Image Generation and Classification
- After training, the generator produces synthetic digit images
- Images are classified using a pre-trained **LeNet-5** model
- Generated images are saved into folders labeled **0–9** based on predictions

### Performance Evaluation
- Classification accuracy on generated images is calculated
- A prediction breakdown provides insight into model performance per digit

## Purpose
This project demonstrates how GANs can be used to generate realistic handwritten digits and how a classifier can be leveraged to quantitatively evaluate the quality of generated samples.
