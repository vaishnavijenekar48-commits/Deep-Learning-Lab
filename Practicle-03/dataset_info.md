# Dataset Information

## Dataset Name
MNIST Handwritten Digit Dataset

## Source
TensorFlow/Keras built-in dataset

## Description
MNIST is a dataset of handwritten digit images containing
digits from 0 to 9.

## Number of Samples
70,000

- Training samples: 60,000
- Testing samples: 10,000

## Number of Classes
10

Classes:
- 0
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9

## Image Size
28 × 28 pixels

## Image Type
Grayscale

## Pixel Value Range
0–255 before normalization.

## Normalized Pixel Range
0–1 after normalization.

The pixel values were converted to float32 and divided by 255.

## Input Size
Each image contains:

28 × 28 = 784 pixels

The Flatten layer converts each 28 × 28 image into
784 input values for the MLP.

## Train-Test Split
The MNIST dataset already provides separate training
and testing datasets.

- Training: 60,000 images
- Testing: 10,000 images

During model training, 10% of the training data was used
as validation data.

## Preprocessing
1. Converted pixel values to float32.
2. Normalized pixel values from 0–255 to 0–1.
3. Flattened the images using the Flatten layer.

## Purpose in This Practical
The MNIST dataset was used to implement forward propagation
and backpropagation using a Multilayer Perceptron (MLP).

It was also used to analyze the effect of different learning
rates and numbers of epochs on model performance.

## Evaluation
The model was evaluated using:

- Accuracy
- Loss
- Confusion Matrix
- Training and Validation Accuracy
- Training and Validation Loss
