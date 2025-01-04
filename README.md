# Named-Entity-Recognition-NER-and-Feature-Engineering
Fake vs Real News Classifier

Project Overview

This project implements a machine learning-based classifier that distinguishes between fake and real news articles. The model uses data collected from two popular fact-checking websites: Politifact and Gossipcop. By analyzing features such as sentiment, named entities (organizations, locations, and people), and article characteristics, the classifier predicts whether a given news article is fake or real.

Dataset

The dataset is composed of news articles obtained from:

Politifact (both fake and real articles)

Gossipcop (both fake and real articles)

These datasets are preprocessed and cleaned to extract meaningful features such as named entities, sentiment scores, article length, and tweet counts (a measure of popularity).

Features

The following features are extracted for classification:

Tweet Count: Number of tweets associated with the article, indicating its popularity.

Article Length: Number of words in the article title.

Sentiment Score: The sentiment of the article title, derived using TextBlob.

Named Entities:
Organizations
Locations
People

Approach

Text Preprocessing: Titles are converted to lowercase, special characters are removed, and extra spaces are eliminated.

Named Entity Recognition (NER): Using Spacy's en_core_web_sm model, we extract named entities like organizations, locations, and people from the article titles.

Sentiment Analysis: The sentiment score of each article title is computed using TextBlob.

Modeling: A Random Forest Classifier is used to classify articles into fake or real categories based on the features.

Visualization

Box plots: Show the distribution of named entities and tweet count based on the label (fake/real).

Correlation Heatmap: Visualizes the correlation between the extracted features.

Model Evaluation

The classifier is evaluated using:

Accuracy Score: Measures the overall performance of the model.

F1 Score: Provides a balance between precision and recall, especially useful for imbalanced datasets.
