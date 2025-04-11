# Low-Light Image Enhancement

## Overview
This repository contains the implementation of the PixelWarrior model, a deep learning model designed for enhancing low-light images. This project combines the strengths of the UNet architecture with Multi-Layer Perceptron (MLP) blocks to improve image quality and visibility in low-light conditions.

## Model Architecture
The PixelWarrior Architecture consists of the following components:
1. **UNet Architecture:** A symmetric encoder-decoder structure with skip connections to capture both spatial and contextual information.
2. **MLP Blocks:** Enhance feature representation with convolutional layers followed by GELU and Sigmoid activations.
3. **Downsampler and Upsampler:** Reduce and restore spatial dimensions of the input image to facilitate high-level feature extraction and apply these features to the original resolution.

## Training
The model is trained with the following setup:
- **Loss Function:** Mean Squared Error (MSE)
- **Optimizer:** Adam with an initial learning rate of 0.0001
- **Learning Rate Scheduler:** CosineAnnealingLR
- **Mixed Precision Training:** Utilizes PyTorch’s autocast and GradScaler for faster computations and reduced memory usage.

## Results
The PixelWarrior Model successfully enhances low-light images, providing high-quality outputs with improved visibility. The combination of UNet architecture and MLP blocks allows the model to capture intricate details and enhance images effectively. Achieved an average psnr of 21 on training dataset with a batch size of 4.

## Model Weights 
Here is the drive for the weights 
- [Weights](https://drive.google.com/file/d/1qdkIVcsLLzZ-K9s9mFAKP_MDnAbKG_ct/view?usp=sharing)

## Reference
The model architecture and training methodology are based on the research presented in the following paper:
- [Research Paper](https://arxiv.org/pdf/2404.14248)


