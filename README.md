# CNN Images Classification

A Convolutional Neural Network (CNN) implementation using TensorFlow and Keras to classify 32x32 images of handwritten digits (0-9).

## Overview

This project trains a CNN model to recognize handwritten digits with **93.54% test accuracy**. The model uses convolutional layers, max pooling, and dense layers to extract features and classify images.

## Requirements

- Python 3.x
- TensorFlow
- NumPy
- Pillow (PIL)

Install dependencies:
```bash
pip install tensorflow numpy pillow
```

## Model Architecture

- **Conv2D Layer**: 32 filters, 3x3 kernel, ReLU activation
- **MaxPooling2D**: 2x2 pool size
- **Flatten Layer**: Converts feature maps to 1D vector
- **Dense Layer**: 64 neurons, ReLU activation
- **Output Layer**: 10 neurons (digits 0-9), Softmax activation

## Dataset

The model expects images in the following structure:
```
digit_dataset/
├── train/
└── test/
```

Images should be 32x32 grayscale handwritten digits.

## Usage

Run the training script:
```bash
python cnn.py
```

The model will:
1. Load and preprocess images
2. Normalize pixel values (0-1 range)
3. Train for 10 epochs with batch size 32
4. Output test accuracy

## Results

- **Test Accuracy**: 93.54%
- **Training**: 10 epochs, SGD optimizer
- **Loss Function**: Sparse Categorical Crossentropy

## Author

Khoi Pham - CS 4210 Assignment #4
