# Neural Networks

This section of the repository contains my implementation for the **Programming Assignment 3:Neural Networks** project, where I designed and trained neural networks to classify **Fashion-MNIST** dataset images.

**Project Status:** 🟡 *Ongoing* – Documentation and visualizations in progress

---

## Overview

In this project, I implemented two types of neural networks to classify Fashion-MNIST images:

- **Feedforward Neural Network (FNN):**  
  A fully connected architecture that takes flattened 28×28 grayscale images as input.

- **Convolutional Neural Network (CNN):**  
  An architecture with convolutional layers optimized for image recognition tasks.

Both networks were tasked with classifying Fashion-MNIST images into **10 clothing categories**.

---

## Key Implementations

### Feedforward Network (`ffn.py`)
- Multiple fully-connected layers with optimized neuron counts
- **ReLU** activation functions
- **Dropout** for regularization 
- Accepts flattened image inputs (784 features)

### Convolutional Network (`cnn.py`)
- Multiple convolutional layers using **kernel**
- **MaxPooling** for spatial downsampling
- **ReLU** activations between layers
- Fully connected layers following conv operations
- **Dropout** for preventing overfitting 
---

## 🔍 Additional Visualizations (Work in Progress)
-  **Kernel visualization** to understand learned features
-  **Feature maps** showing how the CNN processes images
-  **Training loss graphs** for convergence tracking
-  **Correct vs. incorrect classifications** with example visualizations

---

## Tools and Technology 
- **PyTorch** for deep learning model construction
- **Convolutional Neural Networks** for spatial feature extraction
- **MaxPooling** for downsampling and noise reduction
- **Dropout** for regularization
- **ReLU activation** for non-linearity
- **Cross-entropy loss** for multi-class classification

---

## Reinforcement Learning Add-on – *Escape the Castle*

This repo also includes my implementation of a **Reinforcement Learning** project:
- Developed a **model-based Monte Carlo approach** for estimating state values
- Implemented **Q-learning with experience replay**
- Trained agents to **learn optimal navigation strategies**
- Achieved average performance of **8669.4373**, exceeding the assignment benchmark of **8600**

---

## Current Work in Progress
-  Hyperparameter tuning for better accuracy
-  Visual tools for model interpretability
-  Comparative analysis between CNN and FNN performance
-  Documentation of model architecture decisions

---

## Access Policy

As with other projects in this repository, implementation code is stored in a **private repository** to comply with university academic integrity policies.  
Please refer to the main README for instructions on requesting access.

---
