# TripleTen Analyzing Profits & Losses for the Superstore - Tableau
This is the 2nd project I worked on in the TripleTen Business Intelligence Analytics program. It was my first time using Tableau.

## Superstore Analysis
This project aims to provide a comprehensive analysis of the superstore's performance to identify key areas for profit maximization and loss reduction. By examining various dimensions such as product subcategories, regions, and shipping modes, the project seeks to uncover the most significant profit centers and areas with the highest losses. Additionally, the project evaluates the potential effectiveness of targeted advertising and analyzes return rates to inform strategic business decisions. Through data-driven insights and visualizations, the goal is to recommend actionable strategies to enhance the superstore's overall profitability and efficiency.

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
#### Part 1: Profits & Losses
1. Identify Profit and Loss Centers:
  - Objective: Determine the key areas contributing to profits and losses within the superstore.
  - Approach:
    - Analyze combinations of dimensions such as subcategory + region and shipping mode + product ID.
    - Use visualizations (e.g., bar charts, heat maps) to identify and justify the two largest profit centers and two largest loss-makers.
  - Steps:
    - Loaded and cleaned the dataset.
    - Aggregated profit data by various dimension pairs.
    - Visualized the data to highlight the most significant profit and loss centers.
    - Interpreted the visualizations to identify actionable insights.
2. Identify Products to Stop Selling:
  - Objective: Determine which products are underperforming and should be discontinued.
  - Approach:
    - Created a visualization that shows profit margins for each product.
    - Identified products with consistently low or negative profits.
  - Steps:
    - Aggregated profit data by product.
    - Visualized the profit margins for each product.
    - Highlighted and listed the products with the lowest profit margins.
3. Focus and Stop Selling Subcategories:
  - Objective: Recommend subcategories to focus on and to stop selling.
  - Approach:
    - Analyzed profit data by subcategory.
    - Identified three subcategories with the highest profits and three with the lowest.
  - Steps:
    - Aggregated profit data by subcategory.
    - Created visualizations to compare subcategory performance.
    - Recommended three subcategories to focus on and three to discontinue.
   
#### Part 2: Advertising
1. Evaluate Advertising Opportunities:
  - Objective: Determine the best states and times of the year for advertising to maximize profit.
  - Approach:
    - Analyzed profit data by state and month.
    - Identified three state-month combinations with the highest average profits.
    - Visualized average profits by month for the top three states.
  - Steps:
    - Aggregated profit data by state and month.
    - Created visualization to show average monthly profits for each state.
    - Selected the top three state-month combinations based on profit data.
    - Calculated the recommended advertising spend based on a 1/5 profit to ad spend ratio.

#### Part 3: Returned Items
1. Analyze Return Rates:
  - Objective: Understand product and customer return behaviors.
  - Approach:
    - Integrated the Returns table with the Orders table using a LEFT JOIN.
    - Created a calculated field to categorize returns (1 for YES, 0 for null).
    - Visualized return rates by product and customer.
  - Steps:
    - Joined the Returns table with the Orders table.
    - Created a calculated field for return status.
    - Aggregated return data by product and customer.
    - Visualized return rates to identify products and customers with the highest return rates.
2. Profit vs. Return Rate Analysis:
  - Objective: Evaluate the relationship between profit and return rates across various dimensions.
  - Approach:
    - Create visualizations comparing average profit and return rates by selected dimensions (e.g., state, shipping mode, product type).
    - Provide a visual argument for retaining or discontinuing business practices based on these dimensions.
  - Steps:
    - Aggregated profit and return rate data by the chosen dimension.
    - Created visualizations to show the relationship between profit and return rates.
    - Interpreted the visualizations to make data-driven recommendations.

## Results
Through the use of different styles of bar charts and heat maps in Tableau, I was able to effectively communicate my findings to the stakeholders. 

Please have a look at my Tableau workbook. (https://public.tableau.com/views/TTProject_17132682180760/ProfitandLossAnalysisforSub-categoryandRegion?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Please note that these are projects I created some time ago. While they may not reflect my current skill level, they demonstrate my proficiency in Tableau and data visualization techniques at that time.
