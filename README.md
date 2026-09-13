# FUTURE_ML_02 — Support Ticket Classification & Prioritization

## Project Overview

This project builds a machine learning system that automatically classifies IT support tickets by **ticket type** and **priority** using their text.

The goal is to help support teams automatically organize incoming tickets and identify how they should be handled.

## Objectives

- Clean and preprocess support ticket text
- Convert text into numerical features using TF-IDF
- Classify tickets into:
  - Incident
  - Request
  - Problem
  - Change
- Predict ticket priority:
  - High
  - Medium
  - Low
- Evaluate model performance using classification metrics
- Visualize model performance using confusion matrices
- Test the system on a new support ticket

## Dataset

The project uses an IT service ticket dataset containing **4,000 support tickets** and 17 columns.

Relevant fields include ticket subject, ticket body, ticket type, and priority.

The dataset itself is excluded from the GitHub repository using `.gitignore`.

## Machine Learning Approach

### 1. Text Preparation

Ticket subject and body text are combined into a single text feature.

### 2. Train-Test Split

The data is divided into:

- 80% training data
- 20% testing data

Stratified splitting is used to preserve class distributions.

### 3. TF-IDF

TF-IDF (Term Frequency-Inverse Document Frequency) is used to convert ticket text into numerical feature vectors.

### 4. Classification

Logistic Regression and Support Vector Machine models are used for classification.

The models predict:

- Ticket Type
- Ticket Priority

## Results

The final models achieved approximately:

| Task | Accuracy |
|---|---:|
| Ticket Type Classification | 62.38% |
| Ticket Priority Classification | 37.62% |

The notebook also contains detailed precision, recall, F1-score results and confusion matrices.

## Example Prediction

A new ticket describing an unavailable AWS production service was passed to the trained models.

The system predicted:

- **Ticket Type:** Incident
- **Ticket Priority:** Medium

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- TF-IDF
- Logistic Regression
- Support Vector Machine

## Project Structure

```text
FUTURE_ML_02/
├── .gitignore
├── notebooks/
│   └── support_ticket_classification.ipynb
└── data/
    └── dataset excluded from GitHub
