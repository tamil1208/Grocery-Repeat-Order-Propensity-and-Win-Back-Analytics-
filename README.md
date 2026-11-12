# Supermarket Customer Churn Analysis

## Introduction

This project analyzes customer data from a supermarket chain to understand factors influencing customer churn. By examining customer demographics, purchase behavior, and loyalty indicators across different branches and product categories, we aim to provide insights that can help improve customer retention strategies.

Churn refers to the rate at which customers stop doing business with a company over a given period. In this supermarket analysis, churn is identified when a customer ceases to make purchases. Understanding churn is crucial as it directly impacts revenue and growth. By analyzing factors contributing to churn, such as demographics, purchasing behavior, and customer satisfaction, the supermarket can develop targeted strategies to improve retention and reduce customer attrition.

## Data Description

The dataset contains 10,000 rows of raw customer data showing detailed information on customer transactions and characteristics, including:

- Customer demographics (age, gender, credit score)
- Membership status and activity
- Transaction details (products purchased, amounts, ratings)
- Branch information
- Churn status

Key fields include:

- `id`: Unique identifier for each transaction
- `branch`: Location of the supermarket (Houston, Dallas, San Antonio)
- `customer_type`: Type of customer (Normal/Member)
- `product_category`: Category of products purchased
- `total_amount`: Total amount of the transaction including tax
- `customer_churn`: Whether the customer has churned (1) or not (0)

## Tools Used

- Power BI: For data visualization and dashboard creation
- DAX (Data Analysis Expressions): For creating calculated measures and columns

## Visualization

The project includes a comprehensive Power BI dashboard with two main pages:

1. Overview Page: Provides a high-level summary of key metrics and trends.
2. Customer Churn Analysis Page: Offers detailed insights into churn factors and customer segments.

The dashboard is interactive, allowing users to filter data by various dimensions such as branch, product category, and customer type.

[Link to Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzg3YjRmMTMtNTk1NC00ZmMwLWE3MGMtZjBmZGVlZjVmNGE3IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9&pageName=7b5c417c287e1802cdb9)


## Key Findings

### Overview Page - [View Page Screenshot](https://github.com/mosesziregbe/Supermarket-Customer-Churn-Analysis/blob/main/supermarket_churn_overview.jpg)

#### Churn Rate and Customer Retention
- **Overall Churn Rate**: 20.37%, with 2,037 customers churned out of a total of 10,000.
- **Member Retention**: 79.3% of members are retained (3,964 members), while 20.7% have churned (1,046 members).
- **Regular Customers (Non-Members)**: 80.1% retention rate, with 3,999 retained and 991 churned.

#### Financial Performance
- **Total Revenue**: $3.2 million across all branches.
- **Total Transactions**: 10,000 transactions recorded.
- **Total Quantity Sold**: 55,100 units sold.
- **Average Customer Rating**: 7.0 out of 10, indicating moderate customer satisfaction.

#### Revenue Breakdown by Branch
- **Dallas**: Highest revenue at $1.11 million.
- **Houston and San Antonio**: Both branches generated $1.06 million in revenue.

#### Revenue Breakdown by Product Category
- **Top Category**: Food and beverages generate the most revenue at $0.56 million.
- **Second Category**: Sports and travel closely follows with $0.55 million.
- **Other Categories**: Revenue from electronic accessories, fashion accessories, home and lifestyle, and health and beauty categories is relatively evenly distributed.

#### Churn Analysis by Credit Score
- **Churn by Credit Score**: Customers with poor credit scores exhibit the highest churn rates, while those with excellent credit scores show the lowest churn rates.

#### Branch Performance Insights
- Notably, while Dallas has the highest total revenue, it also experiences a higher churn rate in certain categories.

### Customer Churn Analysis Page - [View Page Screenshot](https://github.com/mosesziregbe/Supermarket-Customer-Churn-Analysis/blob/main/supermarket_churn_customer_analysis.jpg)

#### Customer Demographics:
-**Total Customers:** 10K
-**Average Customer Age:** 39 years
-**Average Credit Score:** 651
-**Customers with Credit Card:** 71%

#### Gender Distribution of Churned Customers:
Female customers show higher churn (55.9%) compared to males (44.1%)

#### Credit Card Impact on Customer Churn:
More churned customers have a credit card (1,424) compared to those without (613)

#### Age Segments Contributing Most to Revenue:
- Mid Career (35-44) and Early Career (25-34) segments contribute the most
- Senior (65 & Above) segment contributes the least

#### Age Segments with Highest Customer Churn Rates:
- Late Career (55-64) has the highest churn rate at 49.83%
- Experienced Professional (45-54) follows at 48.15%
- Churn rate drops significantly for the Senior segment (65 and above)

#### Product Categories Generating Most Revenue from Churned Customers:
- Sports and Travel and Electronic Accessories categories lead
- Food and Beverages category generates the least revenue from churned customers

#### Customer Activity Status and Churn Across Membership Types:
- The distribution of customers across activity and churn status is similar for both Normal and Member types

## Insights and Recommendations

**1. Female customers show a higher churn rate (55.9%) compared to males (44.1%).** Develop targeted marketing campaigns and loyalty programs tailored to female customers' preferences. Consider conducting surveys to understand their specific needs and pain points.

**2. Customers with credit cards are more likely to churn, contrary to expectations.** Redesign credit card benefits to offer more valuable perks for frequent shoppers. Implement tiered rewards systems that increase benefits with usage, encouraging loyalty.

**3. Mid-career (35-44) and early-career (25-34) segments contribute most to revenue but have high churn rates.** Create age-specific retention programs. For mid-career customers, offer family-oriented deals. For early-career, focus on convenience and budget-friendly options.

**4. Late-career (55-64) customers have the highest churn rate at 49.83%.** Develop a senior loyalty program with benefits like priority service, special shopping hours, and health-focused products/services to appeal to this demographic.

**5. Sports and Travel and Electronic Accessories categories generate the most revenue from churned customers.** Improve customer experience in these categories through personalized recommendations, extended warranties, or exclusive access to new products. Implement a post-purchase follow-up program to ensure satisfaction.

**6. Customer activity level appears more significant in preventing churn than membership status.** Implement a multi-channel engagement strategy (e.g., app, email, in-store events) to keep customers active. Create a points system that rewards frequent visits and purchases across all categories.

**7. Membership status has less impact on churn than expected.** Revamp the membership program to offer clear, tangible benefits that differentiate from non-member experiences. Consider partnerships with local businesses to expand member benefits beyond the supermarket.

**8. Food and Beverages category generates the least revenue from churned customers.** Leverage the stability of this category by cross-selling and upselling to customers who primarily shop for groceries and suggest complementary products from higher-churn categories.

**9. Customers with poor credit scores have higher churn rates.** Develop financial wellness programs or partnerships with financial institutions to offer credit improvement resources. This can build loyalty while addressing a key churn factor.

**10. Churn rates and performance vary across branches (Dallas, Houston, San Antonio).** Implement localized retention strategies based on each branch's specific churn patterns and customer demographics. Share best practices across branches while allowing for local customization.

By implementing these data-driven recommendations, the supermarket chain can create a more personalized and engaging customer experience, potentially reducing churn rates and increasing overall customer lifetime value.

