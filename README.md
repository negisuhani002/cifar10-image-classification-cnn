# CIFAR-10 Image Classification using CNN

## Overview

This project implements a Convolutional Neural Network (CNN) using PyTorch to classify images from the CIFAR-10 dataset into 10 different categories.

The objective is to understand how CNNs learn spatial features from images and use them to perform multi-class image classification.

## Dataset

The project uses the **CIFAR-10 dataset**, which contains 60,000 color images of size 32 × 32 pixels.

- Training images: 50,000
- Testing images: 10,000
- Image channels: 3 (RGB)
- Number of classes: 10

### CIFAR-10 Classes

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

## Technologies Used

- Python
- PyTorch
- Torchvision
- Matplotlib (optional for visualization)

## Data Preprocessing

- Convert images into PyTorch tensors using `ToTensor()`.
- Normalize RGB channels using mean = [0.5, 0.5, 0.5] and standard deviation = [0.5, 0.5, 0.5].
- Load the training and testing datasets using DataLoader.
- Batch size: 64

## CNN Architecture

The model consists of three convolutional blocks followed by fully connected layers.

### Convolutional Layers

| Layer | Configuration |
|---|---|
| Conv Layer 1 | 3 → 32 channels, 3 × 3 kernel |
| Activation | ReLU |
| Max Pooling | 2 × 2 |
| Conv Layer 2 | 32 → 64 channels, 3 × 3 kernel |
| Activation | ReLU |
| Max Pooling | 2 × 2 |
| Conv Layer 3 | 64 → 128 channels, 3 × 3 kernel |
| Activation | ReLU |
| Max Pooling | 2 × 2 |

### Fully Connected Layers

- Flatten the extracted feature maps.
- Linear layer: 2048 → 256 neurons.
- ReLU activation.
- Output layer: 256 → 10 neurons.

**Architecture:** Three convolutional layers followed by two fully connected layers.

## Model Training

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Number of Epochs: 10
- Batch Size: 64

The model is trained using forward propagation, loss calculation, backpropagation, and optimizer updates.

Training loss is monitored across epochs to observe the learning progress.

## Model Evaluation

The model is evaluated on the CIFAR-10 test dataset.

- Evaluation metric: Accuracy
- Test Accuracy: **75.55%**

## Key Learnings

- Understanding CNN architecture and its components.
- Working with convolutional and pooling layers.
- Understanding channels and feature maps.
- Learning how spatial dimensions change through pooling.
- Flattening feature maps before fully connected layers.
- Training a multi-class image classifier using PyTorch.
- Using CrossEntropyLoss and the Adam optimizer.
- Evaluating a CNN using test accuracy.

## Repository Structure

```text
cifar10-image-classification-cnn/
│
├── README.md
└── cifar10_cnn_classifier.ipynb
```

## Conclusion

This project demonstrates the implementation of a CNN for multi-class image classification using PyTorch.

The model achieved a test accuracy of 75.55% after 10 epochs of training. It provided practical experience with convolutional layers, feature extraction, pooling, fully connected layers, and the CNN training process.
