# AdventureWorks-PowerBI

📊 AdventuresWork Power BI Dashboard Project
Welcome to my Power BI Retail Sales Dashboard, built using the AdventuresWork dataset.
This project is part of my Data Analyst journey to showcase data storytelling, dynamic visualizations, and strong DAX modeling for business insights.

🎯 Project Objectives:
Provide management-level KPIs on revenue, profit, returns, and sales trends

Analyze customer behavior by income group, age, and occupation

Highlight top-selling products, frequently returned items, and return rates

Compare actual performance vs targets

Create an interactive report that filters across country, product category, and customer segments

📊 Key Visuals & Insights:
Insight Area	Description
💰 Revenue Analysis	Trend of $24.9M revenue across 6 countries with yearly/monthly split
📈 Profit & Margin	$10.5M in profit with dynamic margin %
🛒 Order Insights	Total 25.2K orders analyzed for volume and profitability
📦 Returns Overview	Tracked number of returns, return % by product, and customer
🧍‍♂️ Customer Segmentation	Insights by income group, age category, and occupation
🎯 Target Achievement	Visuals showing performance vs target using DAX KPIs
🌍 Country-Wise Drilldown	Geo analysis of sales and returns across countries
🧠 Key DAX Measures Used:
Some of the many DAX measures created to drive this dashboard:

% of all Orders = DIVIDE([Total Orders],[All Orders])

% of All Returns = DIVIDE([Total Returns],([All Returns]))

Adjusted Price = [Average Retail Price]*(1+'Price Adjustment(%)'[Price Adjustment(%) Value])

Adjusted Profit = [Adjusted Revenue] - [Total Cost]

Adjusted Revenue = SUMX('Sales Data','Sales Data'[OrderQuantity]*[Adjusted Price])

All Orders = CALCULATE([Total Orders],All('Sales Data'))

All Returns = CALCULATE([Total Returns],All('Returns Data'))

Average Retail Price = AVERAGE('Product Lookup'[ProductPrice])

Total Cost = SUMX('Sales Data','Sales Data'[OrderQuantity]*RELATED('Product Lookup'[ProductCost]))

Total customers = DISTINCTCOUNT('Sales Data'[CustomerKey])

Total Orders = DISTINCTCOUNT('Sales Data'[OrderNumber])

Total Profit = [Total Revenue]-[Total Cost]

Total Returns = COUNT('Returns Data'[ReturnQuantity])

Total Revenue = SUMX('Sales Data','Sales Data'[OrderQuantity]*RELATED('Product Lookup'[ProductPrice]))

(And many more using CALCULATE, FILTER, ALLSELECTED, DATESYTD, etc.)

🧩 Data Model Overview:
Star schema built using:

FactInternetSales (fact table)

DimCustomer, DimProduct, DimDate, DimGeography, DimPromotion, etc.

Relationships created as 1-to-many (dimension to fact)

Date table used for time intelligence functions

Cleaned and transformed data using Power Query Editor

🧪 Filters, Interactions & Slicers:
Year, Country, Product Category, Occupation

Dynamic tooltips for KPIs

Drillthrough enabled for product-level and customer-level details

🌐 Live on LinkedIn:
📢 Shared on my LinkedIn: [(https://www.linkedin.com/posts/vishnu15050_power-bi-project-adventureswork-sales-activity-7314171937235116034-RUT4?utm_source=share&utm_medium=member_desktop&rcm=ACoAAC-6sSIB8RSi7Rez4NR5K2fkCWGUebTIKZE)]
I'd love to hear your feedback and suggestions 🙌

🛠️ Tools & Techniques Used:
Power BI Desktop

Power Query Editor

DAX (Data Analysis Expressions)

Star Schema Modeling

Interactive Visuals & Drillthrough

Custom Visuals and KPIs

Data Storytelling

🙌 Let’s Connect:
📩 If you're hiring or collaborating on dashboards, feel free to connect:
[LinkedIn Profile → Insert your URL here]

⭐ Future Improvements:
Add RLS (Row-Level Security) for restricted access views

Embed Power BI to web or internal portal

Add mobile layout for optimized viewing

📌 If you found this helpful, leave a star 🌟 on the repo and feel free to use the dataset for your own projects.

💌 With love,
Kathi Vishnuvardhan Reddy
Aspiring Data Analyst | Power BI Enthusiast
