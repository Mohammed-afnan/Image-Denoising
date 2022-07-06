# Image-Denoising
The noise in the image has been removed using Autoencoders. Here I have presented the difference between the Basic Autoencoders, Variational Autoencoders and Convolutional Autoencoders
# INTODUCTION
Deep learning-based autoencoders have progressed significantly in recent years as a result of remarkable advances in the field of data science. Autoencoders are a subset of unsupervised learning techniques, which are a sort of machine learning approach. Picture denoising, image production, dimensionality reduction, image colorization, and feature extraction are just a few of the applications where autoencoders are utilised. Autoencoders are used in a variety of ways in all of the applications. We employ neural networks to conduct autoencoders in such a manner that the neural network has a bottleneck that imposes a compressed knowledge representation of the original input.
To put it another way, see Autoencoders as a sandwich, with the lower bread acting as an encoder, the material in the middle acting as a bottleneck, and the top bread acting as a decoder. As a result, autoencoders must be symmetric.

The hidden layer between the encoder and decoder layers is known as the latent space. It's a compressed representation of the data being input. It may be used to learn data characteristics and to develop a simplified data representation for analysis. In the latent space representation of a variational autoencoder, the encoder network will convert the input samples into two parameters, which are designated mean and variance. There are no such parameters in latent space for basic autoencoders and convolutional autoencoders. There are no such parameters in latent space for basic autoencoders and convolutional autoencoders.

The main distinction between an autoencoder and a variational encoder is the latter's capacity to supply continuous data or a range of data in the latent space, which aids in the generation of new data or images.

Variational autoencoders are well-known for their ability to generate the supplied input. There are two types of losses: reconstruction loss and KL-divergence loss. We sum both losses in VAE and strive to reduce the overall loss.
# Addition of noise to data in real world:
An image is NXM dimensional array with N*M pixels that ranges from 0 (for white) to 255(for black), the random variation of color information in pixels of an image will lead to an addition of noise in that image.
Even when we compress the memory of the image, sometimes we encounter blurry ness in that image so with the help of this image de-noising phenomenon we can recover the details of images
#Auto Encoders:
Autoencoders were initially presented as a neural network design that primarily focuses on encoding, in which the input data is compressed and then rebuilt using a decoder. Autoencoders are similar to Principal Component Analysis in that they have the same generalized or latent representation as PCAs and are similarly an unsupervised learning approach that does not require labels.

# Variational Auto Encoders:
VAEs are neural networks that receive input data and convert it to its latent representation, which has mean and variance as hidden layers. These two hidden layers are then transformed to sampled latent vectors, through which the original data is rebuilt. In VAE, we must concentrate on the two losses it causes. Here fig (3) shows the variational autoencoder where the encoder samples the input to its latent space representation and we have a decoder which samples the latent space and reconstructs the input image.
![image](https://user-images.githubusercontent.com/64902552/177459315-222b0771-7d27-419e-a40a-867c8ec06916.png)
# Convolutional Auto Encoders
Convolutional neural networks excel in a variety of tasks, therefore it's only reasonable to consider them for picture denoising. In convolutional autoencoders, max-pooling layers are used in conjunction with convolutional layers to compress the size of the original input and represent it in a latent space, and up-sampling is used in conjunction with convolutional layers to reconstruct the original input from the latent space at the decoder side. We can also use a transposed convolution layer instead of up-sampling, but the up-sampling method reduces the number of training parameters in the network and is suitable for a wide range of problems, especially when the training data is sufficient.

Using Python built-in methods, import essential libraries such as NumPy, TensorFlow, Keras, and Matplotlib for all three types of autoencoders. The mnist data was utilised in this experiment. You can also use any other information.
Fig shows the architecture of our model where it consists of an encoder given with input image (256,256,3) which gives a latent space representation and the decoder decodes the latent space representation to give the original input image back. 
![image](https://user-images.githubusercontent.com/64902552/177459372-fd502e27-619a-4c17-883a-0fbc831a39c4.png)
