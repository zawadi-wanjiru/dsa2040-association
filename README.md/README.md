# DSA 2040 - Association Rule Mining

## Author
Gachunga Gift

## Dataset
**Amazon Sale Report.csv** – E-commerce dataset (from Kaggle). Contains order transactions with product categories.

## Objective
Explore association rule mining to discover relationships between product categories. This helps understand which products are often bought together and can guide cross-selling and marketing strategies.

## Steps Taken
1. **Data Preparation**
   - Removed duplicates and missing values.
   - Converted transactional data into a basket format (one-hot encoding).
2. **Frequent Itemset Mining**
   - Applied Apriori and FP-Growth algorithms.
   - Experimented with two minimum support thresholds: 0.05 and 0.1.
3. **Association Rule Generation**
   - Generated rules using support, confidence, and lift metrics.
   - Analyzed top rules for real-world insights.
4. **Visualization**
   - Plotted top 10 frequent itemsets by support.

## Libraries Used
- pandas
- mlxtend.frequent_patterns
- matplotlib
- numpy
- itertools
- collections

## How to Run
1. Clone the repository.
2. Ensure the dataset is in `/data/`.
3. Open `/notebooks/association_rules.ipynb` in Jupyter Notebook or Google Colab.
4. Run all cells to reproduce the analysis.
