# lca_dehaze
- Light Convolutional AutoEncoder for Dehazing of Images
- Python Implementation of research paper titled **'LCA-NET: Light Convolutional Autoencoder for Image Dehazing'**
- Research Paper citing: https://doi.org/10.48550/arXiv.2008.10325
- Research Paper can be found at: https://arxiv.org/pdf/2008.10325

- To train this implementation, the model trains on O-Haze dataset, which can be found on the following link: https://data.vision.ee.ethz.ch/cvl/ntire18/o-haze/
- NOTE: In the paper, the authors trained the model on a combination of custom images and images from RESIDE dataset. However, this model was trained on O-Haze dataset 2018, provided by New Trends in Image Restoration (NTIRE), which which includes 45 pairs of outdoor scenes featuring the same visual content captured in both hazy and haze-free conditions, under identical illumination parameters.

* Autoencoders are unsupervised machine learning algorithms consisting of neural networks attempting to learn the efficient data generating probability distribution of an unlabeled dataset.  The main idea of an Autoencoder is to learn the most contributing and relevant features through data compression. Autoencoders consists of three main parts:
1. Encoders: The encoder network processes the input image using convolutional layers and pooling operations to produce a low dimensional latent space which is a feature representation of the image.
2. Latent Space: Latent space is a low-dimensional feature representation of the content of the input image, compressed by the Encoder network
3. Decoders: The third and final part, decoder network takes the low-dimensional latent space and upscales the image back to the original input size using deconvolutional layers

* For training, just like the paper, we are utilising Mean Squared Error (MSE) loss, along with Adam Optimiser algorithm
