
[![Open In Power Bi](https://img.shields.io/badge/open_in_power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiMTQ1YjJiODctNmJjMS00NGYwLWFjMWEtNGE5YzdkYWUyYzIwIiwidCI6ImFlZDI3MWNkLTYzOTgtNDllZi1hOWNmLTQ4NDIyMTAxZTE0ZSIsImMiOjEwfQ%3D%3D)

💊 Pharmaceutical Sales Analysis – Student Project
📌 Introduction

This project was developed as part of my college coursework in Data Analytics & Visualization.
The main objective was to explore, clean, and analyze a pharmaceutical sales dataset, then present the findings using an interactive Power BI dashboard.

The fictional company, PharmaCo, operates in multiple regions and sells products through distributors to pharmacies and hospitals. The dataset provided was in .csv format and represents wholesale-to-retail transactions.

While the business scenario is realistic, the dataset was adapted for educational purposes.

🎯 Objectives

Practice data cleaning & transformation using Power Query Editor.

Build an interactive Power BI dashboard for quick insights.

Analyze sales trends by year, month, product, and region.

Identify top products, top cities, and top-performing sales teams.

Learn how to apply EDA (Exploratory Data Analysis) concepts on real-world-like data.

📂 Dataset

The dataset contains fictional sales transactions with the following fields:

Field	Description
Distributor	Name of wholesaler
Customer Name	Name of customer (pharmacy, hospital, etc.)
City	Customer’s city
Country	Customer’s country
Channel	Type of buyer (Hospital, Pharmacy)
Sub-channel	Sector of buyer (Government, Private, etc.)
Product Name	Medicine/drug name
Product Class	Class of drug (Antibiotics, etc.)
Quantity	Quantity purchased
Price	Selling price per unit
Sales	Total revenue from the sale
Month	Month of sale
Year	Year of sale
Sales Rep	Sales representative name
Manager	Sales manager’s name
Sales Team	Team name of sales rep

🛠 Tools & Technologies Used

Power BI Desktop – Dashboard creation & visualization
Power Query Editor – Data transformation & modeling
Python (pandas) – Exploratory Data Analysis (optional)
Power BI Service – Publishing the report for web access

## Dataset
The dataset is sourced from each distributor. It contains Pharmaceutical Manufacturing Company’s, Wholesale-Retail Data. The field description of the raw data is given below. The raw dataset `pharma-data.csv` can be downloaded from [here](https://drive.google.com/file/d/1npKF_C2tG5psY-at4wvpEgh6T-7KHxEZ/view?usp=share_link)

📊 Project Workflow

Exploratory Data Analysis (EDA)

Checked for missing values, unusual entries, and outliers.

Identified categorical & numerical fields.

Confirmed realistic ranges for sales and quantities.

Data Cleaning & Transformation

Renamed columns for clarity.

Fixed data types (e.g., numbers, dates, text).

Removed any incorrect/duplicate entries.

Data Modeling

Created a star schema model in Power BI.

Separated facts (sales data) from dimensions (product, customer, date, etc.).

Established relationships for efficient filtering.

Dashboard Creation

Executive Summary Page – Overall sales KPIs & trends.

Customer & Distributor Analysis Page – Sales by distributor, city, and product.

Sales Team Performance Page – Sales by team, manager, and rep.
## Solution Approach 

|Requirement ID|Solution ID|Proposed Solution|
|:--|:---|:--|
|DM-DA01-REQ-1|DM-DA01-SOL-1|An `Executive Summary` PowerBI dashboard/report page will be built to show a high-level overview of sales data in interactive visuals per the requirements. A `year` filter will be provided to filter the data by a particular or combination of years |
|DM-DA01-REQ-2|DM-DA01-SOL-2|A `Distributor & Customer Analysis` PowerBI dashboard/report page will be provided with interactive visuals showing data as per the requirement|
|DM-DA01-REQ-3|DM-DA01-SOL-3|A `Sales Team Performance` PowerBI dashboard/report page will be provided with interactive visuals showing data as per the requirement. `year` and `month` slicers will be provided to slice/filter data by year and/or months|

***Table-3 : Proposed Solution***

### Exploratory Data Analysis (EDA) [pandas]
To understand, be familiar with and check the sanity of the given data, the first step is EDA. This project's initial data exploration has been carried out using the `pandas` python package. Here, in general, we are checking... 
 * Presence of any missing values 
 * Any unusual value (outliers) 
 * Incorrect values (e.g., sales column, we see -ve numbers)
 * Determine `categorical` and `numeric` columns
 * Determine dimensions of categorical columns and range of numeric columns
Note that these steps can be performed using `PowerQuery Editor` and/or excel; however, `pandas` makes it much easier and faster; on top of that, `pandas` can handle massive datasets.

EDA steps can be found in the `data-exploration.ipynb` notebook.

### Data Cleaning and Transform [PowerQuery Editor]
The provided dataset was relatively clean and well organized; hence only a little work was required in this step; the following steps were carried out...
* Correct column heading provided
* Correct data type is assigned to columns

### Data Model Creation [PowerBI Desktop]
* The provided data is in a single table format. The exploration revealed that it contains both categorical (`dimensions`) and numeric (`facts`) data. 
* We build a data model where dimensions and facts are separated, then they are linked together by logical relationship to form a `star schema.` The resultant data model is shown below...

<img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/data-model.png?raw=true"/>

The tables with the prefix `DIM` are dimension tables, and `FACT` is the fact table.

### Report Creation [PowerBI Desktop]
Three interactive reports/dashboards (report pages) will be created to implement the proposed solution. Refer to [Table-3: Proposed Solution](#solution-approach) for detailed requirements and the corresponding proposed solution. 

#### 1. Executive Summary Report [DM-DA01-SOL-1]
This high-level report shows the overall sales figures and elements at a glance.

<img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/exec-summary-page.png?raw=true"/>

#### 2. Distributor & Customer Analysis Report [DM-DA01-SOL-2]
This more granular detailed report analyses data from the company distributors' and customers' perspectives. Sales by the distributor can be drilled down to specific product levels.
 
 <img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/dist-cust-analysis-page.png?raw=true"/>
 
 #### 3. Sales  Team Performance Report [DM-DA01-SOL-3] 
 This is another detailed report that analyses the performance of the company's sales team. Sales by the sales team can be drilled down to product class and specific product levels.
 
 <img src="https://github.com/sssingh/pharmaceutical-sales-analysis-powerbi/blob/main/images/sales-team-perform-page.png?raw=true"/>


📚 Learning Outcomes

Through this project, I learned:

How to apply data transformation techniques in Power Query.

Designing star schema models for BI reporting.

Creating dynamic, slicer-driven dashboards in Power BI.

Communicating insights visually for decision-making.

📜 License & Credits

This project is licensed under the MIT License, which allows reuse, modification, and distribution with proper attribution.
Original inspiration & dataset structure adapted from an open-source Power BI project by Sunil Singh (MIT License).

MIT License link: https://choosealicense.com/licenses/mit/
