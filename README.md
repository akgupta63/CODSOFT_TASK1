# CODSOFT_TASK1

Movie Genre Classification - Internship Project
Project Overview
This project aims to build an automated machine learning classifier that predicts the genre of a movie based on its textual description. Using natural language processing (NLP) techniques, this system classifies movies into various genres such as drama, documentary, comedy, and horror.

Dataset
The dataset consists of three main files containing movie metadata:

train_data.txt: Training records with structure ID ::: TITLE ::: GENRE ::: DESCRIPTION (54,214 records).
test_data.txt: Unlabeled test records with structure ID ::: TITLE ::: DESCRIPTION (54,200 records).
test_data_solution.txt: Test set ground truth solution with structure ID ::: TITLE ::: GENRE ::: DESCRIPTION (54,200 records).
Methodology
Data Parsing: Safely extracted and parsed the custom ::: delimited records into pandas DataFrames.
Feature Extraction: Converted movie descriptions into numeric features using TF-IDF Vectorization (Term Frequency-Inverse Document Frequency):
Configured with English stop-words filtering.
Extracting both unigrams and bigrams (ngram_range=(1, 2)).
Limited to the top 25,000 features with sublinear TF scaling applied to minimize the impact of repetitive words.
Model Selection: Trained a multinomial Logistic Regression model optimized with the parallel saga solver to handle large-scale multi-class text categorization.
Results & Performance
Overall Accuracy: 60.37%
Top Performing Genres (by F1-Score):
Western: 0.84
Documentary: 0.77
Game-Show: 0.67
Drama: 0.65
Key Learnings & Takeaways
Engineered robust NLP preprocessing and feature scaling pipelines suited for highly imbalanced multi-class classification.
Achieved optimized, fast, and multi-threaded training using SAGA solver optimizations on high-dimensional text matrices.
