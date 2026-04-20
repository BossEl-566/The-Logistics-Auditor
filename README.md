## Executive Summary

This project analyzed delivery performance and its impact on customer satisfaction using the Olist e-commerce dataset, comprising over 99,000 orders. The analysis reveals that while the majority of deliveries are completed ahead of schedule, with an average delivery occurring approximately 12 days earlier than the estimated date, a small proportion of delayed deliveries has a significant negative impact on customer experience.

Specifically, 93% of orders were delivered on time or early, achieving an average review score of 4.29/5, while delayed orders experienced a sharp decline in customer satisfaction. Orders classified as “Late” recorded an average score of 2.99/5, and “Super Late” deliveries dropped further to 1.74/5, demonstrating a strong negative correlation between delivery delay and customer sentiment.

Geographic analysis indicates that delivery issues are not uniformly distributed, with certain states experiencing significantly higher delay rates, such as Alagoas (21.4%) and Maranhão (17.4%), compared to the national average. This suggests localized logistics inefficiencies rather than a systemic nationwide failure.

Further analysis at the product level reveals that bulky and logistics-intensive categories, including furniture and home-related products, exhibit higher delay rates, indicating operational challenges in handling and transportation. These insights highlight critical areas for targeted logistics optimization, particularly in high-risk regions and product segments, to improve overall customer satisfaction.

## B. Project Links

- Notebook: (https://github.com/BossEl-566/The-Logistics-Auditor.git)
- Dashboard: [Your Tableau Public Link]
- Presentation:(https://public.tableau.com/app/profile/elliot.datsomor/viz/DeliveryPerformanceAuditImpactofLogisticsonCustomerSatisfaction/Dashboard1?publish=yes)

## C. Technical Explanation

### Data Cleaning
The dataset was sourced from multiple relational CSV files and required careful preprocessing. I joined the Orders, Customers, and Reviews tables using appropriate keys (`order_id` and `customer_id`) while ensuring that no duplicate rows were introduced. Since the reviews dataset contained multiple entries per order, I aggregated review scores to maintain a one-row-per-order structure. Missing values, particularly for non-delivered orders, were handled by filtering only completed deliveries for delay analysis.

### Candidate’s Choice Feature
To extend the analysis, I introduced a product category-based delivery performance evaluation. By mapping each order to its dominant product category using the order items and product datasets, I identified categories with higher late delivery rates. This analysis revealed that bulky and logistics-intensive items such as furniture and home-related products are more prone to delays, providing actionable insights for targeted operational improvements.