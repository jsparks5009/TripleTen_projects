# TripleTen Analyzing Profits & Losses for the Superstore - Tableau
This is the 2nd project I worked on in the TripleTen Business Intelligence Analytics program. It was my first time using Tableau.

## Superstore Analysis
The goal of the projects was to use Tableau to identify key profit and loss centers, determine product focus areas, and evaluate the effectiveness and profitability of advertising strategies for the Superstore using data visualizations.

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
I first explored the dataset and then loaded it to Tableau and left-joined the `'Orders'` and `'Returns'` sheets. Finally, I analyzed the data using visualizations. 

## Results
Through the use of different styles of bar charts and heat maps in Tableau, I was able to effectively communicate my findings to the stakeholders. 

Please have a look at my Tableau workbook. (https://public.tableau.com/views/TTProject_17132682180760/ProfitandLossAnalysisforSub-categoryandRegion?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Please note that these are projects I created some time ago. While they may not reflect my current skill level, they demonstrate my proficiency in Tableau and data visualization techniques at that time.
