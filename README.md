# Threads-Sentiment-Analysis-CNN
This repo contains a comprehensive analysis of Threads app reviews using Convolutional Neural Networks (CNN) for sentiment analysis and Latent Dirichlet Allocation (LDA) for topic modeling. 

## Context 
Since its launch, Meta's Threads app has faced challenges in retaining its user base. This project analyzes customer feedback to:
- Classify sentiments into positive, negative, and neutral categories.
- Identify key topics driving user satisfaction and dissatisfaction using LDA.
- Provide actionable recommendations for improving app features and addressing user concerns.

## Features 
1. Sentiment Analysis Using CNN:
- Classifies Threads app reviews into positive, neutral, or negative sentiments.
- Achieves 73.1% test accuracy, significantly outperforming baseline classifiers.
- Incorporates strategies to handle class imbalance (e.g., weighted loss functions).
2. Topic Modeling Using LDA:
- Extracts themes from positive and negative reviews.
- Identifies user perceptions, such as satisfaction with the interface or frustration with content moderation.
3. Data Visualization:
- Distribution of sentiment labels across review scores.
- Common keywords in positive and negative reviews for actionable insights.

## Methodology 
1. Data Collection
- Over 37,000 reviews were sourced from the Google Play Store and Apple App Store.
- Each review includes metadata such as star ratings, review dates, and app versions.
2. Preprocessing
- Tokenization, lowercasing, punctuation removal, and stop-word removal.
- Non-English reviews were excluded for consistency.
- Text transformed into matrices for input to CNN.
3. Model: 
Convolutional Neural Networks (CNN):
- Extracts features from word embeddings using 1D convolutional layers.
- Captures local and global patterns indicative of sentiment.
- Includes layers for dimensionality reduction and classification: Convolution (Conv1D) with ReLU activation; Pooling (MaxPooling1D) for feature selection; Flattening layer to prepare data for final classification; Fully connected (Dense) layer with Softmax for sentiment classification.

## Key results 
1. Model Performance:
- Accuracy: 73.1% on test data.
- Cross-validation accuracy: 72.1%, confirming model robustness.
2. Insights from Topic Modeling:
- Positive Reviews: Users appreciate the interface, social features, and Threads' potential as a Twitter alternative.
- Negative Reviews: Users mostly highlight concerns with content moderation, usability, and account management.

## Implementation 
1. Model training:
- Used Stratified K-Fold Cross-Validation for fair performance evaluation.
- Adjusted class weights to handle imbalance in sentiment categories.
3. Tools & Libraries:
- Python: Core programming language.
- TensorFlow/Keras: For CNN implementation.
- scikit-learn: For preprocessing and evaluation.
- Latent Dirichlet Allocation (LDA): For topic modeling. 
