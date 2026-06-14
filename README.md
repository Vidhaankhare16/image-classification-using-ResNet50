# CIFAR-10 Image Classification

## Overview
This project implements a deep learning model to classify images from the CIFAR-10 dataset. The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class. The project explores two different neural network architectures:
1. A simple feedforward neural network
2. A more complex model using ResNet50 as a feature extractor

## Dataset
The CIFAR-10 dataset is downloaded from Kaggle and contains the following classes:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## Requirements
To run this project, you'll need:
- Python 3.x
- TensorFlow/Keras
- NumPy
- Pandas
- Matplotlib
- OpenCV
- Kaggle API (for dataset download)
- py7zr (for extracting 7z archives)

## Installation
```bash
pip install tensorflow numpy pandas matplotlib opencv-python kaggle py7zr
```
## Project Structure

### Data Preparation
- Downloads dataset from Kaggle
- Extracts compressed files
- Loads and preprocesses images
- Splits data into training and test sets

### Model Architectures

#### Simple Neural Network
- Flatten input layer
- Dense layers with ReLU activation
- Output layer with softmax activation

#### ResNet50-based Model
- Upsampling layers to increase image size
- ResNet50 as feature extractor
- Additional dense layers with dropout for regularization

### Training
- Both models are trained for 20 epochs
- Uses Adam/RMSprop optimizer
- Implements sparse categorical crossentropy loss

### Evaluation
- Accuracy metrics on test set
- Training/validation loss and accuracy plots

## Results

### Simple Neural Network
- Final validation accuracy: ~37.8%
- Shows basic learning capability but limited performance

### ResNet50-based Model
- Final test accuracy: ~94.2%
- Demonstrates significant improvement using transfer learning

## Usage
1. Set up Kaggle API credentials
2. Run the notebook cells sequentially to:
   - Download and extract data
   - Preprocess images
   - Train models
   - Evaluate performance

## Visualizations
The project includes plots showing:
- Training vs validation loss over epochs
- Training vs validation accuracy over epochs
<img width="547" height="413" alt="download" src="https://github.com/user-attachments/assets/bc8ab69f-4036-4e32-be9f-ff0891601c4a" />
<img width="547" height="413" alt="download (1)" src="https://github.com/user-attachments/assets/e23a810f-009f-4255-8f26-e8b4cabc973d" />





## Future Improvements
- Experiment with different architectures
- Try more advanced data augmentation
- Implement learning rate scheduling
- Fine-tune hyperparameters

## Acknowledgments
- Dataset provided by Kaggle CIFAR-10 competition
- ResNet50 pre-trained weights from ImageNet
