# Phishermen's Cove


## Project Description

`Phishermen's Cove` is our mini-project for SC1015 Introduction to Data Science & Artificial Intelligence, employing data analytics and machine learning techniques to detect potentially harmful phishing websites.


## Repository Structure

1. [`datasets`](https://github.com/aidanfora/Phishermens-Cove/tree/main/datasets): This folder contains datasets used throughout the Phishermen's Cove project. Key files include:
    - `filtered_malicious_urls.csv`: Dataset containing only URLs classified as either phishing sites or benign sites.
    - `malicious_urls.csv`: Dataset featuring various malicious URL types (phishing, ransomware, defacement, etc.).
    - `sampled_url_information.csv`: Dataset containing a random sample of 1000 entries from `url_information.csv`
    - `url_information.csv`: Our primary dataset, providing over 80 different URL attributes and phishing classifications.

<br>

2. [`src`](https://github.com/aidanfora/Phishermens-Cove/tree/main/src): This folder contains all our source code for the Phishermen's Cove project. Key files include:
    - [`practical-motivation.md`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/practical-motivation.md): Outlines our rationale for focusing on phishing website detection.
    - [`data-preparation.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/data-preparation.ipynb): Contains the explanation for initial feature selection, as well as code for data cleaning and feature extraction.
    - [`exploratory-analysis.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/exploratory-analysis.ipynb): Details our analysis of selected features and their relationship to phishing characteristics.
    - [`feature-engineering.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/feature-engineering.ipynb): Details our attempts to create new, more informative features from existing data.
    - [`machine-learning.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/machine-learning.ipynb): Details the implementation of traditional machine learning models for phishing website classification.
    - [`transformer-approach.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/transformer-approach.ipynb): Details our learning beyond the classroom by attempting to apply transformer-based models for phishing website classification.


## Project Development Journey

### Dataset Preparation

Based on our selected and engineered variables detailed in `exploratory-analysis.ipynb` and `feature-engineering.ipynb`, we split them based on their types into the following 5 categories of training datasets to benchmark our machine learning model performance.

**Training Sets:**
1. Numerical
2. Categorical
3. Feature Engineered
4. Numerical + Categorical
5. Numerical + Categorical + Feature Engineered

### Machine Learning and Model Selection

We then train multiple logistic regression and decision tree models based on the 5 prepared training datasets each and evaluate each model based on their test accuracy and goodness of their fit.

#### Logistic Regression:


| Training Sets      | Num | Cat | Engi | Num + Cat | Num + Cat + Engi | 
|--------------------|:-------:|:----------:|:--------:|:-----------:|:------------:|
| Test <br> Accuracy | 0.8431 |  0.86302   | 0.7263  |   0.8485   |   0.8621    |

#### Decision Trees:


| Training Sets      | Num | Cat | Engi | Num + Cat | Num + Cat + Engi | 
|--------------------|:-------:|:----------:|:--------:|:-----------:|:------------:|
| Test <br> Accuracy | 0.9175 |  0.6303   | 0.9314  |   0.9193   |   0.9578    |


###### **Refer to `machine-learning.ipynb` for more detailed explanations.*

Comparing Logistic Regression and Decision Trees, we notice that Decision Trees in general performed better than logistic regression models for classifying phishing URLs usiing our selected variables from the dataset.

Best model obtained:
- [X] Decision Tree Classifier (Trained on Numerical + Categorical + Feature Engineered variables), achieving an impressive accuracy of 95.78% on our test set.


### NLP Techniques with BERT

Going beyond coursework, we implemented BERT (Bidirectional Encoder Representations from Transformers) with a binary classifcation head and finetuned it our use case of identifying phishing URLs directly using natural language processing capabilities. (Implemented using `huggingface`).

We used balanced smapling to obtain a balanced dataset of full length phishing and benign URLs from `malicious_urls.csv` and finetuned the BERT model across 3 epochs with a batchsize of 32 and learning rate of 0.00005.

| Metrics      | Finetuned BERT | 
|--------------------|:-------:|
| Test Accuracy | 0.9406 |
| F1 Score | 0.9415 |

Overall, our finetuned BERT model shows promising results in predicting phishing URLs given raw unprocessed full length URLs with a high accuracy of around 94% and a good fit with little bias indicated by the high F1 score of 0.9415.

## Learning Value

The `Phishermen's Cove` project provided a valuable opportunity to delve into two cutting-edge IT fields: **Cybersecurity** and **Artificial Intelligence**.

Through this project, we discovered the deep connections between these areas. By building AI models to detect phishing websites, the project both raised our awareness of crucial security threats and demonstrated the power of AI to address real-world problems across various domains.
