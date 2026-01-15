# MNIST Digit Classification

A neural network implementation for classifying handwritten digits using the MNIST dataset.

## Overview

This project demonstrates building and training an Artificial Neural Network (ANN) using TensorFlow/Keras to classify handwritten digits (0-9) from the MNIST dataset.

## Dataset

- **MNIST**: A dataset of 70,000 handwritten digits (28x28 pixel images)
  - Training set: 60,000 images
  - Test set: 10,000 images
  - Classes: 10 (digits 0-9)

## Model Architecture

The neural network consists of:

1. **Flatten Layer**: Converts 28x28 images to 1D vectors (784 features)
2. **Dense Layer 1**: 128 neurons with ReLU activation
3. **Dense Layer 2**: 32 neurons with ReLU activation
4. **Output Layer**: 10 neurons with Softmax activation (multi-class classification)

```
Input (28x28)
    ↓
Flatten (784)
    ↓
Dense 128 (ReLU)
    ↓
Dense 32 (ReLU)
    ↓
Dense 10 (Softmax)
    ↓
Output (10 classes)
```

## Training Details

- **Loss Function**: Sparse Categorical Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy
- **Epochs**: 25
- **Validation Split**: 20%

## Requirements

- TensorFlow/Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Installation

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn
```

## Usage

Open `main.ipynb` in Jupyter or VS Code and run the cells sequentially to:

1. Load and explore the MNIST dataset
2. Preprocess and normalize the data
3. Build the ANN model
4. Train the model
5. Evaluate accuracy on test set
6. Visualize training performance
