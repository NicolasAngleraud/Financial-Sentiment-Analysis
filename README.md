# Financial-Sentiment-Analysis


[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eYcndSmh13Z2lXXoIVVviYpdVVz1G5Y_?usp=sharing)

---

## Context
This project aims to classify finance-related texts into one of the three sentiment classes: positive, neutral, positive.

## Data
The data used in this project includes:
- Source: [Kaggle dataset](https://www.kaggle.com/datasets/sbhatti/financial-sentiment-analysis)
- Format: csv file with 2 columns Sentence/Sentiment

## Method
The approach consists of the following steps:
1. Data preprocessing
   - Cleaning: dealing with missing values, duplicates, annotation inconsistencies and removing some special characters
   - Transformation: using a sentence transformers model to get embeddings for each sentence and a label encoder for the classes
   - Validation
2. Analysis
   - EDA to have an idea of the type of sentence and of the annotation process
   - Visualiaztion of the class proportions
3. Implementation
   - XGBoost model using the text embeddings
   - Comparison between the basic version and a version weighting classes based on their frequency during training
   - (future experiments will use BERT+MLP and Llama 3.2 few-shot prompting)
4. Evaluation
   - Accuracy
   - F1 score
   - ROC/AUC
   - Confusion matrix

Limitations: class imbalance, class edges ambiguity
