# Practical 8: BERT-Based Sentiment Analysis

## 1. Aim

To implement a pre-trained BERT (Bidirectional Encoder Representations from Transformers) model for sentiment analysis and classify text reviews into positive and negative categories.

## 2. Introduction

BERT is a pre-trained Transformer-based language model developed by Google. It is widely used in Natural Language Processing (NLP) tasks such as sentiment analysis, text classification, question answering, and language understanding.

Unlike traditional language models that process text in one direction, BERT uses bidirectional attention to understand the context of words from both left and right directions.

In this practical, a pre-trained BERT model is fine-tuned using the IMDB Movie Reviews Dataset to perform sentiment classification.

The model identifies whether a movie review expresses a positive or negative opinion.

## 3. Dataset Used

- **Dataset Name:** IMDB Movie Reviews Dataset
- **Source:** Hugging Face Datasets
- **Dataset Type:** Text Data
- **Task:** Binary Sentiment Classification
- **Training Samples Used:** 5,000
- **Testing Samples Used:** 2,000
- **Classes:** Positive and Negative

## 4. Pre-trained Model

**Model Name:** BERT Base Uncased

**Model Source:** https://huggingface.co/google-bert/bert-base-uncased

BERT Base Uncased is a pre-trained Transformer model containing 12 encoder layers, 12 attention heads, and 768 hidden dimensions.

The pre-trained model is fine-tuned for movie review sentiment classification by adding a classification layer with two output classes.

## 5. Technologies and Libraries Used

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Seaborn

## 6. Methodology

The following steps are performed:

1. Download the IMDB Movie Reviews Dataset.
2. Select training and testing samples.
3. Load the pre-trained BERT tokenizer.
4. Convert text reviews into numerical token IDs.
5. Apply padding and truncation to maintain a fixed sequence length.
6. Generate attention masks for identifying valid tokens.
7. Load the pre-trained BERT model with a two-class classification head.
8. Fine-tune BERT using the training dataset.
9. Generate sentiment predictions on testing data.
10. Evaluate the model using accuracy, precision, recall, and F1-score.
11. Generate a classification report and confusion matrix.
12. Test the model using a custom movie review.
13. Save the trained model and tokenizer.

## 7. Model Configuration

| Parameter | Value |
|---|---|
| Pre-trained Model | BERT Base Uncased |
| Maximum Sequence Length | 128 |
| Batch Size | 16 |
| Optimizer | AdamW |
| Learning Rate | 0.00002 |
| Epochs | 2 |
| Output Classes | 2 |
| Loss Function | Cross Entropy |
| Training Method | Fine-Tuning |

## 8. Evaluation Metrics

The model performance is evaluated using:

- **Accuracy:** Measures the percentage of correctly classified reviews.
- **Precision:** Measures how many predicted positive reviews are actually positive.
- **Recall:** Measures how many actual positive reviews are correctly identified.
- **F1-Score:** Represents the balance between precision and recall.
- **Confusion Matrix:** Displays correct and incorrect sentiment predictions.

## 9. Expected Outputs

The practical generates:

- Dataset information and sample reviews.
- BERT model loading and training.
- Training loss graph.
- Training accuracy graph.
- Model evaluation metrics.
- Classification report.
- Confusion matrix.
- Custom movie review sentiment prediction.
- Saved fine-tuned BERT model and tokenizer.

## 10. Conclusion

In this practical, a pre-trained BERT model was implemented for sentiment analysis using the IMDB Movie Reviews Dataset.

The pre-trained BERT model was fine-tuned to classify movie reviews into positive and negative categories.

Its performance was evaluated using accuracy, precision, recall, and F1-score.

This practical demonstrates how Transformer-based models can understand the contextual meaning of text and perform NLP tasks such as sentiment analysis and text classification.
