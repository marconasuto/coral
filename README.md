# Coral - Telco customer churn analysis and prediction
This project is about customer churn analysis and prediction for a fictional telco company using IBM sample dataset.

Churn rate is an essential parameter for evaluating a company. To understand the financial issues caused by churning we can consider

1. The losses directly related to churning:
    - The revenue a company didn't earn for each year the customer was retained (customer lifetime value).
    - The added revenue through upselling
    - The potential for referrals generated

2. The losses indirectly related with churning:
    - New customer acquisition costs due to lost revenues from retained customers: new customers cost on average 4 times the ARPU (Average Revenue Per User) 
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

## Methodology

The methodology adopted is a quite standard one for any classification analysis. 

-  **Business understanding**: The first step is Business Understanding, essential to read and understand the data and to scope the problem. This is where we formulate the questions that will guide our analysis. 
- The next steps follow the **OSEMN (Obtain - Scrub - Explore - Model - iNterpret)**

## Business recommendations
### Churned customer profile
<a href="https://public.tableau.com/views/Coral_churn_prediction_analysis/Dashboard1?:language=en-GB&:display_count=y&:origin=viz_share_link"> <img src="data/images/Screenshot 2021-01-09 at 16.43.18.png"> </a>
During our Exploratory data analysis we highlighted 3 main clusters/segments of churning customers. We created a dashboard as a tool for both marketing and strategic planning. We can make comparisons filtering by clusters:

Cluster 1
- They tend not to be SeniorCitizen
- They spend less per month w.r.t. cluster 3, they churn soon
- They don't use services

Cluster 2
- Half of them has multiple lines
- They tend not to have partners and dependents
- They tend to have a higher median value of SeniorCitizen w.r.t. Cluster==2 or 1
- They spend quite a lot per month, they churn soon
- They have month-to-month contract
- They use fiber optic
- They don't use OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport
- They use StreamingMovies and StreamingTV more than cluster 2
- They tend to use electronic payment methods, although less than cluster 0

Cluster 3 - could be profiled as “Tech-savy families”
- They tend to have a higher median value of SeniorCitizen w.r.t. Cluster==2 or 1
- They spend a lot per month, they churn late
- They use all the services


### Churning risk assessment of current customer base
<a href="https://public.tableau.com/views/Coral_churn_prediction_analysis/Dashboard1?:language=en-GB&:display_count=y&:origin=viz_share_link"> <img src="data/images/Screenshot 2021-01-09 at 16.44.00.png"> </a>
The dashboard above shows the actual customer base by risk level, applying our predictive model. Each customer on the dashboard is identified by its reported gender. 

The dimension of the icons is proportional to each customer's average total charges left.

The quantity obtained for each customer, indicates how much money, on average, we can expect from each customer throughout his lifetime (median tenure).

Clicking on the filter to the right, will show the set of customers that are profitable to target.

### Potential profits and ROI 
<table>
  <tr>
    <th><img src="data/images/Potential profits from marketing campaign by labeling threshold - Conv. rate: 0.4.png" width="500" height="320"></th>
    <th><img src="data/images/Potential ROIs from marketing campaign by labeling threshold - Conv. rate: 0.4.png" width="500" height="320"></th>
    </tr>
 </table>

Assessing which customers are going to churn enables:
- Planning actions to retain customers
- Set KPIs for retention

Key factors for marketing campaigning are:
- Knowing what the target audience is
- Costs and CAC (Cost per ACqusition)
- Potential revenues and ARPU (Average Reveues Per User)
- Potential profits and ROI (Return On Investment)
- Conversion rate

We assessed that the minimum conversion rate for profitable campaigning is around 40%. What is key, though, is what percentage of CAC we want to consider to calculate costs. Usually for retention campaign it's lower than the CAC. If we would consider lower our CAC, we can expect lower conversion rates as KPIs.
In the images above we assumed a max marketing cap per user during a retention campaign equals to the CAC. We estimated that with a conv. rate of 40%, we can expect a max ROI of 36%.


## Future works
1. Longitudinal data, social media data
2. Improving classifier performance
3. Putting into production 

Our churn analysis can’t highlight, i.e., why customers churned, what caused churning, how churning evolved. Also, understanding our customers would mean understanding how we could improve our offers, tailored them, depending on their profiles. For these reasons, we need longitudinal and social media data to enrich our customers profiles and strategic planning.
Another focus point for future works is how to improve our classifier performance. Beyond acquiring enriched data, we would need adopting more advanced techniques, i.e. PCA, neural networks.
Finally, for both marketing and strategic reasons, putting this tool into production would benefit all interested parties.
