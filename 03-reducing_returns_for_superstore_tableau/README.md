# TripleTen Reducing Returns: Analyzing Causes and Strategies for the Superstore - Tableau
This is the 3rd project I worked on in the TripleTen Business Intelligence Analytics program. It was my first dashboard project in Tableau.

## Superstore Analysis
In this project, I conducted an in-depth analysis of the high number of returned orders at a Superstore to assist the CEO in understanding and reducing return rates. Using the `Superstore.xls` dataset, I joined the `Returns` and `Orders` tables and created various calculated fields to accurately measure return rates. I developed multiple visualizations, including scatterplots, bar charts, maps, and composite charts, to identify patterns and root causes of returns across different dimensions such as product category, customer behavior, geography, and time. The insights gained from this analysis were compiled into a comprehensive Tableau Story, which was presented in a PDF report.

### The Data
The data was made up of one file, in three seperate sheets:

- `'Orders'`: Each row corresponds to one order for the Superstore.
  -  `'Row_ID'`: The row id.
  -  `'Order_ID'`: ID number that uniquely identifies each order.
  -  `'Order_Date'`: Date that the order was placed.
  -  `'Ship_Date'`: Date that the order was shipped.
  -  `'Ship_Mode'`: Mode of shipping (First class, Second class, Standard, etc).
  -  `'Customer_ID'`: ID number that uniquely identifies each customer.
  -  `'Customer_Name'`: The name of the customer.
  -  `'Segment'`: Classified as three categories: Consumer, Corporate, Home Office.
  -  `'Country/Region'`: The country in which the order was placed.
  -  `'City'`: The city in which the order was placed.
  -  `'State'`: The state in which the order was placed.
  -  `'Postal_Code'`: The postal code in which the order was placed.
  -  `'Region'`: The region of the United States in which the order was placed.
  -  `'Product_ID'`: ID number that uniquely identifies each product.
  -  `'Category'`: Each product fits into one of three categories: furniture, office supplies, technology.
  -  `'Sub-Category'`: Each product fits into one sub-category: supplies, binders, labels, appliances, storage, accessories, bookcases, art, furnishings, tables, paper, machines, fasteners, phones, envelopes, chairs, copiers.
  -  `'Product Name'`: The name of each product.
  -  `'Sales'`: The monetary amount of each sale.
  -  `'Quantity'`: The amount of each product in the sale.
  -  `'Discount'`: The discount percentage, if any, applied to the sale.
  -  `'Profit'`: Total profit of the sale.
 
- `'People'`
  - `'Regional_Manager'`: The name of the manager for the specified region.
  - `'Region'`: Which region the manager is located in.
 
- `'Returns'`
  - `'Returned'`: A yes/no answer to whether an item was returned or not.
  - `'Order_ID'`: ID number that uniquely identifies each order.
 
The dataset is provided by TripleTen.

### The Process
#### 1. What was the cause of returns?
- Objective: To identify the causes of high return rates at the Superstore.
- Approach:
  - Utilized the `Superstore.xls` dataset to join the `Returns` and `Orders` tables.
  - Created calculated fields to accurately measure return rates.
  - Developed various visualizations, including scatterplots, bar charts, maps, and composite charts.
- Steps:
  - 1. Data Preparation and Joining
    - Ensured the `Returns` table is LEFT JOINED onto the `Orders` table to view both "Yes" and "null" values in the `Returned` column.
    - Created calculated fields for the `Returned` column where null values are assigned 0 and "Yes" values are assigned 1. This calculated field's average represents the return rate.
      - `'Returned Values'` = `IF ISNULL([Returned]) THEN 0 ELSEIF [Returned] = "Yes" THEN 1 ELSE 0 END`
      - `'Return Rate'` = `AVG([Returned Values])`
  - 2. Analysis Worksheets
    - Scatterplot: Built a scatterplot showing the correlation between total sales and total returns, aggregated by product subcategory.
    - Bar Chart: Created a bar chart to display the return rate by product category, highlighting which categories have higher return rates.
    - Customer Return Rate: Developed a view showing the return rate by customer, applying a filter to exclude customers with only one order to identify those more prone to making returns.
    - Geographic Analysis: Constructed a map illustrating the return rate by geographic measure (state), revealing any concentration of returns.
    - Temporal Analysis: Created a line chart showing the return rate over time (month) to identify any seasonal effects on returns.
    - Heat Map: Developed a heat map displaying return rates by sub-category and region to identify trends and patterns in return behavior.
    - Bubble Chart: Created a bubble chart comparing regional return rates with profit to assess whether a higher return rate correlates with increased or decreased profitability.
    - Dashboards: Constructed dashboards in a presentation style to create compelling slides and save a completed version of the Tableau Story.

#### 2. Presenting my Analysis
- Story Arc Construction:
  - Objective: Create a draft of the story using captions for each story point, including:
    - A summary of the returns analysis.
    - A discussion on the best measures for returns and when each measure is appropriate.
    - Identification of key root causes of returns.
    - An overview of each dashboard component, explaining the contents and interpretation of each chart.
    - A demonstration of how to use the dashboard, including interpreting data and using filters to identify root causes.
    - Propose actions based on dashboard insights and a conclusion with next steps, such as implementing the dashboard.

## Results: The PDF Presentation
![1](https://github.com/user-attachments/assets/0e5575ce-c60b-494c-9fce-d74cc157bbab)
![2](https://github.com/user-attachments/assets/0b8a7589-9cf6-4b27-9133-d29d941fa26b)
![3](https://github.com/user-attachments/assets/0dc5c02e-632e-4416-84f3-43741697504f)
![4](https://github.com/user-attachments/assets/93ae2fe4-6edf-4c40-ae70-fca3dd07625d)
![5](https://github.com/user-attachments/assets/b09624bb-24bf-44b7-a24a-b78b47f09ca3)
![6](https://github.com/user-attachments/assets/b966fe09-cffa-4ef1-aabc-7dbf2726c5ff)
![7](https://github.com/user-attachments/assets/43342abd-b909-49c4-bc75-f95dcad32e5c)
![8](https://github.com/user-attachments/assets/27bbd9a2-ee92-4d22-a3a5-83a3a438730b)
![9](https://github.com/user-attachments/assets/ea21dc70-3f88-444a-ad4d-68fcf381a2ca)
![10](https://github.com/user-attachments/assets/23ab3639-1703-42d7-85a5-e76f7e311df9)
![11](https://github.com/user-attachments/assets/4428cf34-9395-4f82-80f1-405765a95fde)
![12](https://github.com/user-attachments/assets/8f881582-4266-4fa9-a53d-03c519bd701c)
![13](https://github.com/user-attachments/assets/f5e3f258-a400-416f-87ab-b4f190425b90)
![14](https://github.com/user-attachments/assets/89df5c67-5594-42ec-8951-0bd3e433d4ab)
![15](https://github.com/user-attachments/assets/d5d8c9fd-e9f8-427d-95be-d943ba29bc4e)
![16](https://github.com/user-attachments/assets/8b6ec10a-c8f4-44b0-9078-413b57d67791)
![17](https://github.com/user-attachments/assets/f61db736-70f9-4bff-b954-446a1fd2226d)
![18](https://github.com/user-attachments/assets/1151e940-f885-4ea7-ba19-633410ff5136)


Please have a look at my Tableau workbook. https://public.tableau.com/views/TTDashboardProject/SuperstoresStoryofReturnRates?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

Please note that these are projects I created some time ago. While they may not reflect my current skill level, they demonstrate my proficiency in Tableau and data visualization techniques at that time.
