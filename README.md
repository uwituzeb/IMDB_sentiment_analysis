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

## Experiment Table 1: LSTM (Deep Learning Model) - Hyperparameter Tuning

| Model # | Vocabulary Size | Sequence Length | Embedding Dim | LSTM Units | Dropout Rate | Batch Size | Learning Rate | Accuracy | Precision | Recall | F1-Score |
|---------|------------------|------------------|----------------|-------------|----------------|-------------|----------------|----------|-----------|--------|----------|
| 1       | 5,000            | 200              | 64             | 64, 32      | 0.2            | 64          | 0.0001         | 0.89     | 0.89      | 0.89   | 0.89     |
| 2       | 10,000           | 200              | 64             | 64, 32      | 0.2            | 64          | 0.0001         | 0.54     | 0.57      | 0.54   | 0.48     |
| 3       | 5,000            | 200              | 64             | 32, 16      | 0.4            | 64          | 0.0001         | 0.88     | 0.88      | 0.88   | 0.88     |
| 4       | 10,000           | 150              | 100            | 32, 16      | 0.4            | 64          | 0.0001         | 0.87     | 0.87      | 0.87   | 0.87     |
| 5       | 7,500            | 150              | 100            | 32, 16      | 0.4            | 64          | 0.0001         | 0.85     | 0.85      | 0.85   | 0.85     |

---

## Experiment Table 2: Logistic Regression Model (Traditional ML Model)

| Model # | Embedding | Accuracy | Precision | Recall | F1-Score |
|---------|-----------|----------|-----------|--------|----------|
| 1       | TF-IDF    | 0.89     | 0.89      | 0.89   | 0.89     |
| 2 (After Tuning)      | TF-IDF    | 0.89     | 0.89      | 0.89   | 0.89     |

## Setup and Installation

1. Clone repository

```
git clone https://github.com/uwituzeb/IMDB_sentiment_analysis.git
cd IMDB_sentiment_analysis
```

2. Create Virtual environment

```
python -m venv venv
source venv/bin/activate
```

3. Install dependencies

```
pip install -r requirements.txt
```

4. Run notebook and start training

## Contributions

| Team Member         | Responsibilities                                                                 |
|---------------------|-----------------------------------------------------------------------------------|
| **Bernice Uwituze** | Data preprocessing, dataset research and analysis, visualizations, README writing |
| **Jean Chrisostome**| Data preprocessing, visualizations, logistic regression modeling                  |
| **Sifa Mwachoni**   | LSTM architecture design, model training and validation, report writing           |
| **Christian Mutabazi** | Hyperparameter tuning, experiment tracking, model optimization               |
