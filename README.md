# Phishermen's Cove


## Project Description

`Phishermen's Cove` is our mini-project for SC1015 Introduction to Data Science & Artificial Intelligence, employing data analytics and machine learning techniques to detect potentially harmful phishing websites.


## Repository Structure

1. [`datasets`](https://github.com/aidanfora/Phishermens-Cove/tree/main/datasets): This folder contains datasets used throughout the Phishermen's Cove project. Key files include:
    - `filtered_malicious_urls.csv`: Dataset containing only URLs classified as either phishing sites or benign sites.

    - `malicious_urls.csv`: Dataset featuring various malicious URL types (phishing, ransomware, defacement, etc.).

    - `sampled_url_information.csv`: Dataset containing a random sample of 1000 entries from `url_information.csv`

    - `url_information.csv`: Our primary dataset, providing over 80 different URL attributes and phishing classifications.

2. [`src`](https://github.com/aidanfora/Phishermens-Cove/tree/main/src): This folder contains all our source code for the Phishermen's Cove project. Key files include:
    - [`practical-motivation`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/practical-motivation.md): Outlines our rationale for focusing on phishing website detection.

    - [`data-preparation.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/data-preparation.ipynb): Contains the explanation for initial feature selection, as well as code for data cleaning and feature extraction.

    - [`exploratory-analysis.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/exploratory-analysis.ipynb): Details our analysis of selected features and their relationship to phishing characteristics.

    - [`feature-engineering.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/feature-engineering.ipynb): Details our attempts to create new, more informative features from existing data.

    - [`machine-learning.ipynb`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/machine-learning.ipynb): Details the implementation of traditional machine learning models (logistic regression, decision trees) for phishing website classification.

    - [`transformer-approach`](https://github.com/aidanfora/Phishermens-Cove/blob/main/src/transformer-approach.ipynb): Details our learning beyond the classroom by attempting to apply transformer-based models for phishing website classification.


## Learning Value

The `Phishermen's Cove` project provided a valuable opportunity to delve into two cutting-edge IT fields: **Cybersecurity** and **Artificial Intelligence**.

Through this project, we discovered the deep connections between these areas. By building AI models to detect phishing websites, the project both raised our awareness of crucial security threats and demonstrated the power of AI to address real-world problems across various domains.