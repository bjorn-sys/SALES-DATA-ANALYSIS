# SALES-DATA-ANALYSIS

🛒 Sales Forecast Data Analysis

📌 Project Overview

This project focuses on the cleaning, preprocessing, and exploratory data analysis (EDA) of a sales dataset from an online retail platform. The goal is to understand purchasing trends, product performance, and seasonal sales variations using Python libraries like pandas, matplotlib, and seaborn.


---

📂 Dataset Summary

File Name: SALES FORCAST DATSET.csv

Total Rows: ~541,909

Columns: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country



---

🔧 Data Preprocessing Steps

1. Initial Data Inspection:

Used df.info(), df.describe(), and df.isnull().sum() to understand structure and missing values.

Identified 91 duplicated rows and dropped them.

Handled ~108,000 missing values in CustomerID and ~1,025 in Description.



2. Null Value Handling:

Filled missing object-type columns using their mode.



3. Data Cleaning:

Removed special characters (e.g., @, #, &, $) and non-alphanumeric values from key columns.

Removed emojis and symbols using regex from Country names.

Dropped the InvoiceNo column as it provided no analytical value.



4. Data Type Conversion:

Converted Quantity, StockCode, and UnitPrice to numeric.

Transformed InvoiceDate to datetime and extracted Year, Month, Day, Time.



5. Feature Engineering:

Created Seasons column from Month.

Added Price of sales column (UnitPrice * Quantity).

Renamed Description to Product and Quantity to Sales.





---

📊 Exploratory Data Analysis (EDA)

📦 Product-Level Insights

Top 20 Products by Sales Volume
Identified and visualized products generating the highest revenue.

Most Frequently Sold Products
Used count plots to identify popular products by purchase count.



---

📅 Time-Based Insights

Monthly Sales Trends
Line plot showing sales variations across months.

Seasonal Sales Performance
Pie and bar charts revealed higher sales during Winter, especially near festive periods.

Yearly Sales Trends
Sales trajectory over the years, including visual distribution by year using count and line plots.



---

🌍 Geographic Insights

Top Purchasing Countries
United Kingdom dominates sales (>91% of all sales).

Sales Distribution by Country
Identified countries contributing significantly to revenue.



---

📈 Other Visuals

Pie charts displaying sales breakdown by Year, Month, Season, and Country.

Line plots showing sales sum trends.



---

📎 Key Libraries Used

pandas
numpy
matplotlib
seaborn
missingno
re


---

🧠 Insights & Conclusions

United Kingdom is the major revenue generator.

Sales spike during Winter, likely due to holiday shopping.

Specific products are purchased repeatedly, indicating strong brand loyalty or demand patterns.

Data cleaning is essential as the raw dataset had many formatting issues, missing values, and anomalies.



---

📌 Next Steps (Optional Suggestions)

Forecast future sales using models like ARIMA, Prophet, or machine learning techniques.

Cluster customers for targeted marketing.

Analyze cart abandonment if more data is available.



---

📁 Folder Structure Suggestion

📁 Sales_Analysis_Project
│
├── 📊 EDA_Notebook.ipynb
├── 📄 SALES FORCAST DATSET.csv
├── 📄 README.md
├── 📁 plots/
│   └── sales_by_month.png
│   └── top_products.png
│   └── seasonal_sales.png


---

🙌 Acknowledgments

Special thanks to the source of the dataset and the open-source community for the powerful Python libraries used in this analysis.

