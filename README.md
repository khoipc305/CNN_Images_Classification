# Handwritten Digit Classification using CNN

This project implements a Convolutional Neural Network (CNN) to classify handwritten digits from 0 to 9. The model is built using TensorFlow and Keras.

## Project Structure

```
CNN/
├── cnn.py                    # Main Python script containing the CNN implementation
├── requirements.txt          # Project dependencies
├── digit_dataset/            # Directory containing training and test images
│   ├── train/                # Training image dataset
│   └── test/                 # Test image dataset
└── README.md                 # Project documentation
```

## Requirements

Install dependencies using:
```bash
pip install -r requirements.txt
```

Or install manually:
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

The dataset contains 32x32 grayscale images of handwritten digits (0-9) organized in:
- `digit_dataset/train/` - Training images
- `digit_dataset/test/` - Test images

Image filenames start with their corresponding label (e.g., `0_001.png`, `1_002.png`).

## Usage

Run the CNN training:
```bash
python cnn.py
```

The script will:
1. Load and preprocess images from `digit_dataset/`
2. Normalize pixel values to [0, 1] range
3. Train the model for 10 epochs with batch size 32
4. Evaluate and display test accuracy

## Results

- **Test Accuracy**: ~92%
- **Optimizer**: SGD (Stochastic Gradient Descent)
- **Loss Function**: Sparse Categorical Crossentropy
- **Training Epochs**: 10

## Author

Khoi Pham - CS 4210 Assignment #4
