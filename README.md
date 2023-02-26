# Pic-Match

Author: Samson Bakos

This project is designed as an app platform using Dash, with the intention of taking any two input images and determining if they are images of the same subject. 

The backend of this project is a Siamese Network, Using DenseNet as a general feature extractor and comparing the transformed features of the input images using contrastive loss. This loss is mapped to a prediction probability, corresponding to whether or not the input images are of the same thing.

This project is trained using the [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) dataset. This dataset is used only for the purpose of creating labelled image pairs, with the trained weights of DenseNet being maintained, as the feature extraction of DenseNet is more general than what is possible with this dataset. Because the application is intented for general classification and not specific to the 10 classes present in CIFAR, it is more sensible to use DenseNet's more robust extraction.

This procedure could be revisited using a larger, more diverse dataset. However, because this project was trained locally, a smaller dataset is used for image pairs to reduce computational costs. This implementation is sufficient for proof of concept, and could easily be enhanced by applying a larger dataset and more computational resources.
