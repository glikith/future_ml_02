# future_ml_02 : Support Ticket Classifier

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-NLP-4B8BBE?style=for-the-badge)

> NLP pipeline for classifying and prioritizing customer support tickets with category detection and urgency scoring from raw ticket text.

---

## Overview

This project builds a dual-output text classification system on customer support ticket data. Raw ticket text is cleaned, converted to TF-IDF features, and fed into two separate classifiers — one for ticket category, one for priority level. Built as part of the **Future Interns Machine Learning Internship (Task 2)**.

---

## Features

| Feature | Description |
|---|---|
| Text Preprocessing | Lowercasing, punctuation removal, stopword removal via NLTK |
| TF-IDF Vectorization | Converts cleaned ticket text into numerical features |
| Category Classification | Classifies tickets into Billing, Technical, Refund, Cancellation, or Product inquiry |
| Priority Prediction | Assigns Critical, High, Medium, or Low urgency per ticket |
| Evaluation | Accuracy, precision, recall, and confusion matrices for both models |
| Visualizations | Category and priority distributions, model performance charts |

---

## Tech Stack

```
Language    : Python 3.10+
Environment : Jupyter Notebooks
NLP         : NLTK (stopwords), TF-IDF (scikit-learn)
ML          : scikit-learn
Data        : Pandas
Dataset     : Customer Support Ticket Dataset — Kaggle
```

---

## Getting Started

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/glikith/future_ml_02.git
cd future_ml_02

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download NLTK stopwords
python -c "import nltk; nltk.download('stopwords')"
```

### Dataset

Download the dataset from Kaggle and place it in the `data/` folder:

[https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset](https://www.kaggle.com/datasets/suraj520/customer-support-ticket-dataset)

### Run

Execute the notebooks in order:

```
1. data_cleaning.ipynb
2. model_training.ipynb
3. visualization.ipynb
```

---

## How It Works

```
Raw ticket CSV (data/)
        |
        v
data_cleaning.ipynb
— lowercase, remove punctuation and stopwords
— output: outputs/cleaned_tickets.csv
        |
        v
model_training.ipynb
— TF-IDF vectorization of ticket text
— Model A: category classifier (5 classes)
— Model B: priority classifier (4 levels)
— evaluate with accuracy, precision, recall
        |
        v
visualization.ipynb
— category and priority distribution charts
— confusion matrices for both models
— outputs/category_predictions.csv
— outputs/priority_predictions.csv
```

---

## Author

[Gummadi Likith](https://github.com/glikith)

Built as part of the **Future Interns Machine Learning Internship - Task 2**.
