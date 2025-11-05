# kmeans-clustering
## project description:
This project performs customer segmentation using the K-Means clustering algorithm. The segmentation is based on customers’ age, education level, years of employment, income, debt, default status, and debt-to-income ratio to identify groups with similar financial and demographic characteristics.

## Dataset:
- **Name:** Customer segmentaion
- **Source:** https://github.com/Nikhil-Adithyan/Customer-Segmentation-with-K-Means
- **Features:** Age,	Edu,	Years, Employed,	Income,	Card Debt,	Other Debt,	Defaulted,	DebtIncomeRatio
- 
## Preprocessing:
 Outline of preprocessing steps used in the repo:

- Loading data: Read CSV and basic sanity checks (missing values, types).

-Missing value handling: Impute or remove rows/columns. Document the strategy used (mode imputation).

- Feature engineering: Compute debt_to_income_ratio if not present, create bins if needed.

- Scaling: Scale numeric features (StandardScaler) before K-Means.

## Methodology

1. Choosing K: Use Elbow method, Silhouette score, and domain knowledge to decide cluster count.


Training K-Means: Fit K-Means on the scaled features and obtain cluster labels.

Post-processing: Profile clusters by computing summary statistics per cluster (mean) and visualize.

## Results
- Found k = 3 clusters balancing silhouette score and business interpretability.
<img width="1222" height="451" alt="image" src="https://github.com/user-attachments/assets/cd0ec8af-434b-462f-891b-19498ef98274" />
- Silhouette Scores show it best performance when number of clusters= 2.

- clusters shape:

<img width="1601" height="836" alt="image" src="https://github.com/user-attachments/assets/964fbc8a-9874-4c14-91f7-8254e03f2da6" />

Cluster 0 – Financially Stable Adults: Mid-aged employees (~35), moderate income, lowest debt and default rate, maintaining the healthiest debt-to-income ratio.

Cluster 1 – Overcommitted Young Adults: Young, well-educated (~30), low income, moderate debt, highest default rate, and high debt-to-income ratio.

Cluster 2 – Wealthy Defaulters: Experienced, highly educated, high income and debt, frequent defaulters with a high debt-to-income ratio.
