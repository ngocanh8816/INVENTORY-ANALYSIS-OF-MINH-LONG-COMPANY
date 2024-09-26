# INVENTORY ANALYSIS OF MINH LONG TECHNOLOGY COMPANY
Analysis of import - export flow and inventory management efficiency of Minh Long Technology Company.
# Overviews
The **Inventory Analysis** project covers the following areas:

+ **Data collection**: Utilize the internal dataset that records the process of importing and exporting goods from the company.
+ **Data preparation**: Cleaning and preprocessing the data for analysis.
+ **Descriptive analysis**: Calculate the metrics and provide insights on the warehouse operations performance.
+ **Propose solutions**: Propose solutions to improve the company's warehouse operations.

# Applied Skills
ETL Data, Data Analysis, Data Visualization 

# Key Features

+ **Data collection**: The dataset is extracted from the internal data source of Minh Long Engineering Joint Stock Company.
+ **Data preparation**: Steps to clean and preprocess the data, including handling missing values, converting data types and handling NULL data.
+ **Transform data**: Calculate key metrics in warehouse operations, product performance, costs, etc.
+ **Data visualization**: Create Measures and Columns in Power BI to calculate and transform the necessary data fields for visualization and reporting purposes.
# Key Findings

+ **Popular content**:

  The analysis emphasizes data processing techniques using Python. It also provides an overview of the company’s warehouse operations and storage activities.

  The analysis delves into each type of product using calculated metrics to propose optimal measures for storing, exporting, and importing those goods.
+ **The growth in inventory levels and storage costs**:

  Use a line chart to simultaneously represent the growth in inventory levels and storage costs during the period 2021-2022.

  Inventory levels and storage costs are closely correlated, often fluctuating in the same direction. This indicates that the company is facing significant increases in both inventory levels and storage costs.
+ **Analysis of warehouse import and export flow by product category**:

  *Gearbox*: The import and export volumes of the warehouse fluctuated across the quarters, not       following a stable trend. Both tended to decrease in the last two quarters of 2022. Although inventory increased, the growth rate tended to slow down in the last quarters.
  
  *Gearmotor*: Regarding inventory levels, there was a general upward trend from Q2/2021 to Q2/2022, followed by a slight decrease at the end of each year. The volumes of products imported and exported also fluctuated, notably with import volumes peaking in Q2/2021 and gradually decreasing thereafter.
  
  *Motor*: In the first quarter of 2022, this product recorded the highest levels of inventory inflow and outflow during the business period. However, these two indicators tend to decrease sharply in the fourth quarter of each year.
  
  *Inverters*: There was a significant decrease (30%) in both inventory inflow and outflow from Q3 to Q4/2022. This decline may reflect a change in customer demand or an adjustment in the company’s business strategy.

+ **Featured Products:**:

  Motors have the highest inventory growth rate (31.58%).
  
  Gearboxes remain the product with the largest inventory.
  
  Inverters are a new product introduced in 2022.

+ **Analysis of the correlation between inventory inflow - outflow - stock for each product category**:

  *Gearbox*: High inventory inflow but low outflow has led to high stock levels (52.67%). This indicates an imbalance between market demand and the quantity of goods imported, resulting in large inventory.

  *Gearmotor*: The rate of inventory inflow and outflow is quite balanced but still leads to relatively high inventory levels (30.31%). This may indicate a discrepancy between demand and supply.

  *Motor*: High inventory inflow and outflow with a low inventory rate (17.03%). This reflects good market demand and effective inventory management, indicating that the business strategy aligns well with market needs.

  * *Inverters*: Low inventory inflow but higher outflow than inflow, and no inventory remaining. This indicates that the product is consumed immediately after being stocked, reflecting high market demand for this type of product.
# Outcomes

+ The company may need to reconsider its strategy for Gearbox products, including reducing imports or finding ways to enhance marketing and sales to increase the outflow rate.

+ Limit import activities to minimize excessive inventory accumulation for Gearmotor product lines, and also boost marketing activities to stimulate purchasing demand.

+ Continue to maintain the current strategy to ensure sufficient supply and reduce the risk of stockouts. The company may need to consider diversifying the types of products in the Motor line to further mitigate risks and take advantage of the broader market opportunities.

# Example Code

Here's a snippet of the initial setup in Google Colab:

```
import pandas as pd
import numpy as np
from collections import Counter

# Đọc file
df_product = pd.read_csv('Product.csv',encoding='ISO-8859-1',header=None)
df_export = pd.read_csv('Export.csv',encoding='utf-8')
df_import = pd.read_csv('Import.csv',encoding='ISO-8859-1')

# Làm sạch dữ liệu
## Xóa 2 dòng đầu tiên và điều chỉnh lại chỉ mục
df_product = df_product.drop(index=[0,1]).reset_index(drop=True)
## Set dòng đầu tiên thành header
df_product.columns = df_product.iloc[0]
df_product = df_product[1:]
## Đổi tên cột
df_product.rename(columns={
    'Code': 'Model code'
}, inplace=True)
```
# Project Structure

The project includes the following main components:

+ `README.md`: This file provides information and an overview of the analysis results.
  
+ `Inventory Analysis of Minh Long Tech`: The Google Colab file contains code for processing, transforming, and retrieving data.






