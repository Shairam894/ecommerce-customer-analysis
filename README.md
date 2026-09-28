# E-Commerce Customer Behavior Analysis

## Project Overview

This project analyzes e-commerce customer session data to understand customer behavior, conversion patterns, funnel drop-offs, and factors associated with purchase decisions.

The project also uses a Decision Tree classification model to predict whether a customer session results in a purchase.

## Objectives

- Clean and validate the e-commerce dataset
- Perform exploratory data analysis
- Analyze the customer purchase funnel
- Compare mobile and desktop conversion rates
- Investigate the relationship between session time and purchase behavior
- Identify important factors associated with purchase prediction
- Build and evaluate a Decision Tree classification model
- Provide data-backed business recommendations

## Dataset

The dataset contains 10,000 e-commerce customer sessions.

### Main Features

| Feature | Description |
|---|---|
| Session_ID | Unique session identifier |
| Customer_Type | New or Returning customer |
| Device | Mobile or Desktop |
| Traffic_Source | Source through which the customer arrived |
| Pages_Viewed | Number of pages viewed |
| Products_Viewed | Number of products viewed |
| Cart_Added | Whether an item was added to cart |
| Checkout_Started | Whether checkout was started |
| Purchase | Whether a purchase was completed |
| Session_Time | Session duration in minutes |
| Discount_Shown | Whether a discount was shown |

## Data Analysis

The analysis includes:

1. Data cleaning and validation
2. Exploratory Data Analysis
3. Customer funnel analysis
4. Device conversion comparison
5. Traffic source analysis
6. Session-time analysis
7. Decision Tree machine learning
8. Model evaluation
9. Feature importance analysis

## Key Findings

- The dataset contains 10,000 sessions and 1,224 purchases, resulting in an overall purchase rate of 12.24%.
- Returning customers have a higher purchase conversion rate (20.39%) than new customers (8.21%).
- Desktop sessions have a higher purchase conversion rate (16.12%) than mobile sessions (8.90%).
- 4,342 sessions added products to the cart and 2,903 sessions started checkout.
- 1,224 sessions resulted in a purchase.
- The largest percentage drop-off occurs between checkout and purchase.
- Purchase conversion varies across traffic sources, with Email showing a 15.70% purchase rate.
- Session time, pages viewed, products viewed, and customer/session characteristics provide useful signals for understanding purchase behavior.

## Machine Learning

A Decision Tree Classifier was used to predict the `Purchase` variable.

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Feature Importance

Post-purchase journey variables such as `Cart_Added` and `Checkout_Started` were excluded from the prediction model to reduce data leakage and make the model more suitable for predicting purchase behavior using earlier session information.

## Business Recommendations

- Improve the checkout experience to reduce checkout-to-purchase abandonment.
- Optimize the mobile shopping experience because mobile conversion is lower than desktop conversion.
- Develop retention strategies for returning customers.
- Evaluate marketing channels using both traffic volume and conversion performance.
- Use browsing behavior to identify highly engaged customers.
- Investigate checkout friction such as payment issues, unexpected costs, or complicated checkout steps.

## Project Structure

```text
ecommerce-customer-analysis/
│
├── README.md
│
├── data/
│   └── ecommerce_cleaned_10000.csv
│
├── notebooks/
│   └── ecommerce_customer_analysis.ipynb
│
├── visualizations/
│   ├── customer_funnel.png
│   ├── mobile_vs_desktop.png
│   ├── session_time_purchase.png
│   └── traffic_source.png
│
└── model/
    └── decision_tree.png