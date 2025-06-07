# IMDB Movie Reviews Sentiment Analysis

## Overview

Sentiment Analysis is a natural language processing(NLP) task of analyzing large volumes of text to determine whether it expresses a positive sentiment, a negative sentiment or a neutral sentiment. The aim of this project is to implement a sentiment analysis sytem that can effectively classify movie reviews based on the expressed sentiment

To achieve this, we explored and compared the performance of:

- Logistic regression model
- LSTM (Long short-term Memory)

## Dataset

We used the [IMDB Movie Reviews Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

The dataset contains 50,000 labeled movie reviews and has a balanced sentiment distribution of 50% positive and 50% negative reviews.

## Data Exploration

- **Class Distribution**: Perfectly balanced dataset
- **Text length**: Reviews vary in length with an average of 230 words per review
- Common stopwords like 'the', 'and', 'a' dominate and were removed in preprocessing
- No missing values were found however, there was duplicate values which were handled in preprocessing

## Data Preprocessing

1. Duplicates removal
2. Text Cleaning:
   - Lowercasing
   - Removed HTML tags, punctuation and special characters
   - Stopwords removal using NLTK's English stopwords
3. Tokenization using `nltk.word_tokenize()`
4. Embeddings:
   - TF-IDF for Logistic Regression
   - Word2Vec for LSTM

## Experimentation and Results

## Contributions


