# Dataset Information – BERT Sentiment Analysis

## 1. Dataset Name

IMDB Movie Reviews Dataset

## 2. Dataset Source

- **Source:** Hugging Face Datasets
- **Official Dataset:** https://huggingface.co/datasets/stanfordnlp/imdb
- **Original Dataset Website:** https://ai.stanford.edu/~amaas/data/sentiment/
- **Download Method:** Hugging Face Datasets Library
- **Data Format:** Text Reviews
- **Classification Type:** Binary Classification

## 3. Dataset Description

The IMDB Movie Reviews Dataset contains movie reviews collected from the Internet Movie Database.

Each review is associated with a sentiment label that indicates whether the review expresses a positive or negative opinion.

The dataset is widely used for Natural Language Processing (NLP), sentiment analysis, and text classification tasks.

## 4. Dataset Details

| Attribute | Description |
|---|---|
| Total Reviews | 50,000 |
| Original Training Samples | 25,000 |
| Original Testing Samples | 25,000 |
| Positive Reviews | 25,000 |
| Negative Reviews | 25,000 |
| Input Type | Text |
| Output Type | Sentiment Label |

**Note:** This practical uses a subset of 5,000 training reviews and 2,000 testing reviews to reduce computational time.

## 5. Dataset Features

The dataset contains two main features:

### A. Text

Contains the actual movie review written by the user.

### B. Label

Represents the sentiment of the review.

| Label | Meaning |
|---|---|
| 0 | Negative Review |
| 1 | Positive Review |

## 6. Dataset Download Code

The dataset is downloaded automatically using the Hugging Face Datasets library.

```python
from datasets import load_dataset

# Download IMDB dataset
dataset = load_dataset("imdb")

# Select training samples
train_data = dataset["train"].shuffle(
    seed=42
).select(range(5000))

# Select testing samples
test_data = dataset["test"].shuffle(
    seed=42
).select(range(2000))

# Display dataset information
print("Training Samples:", len(train_data))
print("Testing Samples:", len(test_data))

# Display sample review
print(train_data[0]["text"])

# Display sentiment label
print(train_data[0]["label"])
```

## 7. Dataset Preprocessing

The following preprocessing operations are performed:

1. Load the IMDB dataset.
2. Select training and testing samples.
3. Load the BERT tokenizer.
4. Convert text reviews into numerical token IDs.
5. Apply padding to maintain a fixed sequence length.
6. Apply truncation to limit reviews to 128 tokens.
7. Generate attention masks.
8. Convert sentiment labels into PyTorch tensors.

## 8. Dataset Splitting

The original dataset contains:

| Dataset | Number of Reviews |
|---|---:|
| Original Training Dataset | 25,000 |
| Original Testing Dataset | 25,000 |

The experiment uses:

| Dataset | Selected Reviews |
|---|---:|
| Training | 5,000 |
| Testing | 2,000 |

The selected samples are shuffled using a fixed random seed for reproducibility.

## 9. Dataset Usage

The dataset is used to fine-tune the pre-trained BERT model for sentiment analysis.

The model takes movie review text as input and predicts whether the sentiment is positive or negative.

## 10. Dataset Reference

**Hugging Face Dataset:**

https://huggingface.co/datasets/stanfordnlp/imdb

**Original Research Dataset:**

https://ai.stanford.edu/~amaas/data/sentiment/

The dataset is used for educational and academic purposes. Refer to the original dataset documentation and license for usage and redistribution conditions.
