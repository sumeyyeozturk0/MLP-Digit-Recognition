# MLP-Digit-Recognition

**Project Overview**
This project aims to build a Multilayer Perceptron (MLP) model from scratch to recognize handwritten digits. As per the assignment requirements, Convolutional Neural Networks (CNNs) and pre-trained models were strictly avoided in order to understand the core mechanics and limitations of the MLP architecture. 

**Dataset and Split**
The model was trained entirely on the standard MNIST dataset. The data was explicitly split into Training, Validation, and Test sets to prevent data leakage and properly evaluate performance.

**Hyperparameters**
* Epochs: 5
* Loss Function: Cross Entropy Loss

**Experiment Results & Distribution Shift (Generalization Gap)**
During the training and validation phases on the standard MNIST dataset, the model achieved a high accuracy of over 96%. However, when the model was tested on real-world data (my own custom handwritten digits drawn on a tablet), it struggled to predict the numbers correctly. 

This experiment perfectly demonstrates **distribution shift**. The MLP architecture evaluates images based on strict pixel-by-pixel spatial mapping. The MNIST dataset consists of heavily pre-processed images where digits are perfectly centered and drawn with a uniform, thick line. In contrast, my custom handwritten digits had thinner strokes and slight off-center alignments. Because MLP models lack the spatial invariance of CNNs, these minor structural differences completely disrupted the model's ability to recognize the digits, highlighting the gap between standardized training data and real-world inputs.
