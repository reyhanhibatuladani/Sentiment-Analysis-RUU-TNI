# Sentiment-Analysis-RUU-TNI

## Comparative Sentiment Analysis of the RUU TNI Revision (Naïve Bayes vs. SVM)
This project analyzes public sentiment toward the controversial revision of Indonesia’s Military Law (RUU TNI), focusing on the surge of online reactions on X (Twitter).

## Overview
The main objective is to compare the performance of Naïve Bayes and Support Vector Machine (SVM) in classifying public opinion into five sentiment categories:
Positive, Slightly Positive, Neutral, Slightly Negative, and Negative.

Results show that SVM delivers higher accuracy and a better F1-Score compared to Naïve Bayes.

## Dataset
Collected during the peak of public discussion: **16–31 March 2025**.
* **Total documents:** 9.924.
    * **Twitter/X:** 9.827 tweets (`#TolakRUUTNI` and related keywords).
    * **News Portals:** 97 articles (used as comparison material).

## Methodology
This project follows the **CRISP-DM** workflow with the following steps:

1.  **Preprocessing:** Text cleaning, normalization, stemming, stopword removal
2.  **Labeling:** Using the **InSet Lexicon**.
3.  **Expert Validation:** Manual validation of **400 sampel tweet**.
4.  **Feature Extraction:** Term Frequency-Inverse Document Frequency (**TF-IDF**).
5.  **Handling Imbalance:** **SMOTE** (Synthetic Minority Over-sampling Technique) untuk menangani ketidakseimbangan kelas data.
6.  **Evaluation:** **Stratified K-Fold Cross Validation**.

## Key Findings
* **SVM** performs better on this dataset than Naïve Bayes
* Public sentiment is dominated by **Negative** reactions.
* Most discussions revolve around:
    * Potential return of **Dwifungsi ABRI**.
    * Expansion of **civilian positions** for active personnel.
    * **Extended retirement age** for TNI members.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Imbalanced-learn, Sastrawi, Matplotlib/Seaborn.
* **Tools:** Google Colab, Google Looker Studio (Dashboard).
