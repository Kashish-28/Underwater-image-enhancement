**Underwater Image Enhancement Using GANs**

**Overview**
This project aims to enhance underwater images using Generative Adversarial Networks (GANs). The goal is to improve image quality by removing distortions and enhancing visibility. The project leverages TensorFlow and various image processing libraries to build, train, and evaluate GAN models.

**Project Structure**
notebook.ipynb - The main Jupyter/Colab notebook with all the code for data processing, model training, and evaluation.
dataset/ - Directory containing training datasets (trainA and trainB).
generator_final.keras - Saved model after training.

**Models**
**Generator**
The generator model builds an enhanced version of an underwater image. It consists of several convolutional and deconvolutional layers to perform image translation.

**Discriminator**
The discriminator model distinguishes between real and generated images, guiding the generator to produce more realistic outputs.

**Refinement Network**
A refinement network further enhances the generated images, improving quality and detail.

**Data Handling**
**Dataset**
File Structure:
dataset/trainA - Low-quality input images.
dataset/trainB - High-quality target images.

**Preprocessing**
Images are resized to 256x256 pixels.
Pixel values are normalized to the range [-1, 1].

**Training**
The training process involves:
Training the discriminator to differentiate between real and generated images.
Training the generator to produce images that the discriminator cannot distinguish from real ones.
**Hyperparameters**
Epochs: 50
Batch Size: 1

**Evaluation**
The following metrics are used to evaluate image quality:
SSIM (Structural Similarity Index)
PSNR (Peak Signal-to-Noise Ratio)
MSE (Mean Squared Error)
VIFP (Visual Information Fidelity in Pixel domain)

**Visualization**
Original vs. Enhanced images.
Histograms and structural similarity maps.
