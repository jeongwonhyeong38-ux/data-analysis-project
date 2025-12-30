# Product Recommendation for Revenue Growth
Customer-Level Purchase Analysis and Category-Based Recommendation using Olist E-commerce Data

## Executive Summary

This project analyzes customer-level purchase behavior in the Olist e-commerce dataset
to evaluate whether personalized product recommendations can drive revenue growth
more effectively than uniform recommendations.

The analysis shows that revenue contribution is highly concentrated among a small
group of high-value customers (VIPs), and that customers repeatedly purchase
specific product categories.

Revenue fluctuations across months are driven primarily by changes in order count,
not average purchase value, indicating that purchase frequency is the key growth lever.

Based on these findings, a category-based, customer-specific recommendation baseline
was implemented to demonstrate how personalization can support revenue growth.

## Business Goal

The goal of this project is to analyze customer-level purchase patterns and derive
data-driven product recommendation strategies aimed at increasing revenue.

Rather than directly optimizing a recommendation algorithm, the project focuses on
understanding *who* to target, *what* to recommend, and *when* recommendations should
be emphasized to maximize business impact.

## Dataset

This project uses the Olist Brazilian e-commerce dataset, which is structured as a
relational database reflecting real-world e-commerce operations.

Meaningful analytical features are created by joining multiple normalized tables,
including:

- order_items (base transaction-level table)
- orders (order status and timestamps)
- customers (customer identity consolidation)
- products (product category metadata)

All features are derived strictly from observed customer behavior, ensuring analytical
validity and reproducibility.

## Problem Background

Many e-commerce platforms rely on uniform recommendation strategies,
such as suggesting the same popular products to all customers.
This approach ignores differences in customer value, preferences,
and purchasing timing, potentially limiting revenue growth.

This project is motivated by the assumption that personalized recommendations
based on historical purchase behavior are more effective than uniform strategies.

## Main Hypothesis

Product recommendations based on customers’ historical purchase behavior
are more effective at increasing revenue than recommending the same products
to all customers.

### Hypothesis 1
Customer contribution to revenue is highly uneven.

### Hypothesis 2
Customers repeatedly purchase products from specific categories.

### Hypothesis 3
Customer purchasing behavior and revenue contribution vary across time periods.

## Customer Profile Construction

To enable revenue-driven and personalized recommendation strategies,
a comprehensive customer-level profile was constructed by aggregating
transaction-level purchase histories.

Key features include:

- Total spending per customer (total_spent)
- Customer segment (VIP / Non-VIP)
- Purchase frequency and count
- Average, maximum, and standard deviation of purchase price
- Average repurchase interval
- Seasonal purchase ratio
- Most frequently purchased product category

## Key Findings

### Hypothesis 1: Revenue Concentration
- A small group of customers accounts for a disproportionately large share of revenue.
- VIP customers drive most sales, justifying customer-level segmentation.

### Hypothesis 2: Category Preference
- Customers concentrate purchases within a limited number of categories.
- Historical category preference is a strong signal for personalization.

### Hypothesis 3: Time Variation
- Monthly revenue differences are driven primarily by order count, not spending per order.
- Purchase frequency is the key lever for revenue growth in non-peak months.

## Business Insights

- Focus personalized recommendations and promotions on high-value (VIP) customers.
- Use customer-specific category preferences for recommendation targeting.
- Increase order frequency during non-peak months through targeted campaigns.
- Apply time-aware recommendation strategies rather than static approaches.

## Recommendation Model

A simple yet interpretable category-based recommendation baseline was implemented.

For each customer:
- Preferred product categories are identified from historical purchase frequency.
- Top products within those categories are recommended.

To reflect revenue contribution differences:
- VIP customers receive revenue-based recommendations.
- Non-VIP customers receive popularity-based recommendations.

This approach prioritizes interpretability, scalability,
and alignment with business objectives.

## Business Value

This project demonstrates a real-world data science workflow including:
- Relational data integration
- Feature engineering
- Customer-level behavioral analysis
- Revenue-oriented recommendation logic

The analysis produces actionable KPIs and recommendation strategies
that directly support marketing decision-making and revenue growth.

## Limitations

- No online A/B testing was conducted to measure causal revenue lift.
- Analysis relies solely on historical purchase data.
- Temporal patterns are analyzed at a coarse monthly level.
- Results are based on a single dataset and context.

## Future Work

- Collaborative filtering using implicit feedback
- Learning-to-rank models for personalized product ordering
- Time-aware recommendation models

