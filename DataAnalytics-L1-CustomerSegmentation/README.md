# Customer Segmentation Analysis (RFM + K-Means)
**Oasis Infobyte — Data Analytics Internship (Level 1, Task 2)**
**Author:** Vineet Pandey

## Objective
Segment customers into distinct groups based on purchasing behaviour, so each group can be targeted with a suitable marketing strategy.

## Dataset
Superstore Sales dataset: 9,800 order lines from 793 customers (2015-2018).

## Approach
1. Loaded and inspected the data (nulls, duplicates, date parsing).
2. Calculated customer-level statistics: average order value, purchase frequency and lifetime value (total spend).
3. Built **RFM features**: Recency (days since last order), Frequency (number of orders), Monetary (total spend).
4. Standardised the features with `StandardScaler`.
5. Used the **Elbow Method** and silhouette score to choose the number of clusters, then applied **K-Means (K = 4)**.
6. Visualised the clusters with scatter plots and profiled each cluster.
7. Wrote marketing recommendations for each segment.

## Tech Stack
Python, pandas, numpy, scikit-learn (KMeans, StandardScaler), matplotlib, seaborn, Jupyter Notebook

## Results

| Segment | Customers | % of customers | % of revenue |
|---|---|---|---|
| Big Spenders (VIP) | 68 | 8.6% | 27.8% |
| Loyal Active | 279 | 35.2% | 39.8% |
| Regular / Potential | 347 | 43.8% | 26.3% |
| At Risk / Lapsed | 99 | 12.5% | 6.1% |

## Key Insights
- About 9% of customers (Big Spenders) generate nearly 28% of revenue, so the business depends heavily on a few customers.
- The Loyal Active group is the largest source of revenue (about 40%) and orders the most often.
- About 12.5% of customers have been inactive for a long time and need a win-back campaign.
- Recommended actions for every segment are in the final section of the notebook.

## Note
This dataset has no profit column, so customer lifetime value is approximated as total historical spend.

## Files
- `Customer_Segmentation.ipynb`: full analysis (executed, with charts and written observations)
- `superstore.csv`: dataset used
- `README.md`: this file

## How to Run
1. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn jupyter`
2. Open `Customer_Segmentation.ipynb` in Jupyter, VS Code or Google Colab, with `superstore.csv` in the same folder.
3. Run all cells top to bottom.
