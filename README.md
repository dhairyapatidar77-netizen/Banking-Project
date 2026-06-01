# 🏦 Bank Term Deposit Subscription Prediction

## Overview
This project analyzes direct marketing campaign data from a Portuguese banking 
institution to predict whether a client will subscribe to a term deposit. 
The dataset contains 45,211 records collected via phone calls between May 2008 
and November 2010.

## Problem Statement
Banks invest heavily in telephonic marketing campaigns. Identifying customers 
likely to subscribe in advance allows targeted outreach, reducing costs and 
improving campaign efficiency.

## Dataset
- **Source:** Portuguese Banking Institution
- **Size:** 45,211 rows × 18 columns
- **Target Variable:** `y` — whether the client subscribed (yes/no)

## Project Structure
- Exploratory Data Analysis (EDA) on all 17 features
- Class imbalance handling using `class_weight='balanced'`
- Logistic Regression model for binary classification
- Model evaluation using Confusion Matrix, Recall, and F1-Score

## Key Findings (EDA)
- Most clients are aged between 25–40
- Majority of clients are married with secondary education
- Cellular is the most used communication channel
- May had the highest number of client contacts
- ~88% of clients did not subscribe (class imbalance)

## Model Performance
| Metric | Score |
|--------|-------|
| Accuracy | 80.4% |
| Recall (Subscribers) | 82.7% |
| Precision (Subscribers) | ~0.35 |
| F1-Score (Subscribers) | ~0.48 |

> Recall was prioritized over accuracy since missing a potential 
> subscriber is more costly than a false alarm in a marketing context.

## Why Logistic Regression over KNN?
- Faster on large datasets (45k rows)
- Built-in `class_weight='balanced'` to handle class imbalance
- More interpretable — useful for business decisions
- Higher recall for the minority class (82.7% vs 46.6% with KNN)

## Tech Stack
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
