# Customer Data Cleaning and Preprocessing Pipeline

This repository contains a complete data preprocessing pipeline built with Python, `pandas`, and `scikit-learn`. The project demonstrates core data science foundational skills: handling missing values, deduplication, categorical variable encoding, and feature scaling.

## Project Structure

- `data_preprocessing.ipynb`: Jupyter Notebook containing the end-to-end Python script split into clear tasks.
- `README.md`: Project documentation and submission details.

## Tasks Covered

### Task 1 — Data Cleaning
- Imputed missing numerical values (`age`) using the **median** to prevent outlier distortion.
- Imputed missing categorical values (`city`) using the **mode** (most frequent value).
- Identified and removed duplicate records based on `customer_id`.

### Task 2 — Categorical Encoding
- Applied **One-Hot Encoding** to the `city` column to prevent the model from assuming an artificial ordinal ranking between geographical locations.
- Applied **Label Encoding** to the binary `gender` column.

### Task 3 — Feature Scaling
- Implemented **Min-Max Scaling** to bound numerical features strictly between `0` and `1`.
- Implemented **Standardisation** to center the data around a mean of `0` with a standard deviation of `1`.

---

## Technical Insights: MinMaxScaler vs. StandardScaler

- **MinMaxScaler** is preferred when the underlying data does not follow a normal distribution, or when using algorithms like K-Nearest Neighbors (KNN) and Neural Networks that require strict feature boundaries (typically `0` to `1`).
- **StandardScaler** is preferred when the data exhibits a normal (Gaussian) distribution or contains significant outliers, as it preserves the outlier variance instead of squishing them into a compressed scale. Algorithms like Linear Regression, Logistic Regression, and SVMs inherently assume standardized features.

## How to Run the Notebook

1. Clone this repository:
   ```bash
   git clone <your-repository-link>
