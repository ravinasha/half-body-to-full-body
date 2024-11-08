# Pix2Pix Image-to-Image Translation Model

This project implements a Pix2Pix model for image-to-image translation using TensorFlow and Keras. Pix2Pix is a type of Generative Adversarial Network (GAN) that performs conditional image generation. In this implementation, the generator learns to translate input images to target images, while the discriminator learns to distinguish real images from generated ones.

# Project Structure

- build_generator : Builds the generator model, using an encoder-decoder architecture.
- build_discriminator : Builds the discriminator model, using a convolutional neural network to differentiate between real and generated images.
- generator_loss : Calculates the generator's loss, including binary cross-entropy and L1 loss.
- discriminator_loss : Calculates the discriminator's loss using binary cross-entropy.
- train_step : Defines a single training step for both generator and discriminator.

# Requirements

Install the necessary libraries using the following command:
pip install tensorflow numpy matplotlib


# Model Training

1. Data Preparation:
   - Place your input images in input_folder and target images in target_folder.
   - Each folder should contain images resized to 256x256 pixels.

2. Train the Model :
   - Run the training script to start training the Pix2Pix model. The model trains for 700 epochs by default.
   - Adjust epochs, batch_size and lambda_l1 for custom configurations.

3. Save Model Weights :
   - After training, the generator and discriminator weights are saved in `/content/generator` and `/content/discriminator`, respectively.


# Image Generation

After training, you can generate images using the trained generator:

1. Load a test image.
2. Use generator.load_weights to load the pre-trained generator model.
3. Generate the output image and display it using matplotlib.
