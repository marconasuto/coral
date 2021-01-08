# Coral - Telco customer churn analysis and prediction
This project is about customer churn analysis and prediction for a fictional Telco company (IBM dataset).
Churn rate is an essential parameter for evaluating a company. To understand the financial issues caused by churning we can consider

1. The losses directly related to churning:
    - The revenue a company didn't earn for each year the customer was retained (customer lifetime value).
    - The added revenue through upselling
    - The potential for referrals generated


2. The losses indirectly related with churning:

    - New customer acquisition costs due to lost revenues from retained customers: new customers cost on average 4 times the ARPU
    - Reputation in the market

For these reasons, churn rate minimisation is a key factor for any company. With this analysis we would like to address **3 main questions**:

1. What are the profiles of churning customers, are there any categories and patterns?

2. Can we assess the churning risk associated with each customer in the dataset?

3. What are the potential profits and ROI if we would target the customers at high risk of churning?

## Project Outline

    ├── LICENSE
    ├── README.md                  <- The project layout (this file)
    ├── data
    │   ├── images                 <- For README.md, presentation
    │   ├── external
    │   ├── processed              <- preprocessed datasets for classification.ipynb, pickled files
    │   └── raw                    <- The original, immutable data dump
    │
    ├── notebooks                  <- Jupyter notebooks
    │   └── data_scrubbing.ipynb   <- Preparing data for EDA and modeling
    │   └── classification.ipynb   <- Cluster analysis, classification modeling, risk levels
    │
    ├── reports                    <- Reports and presentations
    │   └── presentation.pdf       <- Non-technical presentation
    │
    │
    └── requirements.txt           <- The requirements file for reproducing the analysis environment
