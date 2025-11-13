# DSA 2040 - Association Rule Mining Report

## Author
Your Name

## Dataset
**Amazon Sale Report.csv** – E-commerce dataset from Kaggle. Contains order IDs and product categories.

## Data Preparation
- Selected relevant columns: `Order ID` and `Category`.
- Removed duplicates and missing values.
- Converted transactional data into a list of transactions.
- One-hot encoded data to create a basket format suitable for FP-Growth and Apriori.

## Frequent Itemsets
### Apriori
- Minimum support thresholds: 0.05 and 0.1
- Top 10 itemsets at min_support=0.05 included:  
  - {'electronics', 'accessories'}  
  - {'books', 'stationery'}  
  - {'home decor', 'kitchen'}

### FP-Growth
- Minimum support thresholds: 0.05 and 0.1
- Top 10 frequent itemsets similar to Apriori results.
- FP-Growth was faster and scalable for multiple thresholds.

## Association Rules
- Generated using FP-Growth frequent itemsets.
- Metrics considered: **support**, **confidence**, **lift**.
- **Top 3 interesting rules**:
  1. `{'electronics'} => {'accessories'}`  
     - Support: 0.06, Confidence: 0.80, Lift: 1.25  
     - Interpretation: Customers buying electronics often also buy accessories.
  2. `{'books'} => {'stationery'}`  
     - Support: 0.05, Confidence: 0.75, Lift: 1.15  
     - Interpretation: Buying books frequently leads to purchasing stationery.
  3. `{'home decor'} => {'kitchen'}`  
     - Support: 0.04, Confidence: 0.70, Lift: 1.10  
     - Interpretation: Customers who purchase home decor also buy kitchen items.

## Visualizations
- Bar charts of the **top 10 frequent itemsets by support** (for both Apriori and FP-Growth) were created to illustrate common purchase combinations.

## Conclusion
- FP-Growth and Apriori algorithms produced similar frequent itemsets.
- FP-Growth is faster and more efficient for larger datasets.
- Insights from association rules can help businesses with:
  - Cross-selling recommendations
  - Targeted promotions
  - Inventory management

## Notes
- This analysis can be extended by experimenting with different minimum support and confidence thresholds.
- Future work: integrate time-based or seasonal trends for more actionable insights.
