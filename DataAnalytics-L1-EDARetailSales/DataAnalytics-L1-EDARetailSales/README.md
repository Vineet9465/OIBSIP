# EDA on Retail Sales Data
**Oasis Infobyte — Data Analytics Internship (Level 1, Task 1)**
**Author:** Vineet Pandey

## Objective
Perform an Exploratory Data Analysis (EDA) on a retail sales dataset to uncover sales trends,
customer patterns, and actionable business insights.

## Dataset
Superstore Sales dataset — 9,800 orders (2015–2018) across the US.
Columns include `Order_Date`, `Ship_Date`, `Ship_Mode`, `Segment`, `Region`, `Category`,
`Sub_Category`, `Product_Name`, and `Sales`.

> Note: this version of the dataset does not include customer age/gender or Quantity/Profit
> columns. Customer **Segment** (Consumer / Corporate / Home Office) is used as the available
> demographic proxy, and this is documented inside the notebook.

## Tech Stack
- Python
- pandas
- matplotlib
- seaborn
- Jupyter Notebook

## What's in this notebook
1. Data loading & inspection (shape, dtypes, nulls, duplicates)
2. Data cleaning/preparation (date parsing, derived time & shipping-delay features)
3. Descriptive statistics on Sales
4. Monthly & quarterly sales trend analysis
5. Customer segment & regional sales analysis
6. Top 10 best-selling products, revenue by category/sub-category
7. Correlation heatmap of numeric variables
8. Additional insight: shipping delay by ship mode
9. Conclusion — 4 actionable business recommendations

## Files
- `EDA_Retail_Sales.ipynb` — full analysis notebook (executed, with charts and written observations)
- `superstore.csv` — dataset used
- `README.md` — this file

## Key Insights
- Sales are heavily right-skewed — most orders are small, but a few large orders pull the average up.
- Clear seasonality: sales peak every Q4 (Nov–Dec), with an overall upward trend from 2015 to 2018.
- Consumer segment and the West/East regions drive the most revenue.
- A small set of "hero" products account for a disproportionate share of sales.
- Shipping speed is operationally consistent with each Ship Mode but has no correlation with order size.

## How to Run
1. Clone this repo / folder.
2. Install dependencies: `pip install pandas matplotlib seaborn jupyter`
3. Open `EDA_Retail_Sales.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
4. Run all cells top to bottom.
