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
    - Bubble Chart: Developed a bubble chart displaying regional return rates vs. profit to highlight whether or not a higher return rate correlates with profits.

## Results
By utilizing various data visualizations, including scatter plots, interactive maps, line charts, bar charts, and heat maps, I effectively communicated my findings to the stakeholders. The presentation concluded with a comprehensive implementation plan.

Please have a look at my Tableau workbook. https://public.tableau.com/views/TTDashboardProject/SuperstoresStoryofReturnRates?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

Please note that these are projects I created some time ago. While they may not reflect my current skill level, they demonstrate my proficiency in Tableau and data visualization techniques at that time.
