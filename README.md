# MLP-Digit-Recognition

# MLP Digit Recognition

**Project Overview & Model Architecture**
This project aims to build a Multilayer Perceptron (MLP) model from scratch to recognize handwritten digits. As per the assignment requirements, Convolutional Neural Networks (CNNs) and pre-trained models were strictly avoided.
*   **Architecture:** The model includes 2 hidden layers.
*   **Activation Function:** ReLU
*   **Loss Function:** Cross Entropy Loss
*   **Optimizer:** Adam 

**Dataset and Split**
The model was trained entirely on the standard MNIST dataset. The data was explicitly split into Training, Validation, and Test sets to prevent data leakage.

**Experiment 1 - Basic MLP Model Results**
*   **Training Time:** [SÜREYİ BURAYA YAZ, Örn: 45 seconds]
*   **Training Loss:** [DEĞERİ YAZ, Örn: 0.1234]
*   **Validation Loss:** [DEĞERİ YAZ]
*   **Training Accuracy:** [DEĞERİ YAZ, Örn: %97.5]
*   **Validation Accuracy:** [DEĞERİ YAZ]
*   **Test Accuracy:** [DEĞERİ YAZ]
*(Note: Training and validation loss/accuracy graphs are generated and visualized within the project notebook).*

**Experiment Results & Distribution Shift (Generalization Gap)**
During the training and validation phases on the standard MNIST dataset, the model achieved high accuracy. However, when tested on real-world data (my custom handwritten digits drawn on a tablet), it struggled to predict the numbers correctly. 

This experiment perfectly demonstrates **distribution shift**. The MLP architecture evaluates images based on strict pixel-by-pixel spatial mapping. The MNIST dataset consists of heavily pre-processed images where digits are perfectly centered and drawn with a uniform, thick line. In contrast, my custom handwritten digits had thinner strokes and slight off-center alignments. Because MLP models lack the spatial invariance of CNNs, these minor structural differences completely disrupted the model's ability to recognize the digits, highlighting the generalization gap.
