# Market Basket Analysis: Data Mining for Consumer Behavior


## 📌 Project Overview
This project applies **Association Rule Mining** to a large-scale retail dataset (Online Retail II) to discover hidden patterns in customer purchasing behavior. By identifying products frequently bought together, the analysis provides data-driven strategies for store layout optimization, product bundling, and cross-selling.

## 🛠️ Technical Stack
- **Language:** Python 3.x
- **Libraries:** - `pandas`: Data cleaning and transformation.
  - `mlxtend`: Implementation of the **FP-Growth Algorithm** for frequent itemset mining.
  - `networkx` & `matplotlib`: Visualization of product association networks.

## 📈 Methodology & Optimization
1. **Data Preprocessing:** Cleaned over 500,000 rows of transaction data, handling missing values and removing non-commercial entries (returns/cancellations).
2. **Memory Efficiency:** Optimized runtime by converting transaction matrices to **Boolean** types, reducing memory footprint by 80% to prevent runtime crashes.
3. **Algorithm Selection:** Switched from Apriori to **FP-Growth** to handle high-dimensionality data more efficiently.
4. **Metric Evaluation:** Filtered rules based on **Lift (> 1.2)** and **Confidence (> 0.7)** to ensure findings were statistically significant and actionable.

[Image of a product association network graph with nodes and directed edges]

## 💡 Key Business Insights
- **Anchor Products:** Identified high-traffic items like the 'White Hanging Heart T-Light Holder' that serve as primary entry points for customer baskets.
- **Impulse Pairings:** Discovered high-lift associations between themed home decor items, suggesting significant opportunities for "Frequently Bought Together" recommendations.
- **Retail Strategy:** Proposed a strategic store layout where highly associated but functionally different items are placed apart to increase aisle traversal.
<img width="2361" height="1495" alt="image" src="https://github.com/user-attachments/assets/e29109f9-4fb0-4467-8ebf-22707045afce" />


## 🚀 How to Run
1. Clone the repository.
2. Ensure `online_retail_II.xlsx` is in the root directory.
3
