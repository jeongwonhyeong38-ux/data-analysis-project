# Analysis Notebook

This directory contains the core analysis notebook supporting the project
**“Product Recommendation for Revenue Growth”**.

The notebook focuses on customer-level purchase behavior analysis using
the Olist Brazilian E-commerce dataset and demonstrates how data-driven
insights can inform revenue-oriented product recommendation strategies.

---

## Notebook Overview

### analysis.ipynb

This notebook performs an end-to-end analytical workflow, starting from
raw transactional data integration to the construction of an interpretable
baseline recommendation model.

The analysis is structured around three business-driven hypotheses:

1. Customer contribution to revenue is highly uneven  
2. Customers repeatedly purchase products from specific categories  
3. Customer purchasing behavior and revenue contribution vary across time periods  

Rather than training a complex machine learning model, the notebook
emphasizes **who to target**, **what to recommend**, and **when to recommend**
to maximize business impact.

---

## Analytical Flow

### 1. Data Integration and Preprocessing
- Multiple normalized tables from the Olist dataset are joined to construct
  a customer-level purchase history.
- Only delivered orders are retained to ensure revenue validity.
- A numeric customer identifier (`customer_key`) is generated for efficient
  aggregation while preserving traceability.

### 2. Customer-Level Feature Engineering
Customer profiles are constructed by aggregating transaction-level data,
including:
- Total spending and revenue contribution
- Purchase count and purchase frequency
- Average, maximum, and variability of purchase price
- Average repurchase interval
- Seasonal purchase ratio
- Most frequently purchased product category

These features provide a multi-dimensional view of customer behavior beyond
simple order-level metrics.

### 3. Hypothesis Validation and Exploratory Analysis
- Revenue concentration analysis confirms that a small group of customers
  (VIPs) accounts for a disproportionate share of total revenue.
- Category preference analysis shows that customers tend to concentrate
  purchases within a limited number of product categories.
- Temporal analysis reveals that monthly revenue fluctuations are driven
  primarily by changes in order count rather than average purchase value.

### 4. Business-Oriented Insights
- Customer segmentation is necessary to avoid treating all customers equally.
- Category-based personalization is supported by repeated purchasing behavior.
- Increasing order frequency during non-peak months is a key lever for
  revenue growth.

---

## Baseline Recommendation Logic

A simple yet interpretable category-based recommendation baseline is implemented:

- Each customer’s preferred product category is identified from historical
  purchase frequency.
- Products are recommended within the customer’s top category.
- VIP customers receive revenue-based recommendations (top revenue products).
- Non-VIP customers receive popularity-based recommendations (top purchased products).

This approach prioritizes interpretability, scalability, and direct alignment
with business objectives, making it suitable as a baseline for real-world
deployment.

---

## Execution Environment

- The notebook was developed and executed in the Kaggle environment.
- Data loading paths follow Kaggle’s `/kaggle/input/` structure.
- Raw data files are not included in this repository due to size and licensing
  constraints.

Refer to `data/raw/README.md` for dataset access and reproduction instructions.

---

## Purpose of This Notebook

This notebook demonstrates:
- Customer-level behavioral analysis using relational data
- Business-driven hypothesis testing
- Feature engineering for recommendation systems
- Translation of analytical findings into actionable recommendation strategies

The focus is on **decision-making support and revenue impact**, rather than
model complexity.
