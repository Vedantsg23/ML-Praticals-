# ML Practicals and Mini Project

This repository contains the email spam classification practical followed by the Uber fare prediction mini project. The mini project is listed last as requested.

## 1. Email Spam Classification

Notebook: 01_Practical_Email_Spam_Classification.ipynb

Classifies the Kaggle email dataset as not spam (0) or spam (1) with K-Nearest Neighbors and a linear Support Vector Machine. Reports accuracy, balanced accuracy, spam precision, spam recall, F1-score, and confusion matrices.

Results on the stratified 20% test split (random state 42):

| Model | Accuracy | Spam precision | Spam recall | Spam F1 |
| --- | ---: | ---: | ---: | ---: |
| KNN (k=5) | 0.9140 | 0.8187 | 0.9033 | 0.8590 |
| Linear SVM | 0.9729 | 0.9224 | 0.9900 | 0.9550 |

## 2. Mini Project: Uber Fare Prediction

Notebook: 02_Mini_Project_Uber_Fare_Prediction.ipynb

Preprocesses the Uber Fares data, identifies fare outliers, checks correlations, trains Linear Regression and Random Forest Regression, and compares R², RMSE, and MAE.

Results on the random 20% test split (random state 42):

| Model | R² | RMSE (USD) | MAE (USD) |
| --- | ---: | ---: | ---: |
| Linear Regression | 0.6904 | 5.5376 | 2.3984 |
| Random Forest | 0.8336 | 4.0603 | 1.8388 |

## Setup

Install dependencies with:

    python -m pip install -r requirements.txt

Open either notebook from the repository root in Jupyter and run the cells in order.

## Datasets

The source CSV files are not committed. Download them from Kaggle and place them in the Data directory:

- Email Spam Classification: https://www.kaggle.com/datasets/balaka18/email-spam-classification-dataset-csv — extract emails.csv to Data/emails.csv.
- Uber Fares: https://www.kaggle.com/datasets/yasserh/uber-fares-dataset — extract uber.csv to Data/uber.csv.

The email dataset is a pre-tokenized word-frequency table with an Email No. identifier and a Prediction label. The notebooks exclude identifiers from model features. Raw CSV files in Data are ignored by Git.

See Data/README.md for the exact file placement.
