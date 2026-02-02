# MSCS 634 Lab 1: Data Analysis and Visualization

## Overview
This lab explores the Diamonds dataset using Python data science libraries 
(Pandas, Matplotlib, Seaborn) to perform data cleaning, visualization, 
and statistical analysis.

## Dataset
- **Source:** Seaborn built-in datasets
- **Size:** 53,940 diamonds (reduced to ~16,000 after preprocessing)
- **Features:** Carat, Cut, Color, Clarity, Depth, Table, Price, Dimensions

## Key Insights

### Visualizations
1. **Price vs Carat Scatter Plot:** Strong positive exponential relationship 
   observed - larger diamonds command disproportionately higher prices.
2. **Price by Cut Box Plot:** Premium and Ideal cuts show higher median prices, 
   but significant overlap suggests cut is not the sole price determinant.

### Statistical Findings
- **Price Range:** $326 - $18,823
- **Strong Correlation:** Carat and Price (0.92)
- **Data Quality:** Removed 8 rows with invalid zero dimensions
- **Outliers:** Removed ~2,000 price outliers using IQR method

## Techniques Applied
- **Missing Values:** Dropped rows with invalid dimensions (x,y,z = 0)
- **Outlier Removal:** IQR method (1.5 * IQR rule)
- **Data Reduction:** Column elimination + 30% random sampling
- **Scaling:** Min-Max normalization (0-1 range)
- **Discretization:** Price categorized into Budget/Mid/Premium/Luxury tiers

## Challenges Faced
- Determining appropriate thresholds for outlier removal
- Balancing data reduction with maintaining statistical significance
- Choosing between Min-Max and Standard scaling (selected Min-Max for price 
  interpretability)

## How to Run
1. Install requirements: `pip install pandas numpy matplotlib seaborn scipy sklearn`
2. Open `MSCS_634_Lab1.ipynb` in Google Colab
3. Run cells sequentially from top to bottom

## Author
 Sai Venkata Bharath Reddy Singareddy - MSCS 634
