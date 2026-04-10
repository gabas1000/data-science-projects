# CNN Depth and Hyperparameter Effects on CIFAR-10

This project investigates how convolutional neural network depth and training hyperparameters affect image classification performance on CIFAR-10.

## Overview

The main goal of this project was to analyze how architectural choices and optimization settings influence CNN accuracy. I built a flexible CNN setup and compared networks with different depths, learning rates, optimizers, pooling methods, and activation functions.

## Methods

- Dataset:
  - CIFAR-10
- Framework:
  - PyTorch
- CNN depth settings:
  - 2 blocks
  - 3 blocks
  - 4 blocks
- Hyperparameters explored:
  - Optimizer: Adam vs SGD
  - Learning rate
  - Batch normalization
  - ReLU vs Leaky ReLU
  - Max pooling vs average pooling
  - Training duration

## Model Design

The CNN used a modular block structure with progressively increasing channel sizes:

`3 → 32 → 64 → 128 → 256`

Each convolutional block included:
- convolution
- optional batch normalization
- activation
- pooling

The model then used:
- flattening
- fully connected layer
- dropout
- final classification layer

## Key Findings

- Increasing CNN depth consistently improved performance when training time was sufficient.
- The 4-block CNN outperformed the 2-block and 3-block versions.
- Longer training was especially important for deeper models.
- Adam and SGD produced similar performance overall, with Adam slightly ahead.
- A moderate learning rate performed best.

## Best Result

Best configuration identified in the project:

- Depth: 4 blocks
- Optimizer: Adam
- Learning rate: 0.001
- Batch normalization: Yes
- Activation: ReLU
- Pooling: Max
- Epochs: 30
- Best test accuracy: **85.17%**

## Example Results

### Effect of depth
- 2 blocks, 10 epochs: 72.86%
- 3 blocks, 10 epochs: 77.66%
- 4 blocks, 10 epochs: 79.94%
- 3 blocks, 30 epochs: 82.62%
- 4 blocks, 30 epochs: 85.17%

### Learning rate comparison (4-block CNN)
- 0.0005: 84.37%
- 0.001: 85.17%
- 0.002: 85.03%

### Optimizer comparison (4-block CNN)
- Adam: 85.17%
- SGD: 84.72%

## Tools Used

- Python
- PyTorch
- NumPy
- Matplotlib

## Files

- `cnn-depth-hyperparameter-effects-cifar10.pdf` — final report for the project

## Notes

This was an academic deep learning project completed at UC San Diego. I am including it here as part of my machine learning portfolio.
