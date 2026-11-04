# Practical 7: Transfer Learning Using Pre-trained CNN Models

## 1. Aim

To implement transfer learning using pre-trained AlexNet, VGG16, ResNet50, and EfficientNetB0 models for image classification and compare their performance using appropriate evaluation metrics.

## 2. Introduction

Transfer Learning is a deep learning technique in which a model trained on a large dataset is reused for a different but related task.

Instead of training a CNN model from scratch, we use pre-trained models that have already learned useful image features from the ImageNet dataset.

In this practical, four pre-trained CNN architectures are implemented using the CIFAR-10 dataset.

The final classification layers of these models are replaced with new layers to classify images into 10 categories.

## 3. Models Implemented

### A. AlexNet
AlexNet is a deep CNN architecture that uses convolutional and pooling layers to extract image features. It is one of the important architectures in the development of deep learning for image classification.

### B. VGG16
VGG16 is a CNN architecture that uses multiple 3 × 3 convolutional filters to learn image features through a deep network.

### C. ResNet50
ResNet50 uses residual connections or skip connections to improve the training of deep neural networks and address the vanishing gradient problem.

### D. EfficientNetB0
EfficientNetB0 is an efficient CNN architecture that balances network depth, width, and image resolution to achieve good performance with computational efficiency.

## 4. Dataset Information

- **Dataset Name:** CIFAR-10
- **Source:** TensorFlow / Toronto University dataset
- **Total Images:** 60,000
- **Training Images:** 50,000
- **Testing Images:** 10,000
- **Image Size:** 32 × 32 pixels
- **Image Type:** RGB
- **Number of Classes:** 10

For this experiment, a stratified subset of 10,000 training images and 2,000 testing images is used to reduce computational time.

## 5. Technologies and Libraries Used

- Python
- Google Colab
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn

## 6. Methodology

The following steps are performed:

1. Download the CIFAR-10 dataset.
2. Load pre-trained AlexNet, VGG16, ResNet50, and EfficientNetB0 models.
3. Resize images to 224 × 224 pixels.
4. Normalize images using ImageNet mean and standard deviation.
5. Select a stratified training and testing subset.
6. Load ImageNet-pretrained model weights.
7. Freeze the pre-trained feature extraction layers.
8. Replace the final classification layer with a new 10-class output layer.
9. Train the new classification layers.
10. Evaluate all four models using the testing dataset.
11. Compare accuracy, precision, recall, F1-score, and training time.
12. Visualize the results using graphs and confusion matrices.

## 7. Model Configuration

| Parameter | Value |
|---|---|
| Input Image Size | 224 × 224 |
| Batch Size | 32 |
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Loss Function | Cross Entropy |
| Epochs | 3 |
| Output Classes | 10 |
| Pre-trained Weights | ImageNet |
| Transfer Learning Type | Feature Extraction |

## 8. Evaluation Metrics

The following metrics are used to compare the four models:

- **Accuracy:** Measures the percentage of correctly classified images.
- **Precision:** Measures the correctness of positive class predictions.
- **Recall:** Measures how many actual class samples are correctly identified.
- **F1-Score:** Represents the balance between precision and recall.
- **Training Time:** Measures the time required to train the classification layer.

Confusion matrices are also generated to analyze classification errors.

## 9. Expected Outputs

The practical generates:

- Sample CIFAR-10 images.
- Pre-trained model architecture.
- Training loss graphs.
- Accuracy comparison graph.
- Precision, recall, and F1-score comparison.
- Training time comparison.
- Confusion matrices for all four models.
- Classification reports.
- Best-performing model identification.
- Saved model classification heads and prediction results.

## 10. Conclusion

In this practical, transfer learning is implemented using four pre-trained CNN architectures: AlexNet, VGG16, ResNet50, and EfficientNetB0.

The models use ImageNet-pretrained weights and are adapted to classify images from the CIFAR-10 dataset.

Their performance is compared using accuracy, precision, recall, F1-score, and training time.

This practical demonstrates how transfer learning can reuse previously learned image features to solve new image classification problems while reducing the need to train an entire deep learning model from scratch.

The best-performing architecture is identified based on the experimental evaluation results.
