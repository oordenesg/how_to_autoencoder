# how_to_autoencoder

Autoencoders are a class of neural network that attempt to recreate the input
as their target using back-propagation. An autoencoder consists of two parts; an **encoder** and a **decoder**. The encoder will read the input and compress it to a compact representation, and the decoder will read the compact representation and recreate the input from it. In other words, the autoencoder tries to learn the identity function by minimizing the reconstruction error. They have an inherent capability to learn
a compact representation of data. They are at the center of deep belief networks
and find applications in image reconstruction, clustering, machine translation,
and much more.

This exercise aims to test your understanding of autoencoder architecture, and how it can be used to denoise an image. We will build a convolutional autoencoder. Combining your knowledge of a Vanilla/Denoising Autoencoder and Convolutional Networks.

## AutoEncoder  Architecture
The number of hidden units in the autoencoder is typically less than the number of input (and output) units. This forces the encoder to learn a compressed representation of the input, which the decoder reconstructs. If there is a structure in the input data in the form of correlations between input features, then the autoencoder will discover some of these correlations, and end up learning a low-dimensional representation of the data similar to that learned using principal component analysis (PCA).

Once trained
* We can discard **decoder** and use **Encoder** to optain a compact representation of input.
* We can cascade Encoder to a classifier.

The encoder and decoder components of an autoencoder can be implemented using either dense, convolutional, or recurrent networks, depending on the kind of data that is being modeled.
