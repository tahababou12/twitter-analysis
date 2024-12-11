# Predicting Customer Support Engagement on Twitter

## Overview

This repository contains the code, data processing scripts, and analytical models used for the research paper **"Predicting Customer Support Engagement on Twitter Using Hierarchical Modeling and Sentiment Analysis"**.
The project explores the volume and dynamics of customer support interactions on Twitter, utilizing hierarchical models and sentiment analysis to identify patterns and predictors of effective engagement.
This project is conducted in affiliation with **Boston University**, as part of the **MA678 Applied Statistical Modeling** course.

------------------------------------------------------------------------

## Dataset

The project leverages the **Customer Support on Twitter Dataset** sourced from [Kaggle](https://www.kaggle.com/dsv/8841), which contains approximately **2.8 million tweets**.
Key variables include:

-   **tweet_id**: Unique identifier for each tweet.
-   **author_id**: Identifier for the account (customer or brand).
-   **inbound**: Indicates whether the tweet is customer-initiated (True) or brand-initiated (False).
-   **text**: Content of the tweet.
-   **response_tweet_id**: ID of the response tweet.
-   **sentiment_score**: Derived sentiment analysis of the tweet (positive, neutral, negative).
-   **temporal features**: Time-based attributes such as hour, weekday, and month.
-   **follow-up volume**: Number of tweets in a response thread.

------------------------------------------------------------------------

## Objectives

1.  **Predict**: Identify key predictors influencing the volume and timing of follow-ups.
2.  **Analyze**: Examine patterns in sentiment, temporal activity, and follow-up behaviors.
3.  **Model**: Compare Poisson and Negative Binomial regression models for overdispersed count data.
4.  **Validate**: Perform diagnostic checks for multicollinearity, dispersion, and model fit.

------------------------------------------------------------------------

## Key Components

### **1. Data Processing**

Scripts for: - Cleaning and preprocessing the dataset.
- Feature engineering (e.g., sentiment scores, temporal features).

### **2. Exploratory Data Analysis (EDA)**

Notebooks for: - Visualizing tweet volumes, sentiment distributions, and temporal patterns.
- Performing correlation analysis and chi-square tests.

### **3. Modeling**

Code for: - Building a **null model** as a baseline.
- Developing hierarchical models (Poisson and Negative Binomial) with group-level predictors.
- Checking assumptions like overdispersion, linearity, and independence.

### **4. Validation**

-   Calculating metrics such as AIC, MAE, RMSE, and Pseudo-R².
-   Cross-validation for predictive accuracy.
-   Model diagnostics, including Variance Inflation Factors (VIF) and residual plots.

------------------------------------------------------------------------

## Results

-   **Hierarchical Negative Binomial Model** outperformed the Poisson model by addressing overdispersion (dispersion parameter: **1.45**) and accounting for brand-specific variability.
-   **Key Predictors**:
    -   **Sentiment**: Positive tweets elicited more follow-ups.
    -   **Temporal Factors**: Tweets during peak hours and weekdays showed higher engagement.
    -   **Text Length**: Longer tweets correlated with more follow-ups.

------------------------------------------------------------------------

## Technologies Used

-   **R**: For statistical modeling and validation.
    -   Key libraries: `lme4`, `blmeco`, `arm`, `ggplot2`.
-   **Python**: For initial preprocessing and visualization.
-   **Jupyter Notebooks**: To document the analysis.

------------------------------------------------------------------------

## How to Use

1.  Clone the repository:

    ``` bash
    git clone https://github.com/tahababou12/twitter-analysis.git
    cd twitter-analysis
    ```

2.  Install dependencies for R and Python.

3.  Run the scripts/notebooks in sequence:

    -   **Preprocessing**: Data cleaning and feature engineering.
    -   **EDA**: Visualize and explore the data.
    -   **Modeling**: Develop and validate models.

------------------------------------------------------------------------

## Research Paper

Read the full research paper [here](./docs/Final_Paper_Twitter_Analysis.pdf).

### Citation

If you use this repository or reference the paper, please cite:

```         
@misc{ababou2024twitter,
  title={Predicting Customer Support Engagement on Twitter Using Hierarchical Modeling and Sentiment Analysis},
  author={Taha H. Ababou},
  year={2024},
  url={https://github.com/tahababou12/twitter-analysis},
  note={Boston University}
}
```

------------------------------------------------------------------------

## Acknowledgments

-   **Data Source**: [Kaggle - Customer Support on Twitter Dataset](https://www.kaggle.com/dsv/8841).
-   **Research Context**: This project builds on studies in sentiment analysis and hierarchical modeling.

------------------------------------------------------------------------
