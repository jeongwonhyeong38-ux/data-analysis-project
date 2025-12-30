# Product Recommendation for Revenue Growth
Customer-Level Purchase Analysis using Olist E-commerce Data

## Executive Summary
This project analyzes customer purchase behavior to evaluate whether
personalized, customer-level recommendation strategies can support revenue growth
more effectively than uniform recommendations.

The analysis shows that revenue contribution is highly concentrated among a small
group of high-value customers (VIPs), and that purchase frequency—rather than
average order value—is the primary driver of revenue variation across time.

Based on these findings, a simple category-based recommendation baseline is proposed
to demonstrate how personalization can align with business objectives.

## Business Problem
Many e-commerce platforms rely on uniform recommendation strategies,
ignoring differences in customer value, preferences, and purchasing behavior.
This project investigates whether leveraging historical customer behavior
can provide more effective, revenue-oriented recommendation strategies.

## Dataset
- Source: Olist Brazilian E-commerce Dataset (Kaggle)
- Tables used:
  - order_items
  - orders
  - customers
  - products

> Raw data is not included in this repository due to size and licensing constraints.

## Analysis Overview
1. Relational data integration and feature engineering
2. Customer-level purchase aggregation
3. Revenue concentration analysis (VIP vs Non-VIP)
4. Category preference and repurchase behavior analysis
5. Temporal revenue decomposition (order count vs order value)

Detailed analysis and visualizations are available in the notebook.

## Key Insights
- Revenue is highly concentrated among a small group of customers.
- Customers repeatedly purchase from a limited set of categories.
- Monthly revenue fluctuations are driven primarily by order frequency.

## Recommendation Logic (Baseline)
- Customer-specific category preference is used as the primary signal.
- VIP customers receive revenue-oriented recommendations.
- Non-VIP customers receive popularity-based recommendations.

This baseline prioritizes interpretability and business alignment
rather than algorithmic complexity.

## Limitations & Future Work
- No causal measurement via online A/B testing
- No collaborative filtering or learning-based models
- Future extensions include CF, ranking models, and time-aware recommendations
