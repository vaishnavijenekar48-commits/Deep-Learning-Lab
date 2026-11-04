# Practical: Implementation and Comparison of RNN, LSTM and GRU for Sequence Classification

## 1. Aim

To implement and compare Simple Recurrent Neural Network (RNN), Long Short-Term Memory (LSTM), and Gated Recurrent Unit (GRU) models for sequence classification and analyze their performance using appropriate evaluation metrics.

## 2. Introduction

Sequence classification is a machine learning task in which sequential data is classified into different categories.

In this practical, three different recurrent neural network architectures are implemented to perform sentiment analysis on movie reviews.

The IMDB Movie Reviews Dataset is used to classify reviews into two categories:

- Positive Review
- Negative Review

The performance of RNN, LSTM, and GRU models is compared to understand their differences in learning sequential information.

## 3. Models Implemented

### A. Simple RNN

A Recurrent Neural Network processes sequential data by maintaining information from previous time steps. It is useful for learning patterns in sequential information.

### B. LSTM

Long Short-Term Memory is an advanced type of RNN that uses memory cells and gates to retain important information over longer sequences and reduce the vanishing gradient problem.

### C. GRU

Gated Recurrent Unit is another advanced RNN architecture. It uses update and reset gates to control information flow and has a simpler structure than LSTM.

## 4. Dataset Used

- Dataset Name: IMDB Movie Reviews Dataset
- Source: TensorFlow Keras
- Task: Binary Sentiment Classification
- Training Samples: 25,000
- Testing Samples: 25,000
- Classes: Positive and Negative

## 5. Technologies and Libraries

- Python
- Google Colab
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn

## 6. Methodology

1. Download the IMDB movie reviews dataset.
2. Load training and testing data.
3. Perform sequence padding to make reviews equal in length.
4. Create an embedding layer to represent words as numerical vectors.
5. Build Simple RNN, LSTM, and GRU models.
6. Train all three models using the same training dataset.
7. Generate predictions using testing data.
8. Calculate accuracy, precision, recall, and F1-score.
9. Compare model performance using tables and graphs.
10. Identify the best-performing model based on F1-score.

## 7. Model Configuration

- Vocabulary Size: 10,000 words
- Maximum Sequence Length: 200
- Embedding Dimension: 64
- Hidden Units: 64
- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Epochs: 5
- Batch Size: 64
- Dropout: 0.5

## 8. Evaluation Metrics

The following evaluation metrics are used:

- **Accuracy:** Measures the proportion of correctly classified reviews.
- **Precision:** Measures how many predicted positive reviews are actually positive.
- **Recall:** Measures how many actual positive reviews are correctly identified.
- **F1-Score:** Represents the harmonic mean of precision and recall.

Confusion matrices are also generated to analyze classification performance.

## 9. Expected Outputs

The practical generates:

- Training and validation accuracy.
- Model comparison table.
- Accuracy comparison graph.
- Precision, Recall, and F1-score comparison graph.
- Validation accuracy graph.
- Confusion matrices for all three models.
- Best-performing model based on F1-score.

## 10. Conclusion

In this practical, Simple RNN, LSTM, and GRU models are implemented for sequence classification using the IMDB Movie Reviews Dataset.

All three models are trained and evaluated using the same dataset and evaluation metrics.

Their performance is compared using accuracy, precision, recall, and F1-score.

This practical demonstrates the differences between recurrent neural network architectures and their applications in natural language processing and sequence classification.

The best-performing model is identified based on the experimental evaluation results.
