# Dataset Information – Transfer Learning Model Comparison

## 1. Dataset Name

CIFAR-10 Image Classification Dataset

## 2. Dataset Source

- **Dataset Name:** CIFAR-10
- **Source:** University of Toronto
- **Official Website:** https://www.cs.toronto.edu/~kriz/cifar.html
- **Download Method:** PyTorch Torchvision Dataset API
- **Image Format:** RGB Images
- **Image Size:** 32 × 32 pixels
- **Total Images:** 60,000

## 3. Dataset Description

CIFAR-10 is a widely used image classification dataset containing 60,000 color images divided into 10 different classes.

The dataset contains 50,000 training images and 10,000 testing images.

It is used to train and evaluate deep learning models for object recognition and image classification.

## 4. Dataset Categories

The CIFAR-10 dataset contains the following 10 classes:

| No. | Class Name |
|---|---|
| 1 | Airplane |
| 2 | Automobile |
| 3 | Bird |
| 4 | Cat |
| 5 | Deer |
| 6 | Dog |
| 7 | Frog |
| 8 | Horse |
| 9 | Ship |
| 10 | Truck |

## 5. Dataset Download Code

The dataset is downloaded automatically using PyTorch Torchvision.

```python
import torchvision

# Download training dataset
train_dataset = torchvision.datasets.CIFAR10(
    root="./data",
    train=True,
    download=True
)

# Download testing dataset
test_dataset = torchvision.datasets.CIFAR10(
    root="./data",
    train=False,
    download=True
)

# Display dataset information
print("Training Images:", len(train_dataset))
print("Testing Images:", len(test_dataset))

print("Classes:", train_dataset.classes)
```

## 6. Dataset Preprocessing

The following preprocessing operations are performed:

1. Download the CIFAR-10 dataset.
2. Resize images from 32 × 32 to 224 × 224 pixels.
3. Convert images into PyTorch tensors.
4. Normalize images using ImageNet mean and standard deviation.
5. Select 10,000 training images and 2,000 testing images using stratified sampling.
6. Divide images into batches of 32.

## 7. Dataset Splitting

The original dataset contains:

| Dataset | Number of Images |
|---|---:|
| Original Training Dataset | 50,000 |
| Original Testing Dataset | 10,000 |

The experiment uses:

| Dataset | Selected Images |
|---|---:|
| Training | 10,000 |
| Testing | 2,000 |

The selected subsets maintain approximately equal representation of all 10 classes.

## 8. Dataset Usage

The CIFAR-10 dataset is used to compare four ImageNet-pretrained CNN architectures:

- AlexNet
- VGG16
- ResNet50
- EfficientNetB0

The final classification layers are modified to predict one of the 10 CIFAR-10 categories.

## 9. Pre-trained Model Weights

The four models use pre-trained ImageNet weights downloaded through PyTorch Torchvision:

- AlexNet: ImageNet-pretrained weights
- VGG16: ImageNet-pretrained weights
- ResNet50: ImageNet-pretrained weights
- EfficientNetB0: ImageNet-pretrained weights

The original feature extraction layers are frozen, and only the newly added classification layers are trained.

## 10. Dataset Reference

Official CIFAR-10 Website:

https://www.cs.toronto.edu/~kriz/cifar.html

The dataset is used for academic and educational image classification experiments. Refer to the official dataset website for its terms of use.
