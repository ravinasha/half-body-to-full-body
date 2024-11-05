Pix2Pix GAN Image Translation

This project implements a Pix2Pix GAN (Generative Adversarial Network) model using TensorFlow and Keras for image-to-image translation. The model consists of a generator and discriminator network trained together to perform tasks such as generating modified images based on input images.

Project Structure

- generator: Folder to save generator model weights.
- discriminator: Folder to save discriminator model weights.
- Training images are placed in /content/train1 and /content/train2 directories.

 Model Overview

- Generator: The generator model is an encoder-decoder network that maps input images to output images.
- Discriminator: The discriminator model classifies pairs of input and output images as real or fake.
- Loss Functions:
  - generator_loss: Combines GAN loss and L1 loss to ensure realism and similarity to the target image.
  - discriminator_loss: Binary cross-entropy loss to classify real vs. generated images.

