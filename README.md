# Market Basket Analysis: Data Mining for Consumer Behavior


## Project Overview
This project applies **Association Rule Mining** to a large-scale retail dataset to uncover hidden purchasing patterns. By identifying products that are frequently bought together, we can derive actionable insights for store layout optimization, targeted marketing, and cross-selling strategies.

## Technical Implementation
* **Data Transformation**: Processed raw transaction logs into a one-hot encoded "basket" format using `pandas`.
* **Algorithm**: Implemented the **Apriori Algorithm** via the `mlxtend` library to identify frequent itemsets.
* **Metrics**: Evaluated relationships using **Support**, **Confidence**, and **Lift** to ensure statistical significance.
* **Visualization**: Developed a directed graph network using `networkx` to visualize product clusters.

## Methodology
1.  **Cleaning**: Removed transactions with missing values or negative quantities to ensure data integrity.
2.  **Thresholding**: Utilized a `min_support` of **0.01** to capture patterns occurring in at least 1% of all transactions.
3.  **Optimization**: Focused on rules with a **Lift > 1.2**, indicating a relationship stronger than random chance.

   Why the "Empty DataFrame" Error Occurred
   
The "Empty DataFrame" error in your notebook was caused by a mismatch between the Support Threshold and the nature of the dataset.

The Disconnect: You initially set min_support=0.07 (7%). In a large-scale retail dataset like Online Retail II, it is statistically rare for any specific product combination to appear in 7 out of every 100 transactions.

The Result: Because no items met this high bar, the algorithm found zero "frequent itemsets". Without itemsets, the association_rules function has nothing to calculate, resulting in the "Empty DataFrame" message.

The Fix: Lowering the threshold to 0.01 (1%) or 0.02 (2%) allows the algorithm to detect the meaningful patterns that exist in smaller, more realistic percentages of total sales.
