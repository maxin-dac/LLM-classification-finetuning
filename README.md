# LLM Classification Finetuning
<img width="560" height="280" alt="kaggle_66631_logos_header" src="https://github.com/user-attachments/assets/090e2a37-b981-4df2-b8bd-070d22a49226" />

## Context & Objective
This notebook performs an in-depth Exploratory Data Analysis (EDA) on the **LLM Chatbot Arena** dataset from Kaggle: [https://www.kaggle.com/competitions/llm-classification-finetuning/overview].
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
- **Language**: Python 3.13
- **Data Manipulation**: `pandas`
- **Text Processing**: `scikit-learn` (TF-IDF), safe `JSON` parsing
- **Visualization**: `Matplotlib`, `Seaborn`
- **Modeling**: Logistic Regression baseline
- **Environment**: Kaggle Notebook

---

*To explore the detailed code, feel free to download the notebook file on this repo, or check out my Kaggle: [https://www.kaggle.com/code/maximendacleu/llm-classification-finetuning].*

***By: Maxime NDACLEU | BI & Data Analyst***
