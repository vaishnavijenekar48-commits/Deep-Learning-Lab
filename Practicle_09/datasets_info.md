# Dataset Information – Practical 9

## Dataset Name
CIFAR-10 (Canadian Institute for Advanced Research – 10 Classes)

## Dataset Source
Official website: https://www.cs.toronto.edu/~kriz/cifar.html

PyTorch dataset documentation: https://docs.pytorch.org/vision/stable/generated/torchvision.datasets.CIFAR10.html

## Dataset Description
CIFAR-10 is a widely used image classification dataset containing 60,000 colour images.

Each image belongs to one of 10 different object categories.

## Dataset Details

| Property | Description |
|---|---|
| Dataset | CIFAR-10 |
| Total images | 60,000 |
| Training images available | 50,000 |
| Testing images available | 10,000 |
| Image format | RGB |
| Original image size | 32 × 32 |
| Number of classes | 10 |
| Image type | Colour images |

## Classes
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

## Dataset Download
The dataset is downloaded automatically using Torchvision:

```python
torchvision.datasets.CIFAR10(
    root="./data",
    train=True,
    download=True
)
```

## Dataset Selection
For this practical, a smaller subset is selected to reduce computational requirements.

- Training samples: 5,000
- Testing samples: 1,000

## Preprocessing
The following preprocessing operations are performed:

1. Images are resized from 32 × 32 to 224 × 224 pixels.
2. Images are converted into PyTorch tensors.
3. Image values are normalized using ImageNet mean and standard deviation.
4. Training and testing datasets are loaded using DataLoader.
5. Images are processed in batches of 32.

## Dataset Usage
The same CIFAR-10 training and testing subsets are used for both models:

- Pre-trained ResNet18 CNN.
- Pre-trained Vision Transformer (ViT).

This allows their performance to be compared under the same dataset conditions.

## Dataset License
CIFAR-10 is provided for research and educational use. Refer to the official dataset website for its terms and conditions.
