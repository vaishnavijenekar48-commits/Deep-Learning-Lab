# Dataset Information – Tomato Leaf Disease Classification

## 1. Dataset Name

PlantVillage Tomato Leaf Disease Dataset

## 2. Dataset Source

- **Source:** PlantVillage Dataset
- **GitHub Repository:** https://github.com/spMohanty/PlantVillage-Dataset
- **Dataset Directory:** raw/color
- **Download Method:** GitHub ZIP download using Python
- **Image Format:** JPG, JPEG, PNG
- **Image Type:** RGB (Color Images)

## 3. Dataset Description

The PlantVillage dataset contains images of healthy and diseased plant leaves.

For this practical, only tomato leaf images are selected from the complete dataset.

The dataset is used to train a Convolutional Neural Network (CNN) to identify different tomato leaf diseases based on image features.

## 4. Tomato Disease Categories

The dataset contains the following 10 categories:

| No. | Disease Category |
|---|---|
| 1 | Tomato Bacterial Spot |
| 2 | Tomato Early Blight |
| 3 | Tomato Late Blight |
| 4 | Tomato Leaf Mold |
| 5 | Tomato Septoria Leaf Spot |
| 6 | Tomato Spider Mites |
| 7 | Tomato Target Spot |
| 8 | Tomato Yellow Leaf Curl Virus |
| 9 | Tomato Mosaic Virus |
| 10 | Tomato Healthy |

## 5. Dataset Download Code

The dataset is automatically downloaded from GitHub using the following Python code:

```python
import tensorflow as tf
import zipfile

# GitHub dataset URL
dataset_url = (
    "https://github.com/spMohanty/PlantVillage-Dataset/"
    "archive/refs/heads/master.zip"
)

# Download dataset
zip_path = tf.keras.utils.get_file(
    fname="PlantVillage.zip",
    origin=dataset_url,
    extract=False
)

# Extract dataset
with zipfile.ZipFile(zip_path, 'r') as zip_ref:
    zip_ref.extractall("/content/")

print("Dataset downloaded successfully!")
```

## 6. Dataset Preprocessing

The following preprocessing operations are performed:

1. Select only tomato leaf disease images.
2. Read images from their respective class folders.
3. Resize images to 128 × 128 pixels.
4. Normalize pixel values between 0 and 1.
5. Divide images into training, validation, and testing sets.
6. Apply image augmentation to training images.

## 7. Dataset Splitting

The dataset is divided into three subsets:

| Dataset | Percentage |
|---|---:|
| Training | 80% |
| Validation | 10% |
| Testing | 10% |

The split is stratified to maintain the class distribution across subsets.

## 8. Dataset Usage

The dataset is used to train and evaluate a CNN model.

The model learns visual patterns from tomato leaf images and predicts whether a leaf belongs to a healthy or diseased category.

## 9. Dataset Format

The dataset is organized into separate folders based on disease categories.

Each folder contains images belonging to its respective disease class.

The original dataset is downloaded and extracted automatically in Google Colab.

## 10. Dataset Reference and Usage

**Repository:** https://github.com/spMohanty/PlantVillage-Dataset

The dataset is used for educational and academic purposes. Refer to the original repository and dataset terms for licensing and redistribution conditions.
