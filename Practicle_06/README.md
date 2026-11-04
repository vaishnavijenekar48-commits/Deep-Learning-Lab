# Practical 6: CNN-Based Tomato Leaf Disease Classification

## 1. Aim

To design and implement a Convolutional Neural Network (CNN) for image classification using the Tomato Leaf Disease Dataset and classify tomato leaves into different disease categories.

## 2. Introduction

Convolutional Neural Network (CNN) is a deep learning algorithm widely used for image classification and computer vision tasks.

CNN automatically learns important image features such as edges, shapes, textures, and patterns using convolutional layers.

In this practical, a CNN model is developed to identify diseases in tomato leaves using images from the PlantVillage dataset.

The model classifies tomato leaf images into different categories based on their visual characteristics.

## 3. Dataset Used

- **Dataset Name:** PlantVillage Tomato Disease Dataset
- **Dataset Source:** PlantVillage Dataset
- **Source Repository:** https://github.com/spMohanty/PlantVillage-Dataset
- **Image Type:** RGB Images
- **Task:** Multi-Class Image Classification
- **Number of Classes:** 10 Tomato Leaf Categories

## 4. Technologies and Libraries Used

- Python
- Google Colab
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn

## 5. CNN Architecture

The CNN model consists of the following layers:

1. **Convolutional Layer:** Extracts important features from tomato leaf images.
2. **Max Pooling Layer:** Reduces the spatial dimensions of feature maps.
3. **Convolutional Layers:** Learn more complex patterns and image features.
4. **Flatten Layer:** Converts feature maps into a one-dimensional vector.
5. **Dense Layer:** Learns patterns for classification.
6. **Dropout Layer:** Helps reduce overfitting.
7. **Output Layer:** Uses Softmax activation to classify images into disease categories.

## 6. Methodology

The following steps are performed:

1. Download the PlantVillage dataset.
2. Extract tomato disease images from the dataset.
3. Load and preprocess the images.
4. Resize images to 128 × 128 pixels.
5. Normalize pixel values between 0 and 1.
6. Divide the dataset into training, validation, and testing sets.
7. Apply image augmentation to training images.
8. Design and compile the CNN architecture.
9. Train the CNN model using training images.
10. Evaluate the model using testing images.
11. Generate classification reports and confusion matrices.
12. Save the trained CNN model and prediction results.

## 7. Model Configuration

- Image Size: 128 × 128
- Batch Size: 32
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Activation Function: ReLU
- Output Activation: Softmax
- Maximum Epochs: 15
- Early Stopping: Enabled

## 8. Evaluation Metrics

The model performance is evaluated using:

- **Accuracy:** Measures the percentage of correctly classified images.
- **Precision:** Measures how many predicted disease categories are correct.
- **Recall:** Measures how many actual disease images are correctly identified.
- **F1-Score:** Represents the balance between precision and recall.
- **Confusion Matrix:** Shows correct and incorrect predictions for each disease category.

## 9. Expected Outputs

The practical generates:

- Sample tomato leaf images.
- CNN model architecture summary.
- Training and validation accuracy graphs.
- Training and validation loss graphs.
- Test accuracy and loss.
- Classification report.
- Confusion matrix.
- Sample disease prediction.
- Saved trained CNN model.

## 10. Conclusion

In this practical, a Convolutional Neural Network was designed and implemented for tomato leaf disease classification using the PlantVillage dataset.

The CNN model learns visual features from tomato leaf images and classifies them into different disease categories.

The model is evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.

This practical demonstrates how deep learning and computer vision can be applied to agricultural disease detection and image classification.
