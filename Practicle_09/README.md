# Practical 9: Image Classification Using Pre-trained Vision Transformer (ViT) and CNN

## Aim
To perform image classification using a pre-trained Vision Transformer (ViT) model and compare its performance with a pre-trained Convolutional Neural Network (CNN).

## Introduction
Image classification is a computer vision task in which a model identifies and assigns labels to images.

In this practical, two pre-trained deep learning architectures are used:
- **Vision Transformer (ViT):** Uses self-attention mechanisms to understand relationships between different image patches.
- **CNN (ResNet18):** Uses convolutional layers to extract spatial features from images.

Both models use pre-trained ImageNet weights and are adapted for CIFAR-10 classification by replacing their classification heads.

## Dataset
**CIFAR-10 Dataset**

CIFAR-10 contains 60,000 colour images belonging to 10 different classes.

The classes include:
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

For this practical:
- Training samples: 5,000
- Testing samples: 1,000
- Image size: 224 × 224 pixels after resizing.

## Technologies Used
- Python
- Google Colab
- PyTorch
- Torchvision
- Hugging Face Transformers
- Scikit-learn
- Matplotlib
- NumPy

## Methodology

1. Import the required Python libraries.
2. Download the CIFAR-10 dataset.
3. Resize images to 224 × 224 pixels.
4. Normalize images using ImageNet mean and standard deviation.
5. Load the pre-trained ResNet18 CNN model.
6. Load the pre-trained Vision Transformer model.
7. Freeze the pre-trained feature extraction layers.
8. Replace the classification heads with new layers for 10 classes.
9. Train both models on the training dataset.
10. Evaluate both models using the testing dataset.
11. Compare their classification accuracy and other performance metrics.
12. Visualize the model accuracy comparison.

## Models Used

### 1. CNN – ResNet18
ResNet18 is a convolutional neural network that uses residual connections to improve deep network training. It extracts image features using convolutional layers.

### 2. Vision Transformer – ViT
ViT divides an image into small patches and processes them using transformer encoder layers and self-attention mechanisms.

## Evaluation Metrics
The models are evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Classification report

## Expected Outputs
- Training loss and accuracy for both models.
- Test accuracy of ResNet18.
- Test accuracy of ViT.
- Classification reports.
- CNN vs ViT accuracy comparison graph.
- Sample image predictions from both models.
- Saved trained model weights.

## Conclusion
In this practical, image classification is performed using two pre-trained deep learning architectures: ResNet18 CNN and Vision Transformer.

Their performance is compared using test accuracy, precision, recall, and F1-score. The practical demonstrates how CNNs and transformer-based architectures can be applied to image classification tasks.

The model with higher test accuracy performs better on the selected test subset. Actual results depend on training conditions and hardware.
