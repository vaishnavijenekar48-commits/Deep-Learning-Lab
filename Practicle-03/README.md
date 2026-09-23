# Practical 3 — Forward Propagation and Backpropagation using TensorFlow/Keras

## Aim

To implement forward propagation and backpropagation using TensorFlow/Keras and analyze the effect of different learning rates and the number of epochs on model performance.

## Dataset

MNIST Handwritten Digit Dataset

## Tools and Libraries Used

- Python
- Google Colab
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

## Steps Performed

1. Loaded the MNIST handwritten digit dataset.
2. Inspected the training and testing dataset.
3. Normalized the pixel values from 0–255 to 0–1.
4. Visualized sample handwritten digit images.
5. Designed a Multilayer Perceptron (MLP) using TensorFlow/Keras.
6. Used a Flatten layer to convert 28 × 28 images into 784 input values.
7. Used two hidden layers with 128 and 64 neurons.
8. Used ReLU activation functions in the hidden layers.
9. Used Softmax activation in the output layer.
10. Compiled the model using the Adam optimizer and sparse categorical crossentropy loss.
11. Trained the model using forward propagation and backpropagation.
12. Tested different learning rates.
13. Compared model performance for different learning rates.
14. Tested different numbers of epochs.
15. Compared model performance for different numbers of epochs.
16. Evaluated the final model using test accuracy.
17. Generated predictions and a confusion matrix.
18. Visualized training/validation accuracy and loss.

## MLP Architecture

```text
Input Image
28 × 28 pixels
     ↓
Flatten
784 values
     ↓
Dense Layer
128 neurons + ReLU
     ↓
Dense Layer
64 neurons + ReLU
     ↓
Output Layer
10 neurons + Softmax
     ↓
Digits 0–9
