# Neural Networks: Convolutional NN, FeedForward N, MNSIT dataset

## Results & Analysis

Both models were successfully trained to classify 28x28 grayscale clothing images from the Fashion-MNIST dataset into 10 categories. Final performance metrics:

- **Feedforward Neural Network (FFN)**  
  - Architecture: 2 hidden layers with ReLU activations and dropout  
  - Trained over **35 epochs**  
  - **Final Test Accuracy: 88.16%**

- **Convolutional Neural Network (CNN)**  
  - Architecture: 2 convolutional layers (with max pooling), 2 dense layers, dropout  
  - Trained over **10 epochs**  
  - **Final Test Accuracy: 91.28%**

Both models met the **≥ 80% accuracy requirement**, and loss graphs demonstrated convergence with minimal overfitting.

---

## Tools & Technologies Used

- **Python**
- **PyTorch**: Model building, training, and evaluation
- **NumPy**: Matrix manipulation and numeric operations
- **Matplotlib**: Plotting training loss and visualizing predictions
- **OpenCV**: Preprocessing and handling input image for kernel application
- **SciPy**: Applied filters to visualize kernel effects

---

## Neural Network Architectures

### 1. Feedforward Neural Network (`ffn.py`)
- Input: Flattened 784-dimensional vector (28×28 grayscale image)
- Hidden Layers:  
  - Layer 1: x neurons, ReLU, Dropout  
  - Layer 2: x neurons, ReLU, Dropout  
- Output Layer: 10 neurons
- Dropout Rate: 20%  
- Optimizer: Adam with learning rate   
- Loss Function: Categorical Cross Entropy Loss

### 2. Convolutional Neural Network (`cnn.py`)
- Input: 28×28 grayscale image
- Layers:
  - Conv Layer 1: filters, kernel, ReLU, MaxPool
  - Conv Layer 2: filters, kernel, ReLU, MaxPool
  - Flattened followed by 2 Dense layers with ReLU and Dropout
- Dropout Rate: 20%
- Optimizer: Adam with learning rate
- Loss Function: Categorical Cross Entropy Loss

---

## Project Overview

In this project, I implemented two types of neural networks to tackle image classification using the Fashion-MNIST dataset. The goal was to explore the differences in performance between a basic feedforward architecture and a more complex convolutional architecture optimized for visual features.

Both models were evaluated on a held-out test set of 10,000 images and achieved performance exceeding the baseline requirement of 80% test accuracy.

---

## Dataset: Fashion-MNIST

Fashion-MNIST is a drop-in replacement for MNIST but with more complex image content. The dataset includes:

- 60,000 training images and 10,000 test images
- 28x28 grayscale images
- 10 clothing categories: `T-shirt/top`, `Trouser`, `Pullover`, `Dress`, `Coat`, `Sandal`, `Shirt`, `Sneaker`, `Bag`, `Ankle boot`

---

## Problem Statement

The objective was to design, train, and compare two models to classify images from Fashion-MNIST. The core challenges involved:

1. Building an efficient and regularized **FFN** model
2. Designing a convolutional architecture to exploit spatial patterns
3. Achieving test accuracy above 80% for both models
4. Visualizing kernel effects and feature maps for interpretability

---

## Evaluation & Metrics

- **Accuracy**: Calculated as total correct predictions / total test samples
- **Loss Tracking**: Epoch-wise logging of training loss
- **Sample Predictions**: Visual inspection of correct and incorrect classifications for both models
- **Kernel Visualization**: Plotted kernels from the first conv layer after training
- **Feature Maps**: Applied learned kernels to an external image for interpretability

---

## Plot Deliverables

All required visualizations were generated and exported:
- `loss_comparison.png`: Loss curves of FFN and CNN
- `kernel_grid.png`: Learned convolutional filters (1st layer)
- `image_transform_grid.png`: CNN feature maps on sample image
- `*_correct.png` and `*_incorrect.png`: Example classifications
---

## Academic Integrity Notice

This project was completed as part of a university assignment and is stored in a **private repository** to comply with academic integrity policies.

If you're working on a similar project and want to collaborate, ask questions, or learn more about the implementation **(without code sharing)**, feel free to reach out. Happy to help explain concepts, architectures, and training strategies.

 **No code will be shared for coursework requests.**

