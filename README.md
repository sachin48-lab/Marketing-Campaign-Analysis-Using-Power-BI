# Marketing-Campaign-Analysis-Using-Power-BI
To analyze and visualize the performance of marketing campaigns using customer and transaction data. The dashboard provides insights into campaign profitability, customer response rates, and purchasing behavior across different demographic segments.

![Marketing Campaign Analysis](/Marketing Campaign Analysis Using Power BI.png)

Charts showing:
- Sum of income by marital status and education
- Means of purchase (Catalog, Web, Store, Deals)
- Cost vs Revenue comparison
- Target vs Actual Response (Gauge visualization)
- Clean and modern UI with a custom teal color palette


DAX Formulas Used
- Total Purchase = SUM(ifood_df[No.CatalogPurchases]) + SUM(ifood_df[No.DealsPurchases]) + SUM(ifood_df[No.StorePurchases]) + SUM(ifood_df[No.WebPurchases])
- Target Response = 0.15 * SUM(ifood_df[Response])
- Campaign Profit = SUM(ifood_df[Z_Revenue]) - SUM(ifood_df[Z_CostContact])
- Conversion Rate = (SUM(ifood_df[Response])) / (SUM(ifood_df[Campaign_Overall]))
- ROI (%) = DIVIDE([Campaign Profit], SUM(ifood_df[Z_CostContact])) * 100


Tools Used
- Microsoft Power BI
- Power Query (for data cleaning and transformation)
- DAX (for custom calculations)
- Excel (data source)
