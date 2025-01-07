# Custom GAN for CIFAR-10 Cats and Dogs

This repository contains the implementation and training of a **custom Generative Adversarial Network (GAN)** designed to generate realistic images of cats and dogs from the CIFAR-10 dataset. The unique discriminator architecture leverages concepts inspired by **Siamese Networks** to evaluate similarity between image pairs, enhancing the quality of the generated outputs.



## Introduction
Unlike traditional GAN architectures where the discriminator distinguishes between real and fake images, this project introduces a **similarity-based discriminator**. By assigning a similarity score to pairs of images, the model aims to generate images with improved realism and consistency for the cat and dog classes of the CIFAR-10 dataset.

## Dataset
The project uses the **CIFAR-10 dataset**, focusing only on the **cats** and **dogs** classes. The dataset contains 60,000 32x32 RGB images, with the following distribution for this project:
- Cats: 6,000 images
- Dogs: 6,000 images

## Model Architecture
### Generator
- A convolutional neural network (CNN) designed to generate 32x32 RGB images resembling cats and dogs.

### Discriminator
- Inspired by **Siamese Networks**, the discriminator evaluates similarity between pairs of images, generating a similarity score rather than a binary classification.

## Training Details
- Trained on cats and dogs from the CIFAR-10 dataset.
- **500 epochs** of training with an adaptive learning rate.
- Loss metrics monitored:
  - **Generator Loss**: Measures the quality of generated images.
  - **Discriminator Loss**: Measures the discriminator’s ability to distinguish real vs. generated images.
- **Optimizer**: Adam optimizer with beta values of (0.5, 0.999).

## Results
- **Generated Images**: Gradual improvement in image quality over epochs.
- **Challenges**: Blurriness observed in some generated images.
- **Metrics**:
  - Loss values for generator and discriminator.
  - Visual inspection of generated samples.
