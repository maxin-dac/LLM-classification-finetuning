# LLM Classification Finetuning
<img width="560" height="280" alt="kaggle_66631_logos_header" src="https://github.com/user-attachments/assets/090e2a37-b981-4df2-b8bd-070d22a49226" />

## Context & Objective
This notebook performs an in-depth Exploratory Data Analysis (EDA) on the **LLM Chatbot Arena** dataset from [Kaggle](https://www.kaggle.com/competitions/llm-classification-finetuning/overview).
The goal is to understand the structure of the data, and identify patterns that influence human preference between two model responses. 

## Notebook Structure & Workflow
1. **Data Loading & Inspection:** Loading training and test data, exploring basic statistics and missing values.
2. **Text Parsing & Feature Extraction:** Parsing JSON-like prompt and response fields, computing text lengths and basic quality signals.
3. **Target Variable Analysis:** Distribution of winners (`model_a`, `model_b`, `tie`) and class balance.
4. **Prompt & Response Length Analysis:** Length distributions, length difference between responses, and its correlation with the winner.
5. **Baseline Model:** A simple TF-IDF + Logistic Regression baseline with log loss evaluation.
6. **Submission Generation:** Predicting probabilities and saving the submission file.

## Key Insights
- The dataset is **reasonably balanced** between `model_a`, `model_b`, and `tie`, but ties are often the hardest class to predict.
- **Response length difference** is a strong signal: longer responses tend to win more often, but this is not a universal rule.
- Prompt length varies widely, meaning models must handle both short and long contexts effectively.
- Semantic quality and relevance (not just length) are likely the real drivers of preference.

## Key takeaway:
A strong model should combine semantic understanding of prompt-response pairs with relative comparison features.

## Tech Stack & Libraries

* **Language:** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

* **Data Manipulation:** ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)

* **Text Processing:** ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white) ![JSON](https://img.shields.io/badge/JSON-000000?style=flat&logo=json&logoColor=white)

* **Visualization:** ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat) ![Seaborn](https://img.shields.io/badge/Seaborn-5B8DB8?style=flat)

* **Modeling:** ![Logistic Regression](https://img.shields.io/badge/Logistic_Regression-2E8B57?style=flat) 

* **Environment:** ![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-F37626?style=flat&logo=jupyter&logoColor=white) ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)

---

*To explore the detailed code, feel free to download the notebook file on this repo, or check out my [Kaggle](https://www.kaggle.com/code/maximendacleu/llm-classification-finetuning).*
