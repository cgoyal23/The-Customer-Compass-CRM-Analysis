# The Customer Compass – CRM Analytics & Customer Lifetime Value Prediction

## Overview

The Customer Compass is a customer relationship management (CRM) analytics project focused on understanding customer purchasing behaviour, segmenting customers based on their transaction history, and predicting their future value.

Using transactional data from an e-commerce business, the project applies RFM (Recency, Frequency, Monetary) analysis for customer segmentation and probabilistic models such as BG/NBD and Gamma-Gamma to estimate future purchasing behaviour and Customer Lifetime Value (CLTV).

The ultimate objective is to help businesses make data-driven marketing decisions, improve customer retention, identify high-value customers, and develop effective cross-selling and upselling strategies.

## Business Problem

An e-commerce company wants to understand its customer base and develop targeted marketing strategies.

Different customer groups require different approaches:
- Identify high-value and loyal customers.
- Recognize customers who are becoming inactive.
- Identify potential loyal customers.
- Estimate future customer spending.
- Develop targeted retention and marketing campaigns.

This project addresses these requirements through customer segmentation and predictive analytics.

## Dataset

**Dataset:** Online Retail II – Year 2010–2011

The dataset contains transactional records from an online retail business selling gift and souvenir products.

Important features include:
- `Invoice`: Unique transaction identifier.
- `StockCode`: Product identifier.
- `Description`: Product description.
- `Quantity`: Number of products purchased.
- `InvoiceDate`: Date and time of transaction.
- `Price`: Unit price of the product.
- `Customer ID`: Unique customer identifier.
- `Country`: Customer's country.

## Technologies & Libraries

- **Programming:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn, Squarify
- **Predictive Modeling:** Lifetimes (BG/NBD and Gamma-Gamma)
- **Feature Scaling:** Scikit-learn

## Project Workflow

### 1. Data Preprocessing
- Loaded and explored the transactional dataset.
- Removed cancelled transactions and handled missing values.
- Identified and treated outliers in quantity and price.
- Created transaction-level revenue using quantity and unit price.

### 2. Exploratory Data Analysis (EDA)
- Analysed categorical and numerical variables.
- Examined customer purchasing patterns.
- Identified popular products and sales distributions.
- Explored country-wise transaction patterns.

### 3. RFM-Based Customer Segmentation

Applied RFM analysis to classify customers based on three dimensions:

- **Recency:** How recently a customer made a purchase.
- **Frequency:** How frequently a customer purchases.
- **Monetary:** How much money a customer spends.

Generated RFM scores using quantile-based ranking and categorized customers into behavioural segments, including:

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Hibernating
- New Customers
- Promising
- Need Attention

Visualized customer distribution across segments using bar charts and treemaps.

### 4. Predictive Customer Lifetime Value (CLTV)

Implemented probabilistic models to estimate future customer value.

**BG/NBD (Beta-Geometric / Negative Binomial Distribution)**

- Models customer purchasing frequency and dropout behaviour.
- Estimates the expected number
