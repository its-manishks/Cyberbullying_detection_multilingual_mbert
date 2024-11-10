# Multilingual Cyberbullying Detection

A machine learning project to detect cyberbullying across multiple languages using mBERT (Multilingual BERT) and sentiment analysis. This project focuses on providing a context-aware and language-agnostic solution for detecting harmful online behavior in Hindi, Marathi, and Malayalam.

# Table of Contents

- [Introduction](#introduction)
- [Screenshots](#screenshots)
- [Features](#features)
- [Project Architecture](#project-architecture)
- [Datasets](#datasets)
- [Running](#running)
- [Preprocessing](#preprocessing)
- [Model](#model)
- [Evaluation Metrics](#evaluation-metrics)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [Authors](#authors)

## Introduction

With the rise of social media, cyberbullying has become a critical issue affecting individuals across diverse backgrounds and age groups. This project aims to create a robust solution capable of identifying cyberbullying in various languages, providing insights into harmful interactions and promoting safer online spaces.

## Screenshots

![Screenshot](Screenshots/screenshot-1.jpg)
-------------------------------------------
![Screenshot](Screenshots/screenshot-2.jpg)
-------------------------------------------
![Screenshot](Screenshots/screenshot-3.jpg)
-------------------------------------------
![Screenshot](Screenshots/screenshot-4.jpg)
-------------------------------------------
![Screenshot](Screenshots/screenshot-5.jpg)

## Features

- **Multilingual Support:** Supports cyberbullying detection in Hindi, Marathi, and Malayalam.
- **Sentiment Analysis Integration:** Analyzes the emotional tone of input text to improve accuracy.
- **Real-Time Classification:** Classifies text as cyberbullying or non-cyberbullying instantly.
- **Scalable Architecture:** Ready for deployment on platforms like Heroku or AWS.

## Project Architecture

The model architecture consists of several stages:

1. **Input Layer:** Receives text data in Hindi, Marathi, or Malayalam.
2. **Preprocessing:** Cleans and normalizes the text by removing special characters, stop words, and performing lemmatization.Cleans and normalizes the text by removing special characters, stop words, and performing lemmatization.
3. **Feature Extraction:**
   - **TF-IDF:** Extracts term frequency-inverse document frequency values.
   - **mBERT Embeddings:** Generates multilingual embeddings to capture language context.
4. **Logistic Regression Classifier:** Combines TF-IDF and mBERT features for binary classification.
5. **Output Layer:** Outputs binary labels for cyberbullying or non-cyberbullying.

## Datasets

- **Source:** Data collected from social media platforms for sentiment analysis, with samples labeled as cyberbullying or non-cyberbullying.
- **Languages:** Hindi, Marathi, and Malayalam.
- **Size:** Over 30,000 labeled text samples to ensure diverse representation and robust model training.

## Preprocessing

The preprocessing pipeline includes:

- **Text Cleaning:** Removing special characters, URLs, hashtags, and mentions.
- **Lowercasing:** Converting text to lowercase.
- **Stop Words Removal:** Eliminating common, irrelevant words.
- **Lemmatization:** Reducing words to their base forms.

## Model

The project uses:

- **mBERT (Multilingual BERT):** A transformer model that provides robust, multilingual embeddings.
- **Logistic Regression:** A classifier trained on combined TF-IDF and mBERT embeddings to distinguish cyberbullying from non-cyberbullying effectively.

## Evaluation Metrics

The model is evaluated on:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**

These metrics ensure balanced performance across classes and highlight the model’s ability to minimize false positives and negatives.

## Installation

1. **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/Multilingual-Cyberbullying-Detection.git
    cd Multilingual-Cyberbullying-Detection
    ```

2. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Download mBERT Model** (if not included in the repository)
    ```bash
    from transformers import AutoTokenizer, AutoModel
    tokenizer = AutoTokenizer.from_pretrained("bert-base-multilingual-cased")
    model = AutoModel.from_pretrained("bert-base-multilingual-cased")
    ```

## Usage

1. **Run the Preprocessing Script**
   ```bash
    python preprocess.py
    ```

2. **Train the Model**
    ```bash
    python train.py
    ```

3. **Test the Model** Input text samples to see classification results for cyberbullying detection.

## Future Work

- **Deep Learning Integration:** Experiment with LSTM, CNN, or hybrid models for enhanced accuracy.
- **Real-Time Monitoring:** Develop capabilities for live monitoring of social media content.
- **Expanded Language Support:** Extend the model to detect cyberbullying in additional languages.

## Authors
- [**Manish Kumar**](https://github.com/its-manishks)
