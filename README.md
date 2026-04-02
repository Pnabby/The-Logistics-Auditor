# Delivery Performance Audit – Veridi Logistics

## A. Executive Summary

This project analyzes Veridi Logistics’ delivery performance by linking shipping data with customer reviews to understand the impact of delays on customer satisfaction across different regions. The analysis shows a clear relationship between delivery delays and lower review scores, with late orders consistently receiving poorer ratings than on-time and early deliveries. It also reveals that delays are not evenly distributed, as certain states experience significantly higher rates of late deliveries. Furthermore, a significant portion of revenue comes from some of these underperforming areas, suggesting that subpar delivery performance may have a direct impact on long-term business value and customer retention.

## B. Project Links

- **Link to Notebook:** https://github.com/Pnabby/The-Logistics-Auditor/blob/main/logistics_auditor.ipynb
- **Link to Dashboard:** https://lookerstudio.google.com/s/ulcz-BW8jHc
- **Link to Presentation:** https://docs.google.com/presentation/d/16QIoFELc5xI6m1fTeHrYHZAAHFcijYrQlHVNkK6QFVA/edit?usp=sharing

## C. Technical Explanation

**Data Cleaning:**
I merged the orders, reviews, and customers datasets into a single master table using **order_id** and **customer_id**. Duplicate reviews were handled by keeping only the most recent review per order. Date columns were converted to datetime format, and a **Days_Difference** column was created to measure delivery delay. Orders that were canceled or unavailable were excluded, and deliveries were classified as On Time, Late, or Super Late.

**Candidate's Choice:**
I analyzed the revenue impact of poor customer experiences by identifying orders with low review scores (review scores ≤ 2) and calculating their contribution to total revenue by state. This helped highlight regions where delivery issues not only affect customer satisfaction but also pose the highest financial risk.

## Key Insights

- Late deliveries lead to lower review scores.
- Some states have significantly higher delay rates.
- Poor-performing regions also generate high revenue.
- Delivery estimate accuracy is critical for customer satisfaction.

## Tools Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook
- Looker Studio / Tableau (Dashboard)
- GitHub

## Project Structure

├── dataset/
├── notebook.ipynb
├── notebook.html
├── README.md
