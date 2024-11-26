# Handwriting Number Recognition Using PyTorch

This project implements a Convolutional Neural Network (CNN) for recognizing handwritten digits from the MNIST dataset. The architecture is designed for simplicity and efficiency while maintaining accuracy.

Dataset
MNIST Dataset:
60,000 training images and 10,000 test images of handwritten digits (0–9).  
Grayscale images of size 28x28.  
# Model Architecture

## Convolutional Layers (with padding to maintain spatial dimensions):  

Conv1: Input: 1 channel, Output: 8 channels, Kernel: 3x3, Padding: 1.  
Conv2: Input: 8 channels, Output: 24 channels, Kernel: 3x3, Padding: 1.  
Conv3: Input: 24 channels, Output: 48 channels, Kernel: 3x3, Padding: 1.  

## Pooling:

Each convolutional layer is followed by a 2x2 max pooling operation with a stride of 2.  

## Fully Connected Layers:

FC1: Input: Flattened from 48x3x3, Output: 160 neurons.  
FC2: Output: 60 neurons.  
FC3: Output: 10 neurons (corresponding to the digits 0–9).  

## Activation Functions:

ReLU activation for all intermediate layers.  
LogSoftmax applied to the final output for classification.  
