# Dataset Information – RNN, LSTM and GRU Sequence Classification

## 1. Dataset Name

IMDB Movie Reviews Dataset

## 2. Dataset Source

- **Source:** TensorFlow Keras
- **Dataset Website:** https://ai.stanford.edu/~amaas/data/sentiment/
- **Download Method:** TensorFlow Keras Dataset API
- **Task:** Sentiment Analysis
- **Classification Type:** Binary Classification

## 3. Dataset Description

The IMDB Movie Reviews Dataset contains movie reviews collected from the Internet Movie Database (IMDB).

Each review is associated with a sentiment label indicating whether the review expresses a positive or negative opinion.

The dataset is widely used for natural language processing and sentiment classification tasks.

## 4. Dataset Details

| Attribute | Description |
|---|---|
| Total Reviews | 50,000 |
| Training Samples | 25,000 |
| Testing Samples | 25,000 |
| Positive Reviews | 25,000 |
| Negative Reviews | 25,000 |
| Input Type | Text Sequences |
| Output Type | Binary Labels |

## 5. Dataset Features

The dataset contains the following information:

- **Review:** A movie review represented as a sequence of numerical word IDs.
- **Label:** Sentiment category of the review.

### Class Labels

| Label | Meaning |
|---|---|
| 0 | Negative Review |
| 1 | Positive Review |

## 6. Dataset Download Code

The dataset is downloaded automatically in Google Colab using TensorFlow Keras.

```python
from tensorflow.keras.datasets import imdb

# Set vocabulary size
vocab_size = 10000

# Download training and testing data
(X_train, y_train), (X_test, y_test) = imdb.load_data(
    num_words=vocab_size
)

# Display dataset information
print("Training samples:", len(X_train))
print("Testing samples:", len(X_test))
```

## 7. Data Preprocessing

The following preprocessing operations are performed:

1. Load the IMDB dataset.
2. Restrict the vocabulary to the 10,000 most frequent words.
3. Apply padding to make all sequences equal in length.
4. Set the maximum review length to 200.
5. Use the prepared sequences as input to the RNN, LSTM, and GRU models.

## 8. Dataset Usage

The dataset is used to train and evaluate three different recurrent neural network architectures:

- Simple RNN
- LSTM
- GRU

Each model predicts whether a movie review is positive or negative.

## 9. Dataset Format

The dataset is loaded as numerical sequences and labels rather than a traditional CSV file.

The Keras dataset API automatically downloads and prepares the training and testing data.

## 10. Dataset License

The IMDB Large Movie Review Dataset is provided by Stanford AI and is intended for research and educational use. Refer to the original dataset documentation for usage and redistribution conditions.

**Dataset Reference:** https://ai.stanford.edu/~amaas/data/sentiment/
