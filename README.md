# Deep Learning Nanodegree @ Udacity
Udacity Deep Learning Nanodegree - Project 4, face-generation


This project implements a Generative Adversarial Network (GAN) to generate simulated handwritten images resembling those found in the MNIST dataset as well as generating simulated celebrity face images after training on a dataset of real celebrity images.

This project takes in raw data in the form of images and preprocesses or (resizes them to work with the model). Additionally, the model consists of generator and discriminator functions. The generator function (G) is designed to generate fake images resembling the raw data inputs which are later fed into the discriminator simultaneously with real images.  The discriminator function (D) attempts to distinguish real images from simulated or (fake) images produced by the generator and the real images from the raw data.

The G function generates simulated images that are fed along with real images to the D function until D is unable to determine fake images from real images. This is called convergence a point at which the generator function has successfully achieved its goal of producing realistic looking simulated images.

The G & D loss functions are obtained by applying a sigmoid activation function to each. This is followed by an optimization process where the training variables are split into G & D groups. These two functions are optimized using the AdamOptimizer while implementing a beta1 (exponential decay rate for the 1st moment in the optimizer)  and learning rate while training both G & D.  Training of the algorithm is considered accomplished when the validation losses of the two algorithms converge.

