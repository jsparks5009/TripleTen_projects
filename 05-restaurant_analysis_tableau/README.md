# TripleTen Restaurant Analysis - Tableau
This project was the capstone assignment for the TripleTen Business Intelligence Analytics Program. Participants could choose between Tableau and PowerBI for their analysis and select the type of analysis they wished to conduct. Additionally, each participant was responsible for developing their own decomposition plan. The three analysis options available were as follows:
- Customer Analysis Segmentation: who are Zomato’s customers? What segments can we split them into? What is their purchasing behavior?…
- Restaurant Analysis: What restaurants are popular? What restaurants generate the highest revenue? Why?…
- Sales Analysis: Dynamics of sales/revenue overtime, main KPIs, change in distribution of sales and so on…

I chose the Restaurant Analysis for my project.

## Restaurant Analysis
The objective of this analysis is to thoroughly assess restaurant performance using Zomato Restaurant data, incorporating three critical datasets: Orders, Restaurant, and Menu. By analyzing key metrics such as customer ratings, order volume, and revenue, we aim to pinpoint the most popular and profitable restaurants and uncover the underlying factors contributing to their success. Through the use of interactive dashboards and filters, we will offer a comprehensive view of restaurant performance, which will support strategic decision-making. This analysis not only explores customer satisfaction and revenue generation but also delves into the influence of menu diversity and pricing on overall success. The insights gained will enable stakeholders to make informed, data-driven decisions to optimize business strategies and improve performance.

### The Data
The data was spread across five files:

- `'restaurant'`: each row corresponds to one restaurant.
  - `'id'`: ID number that uniquely identifies each restaurant.
  - `'name'`: the name of the restaurant
  - `'city'`: the city where the restaurant is located.
  - `'rating'`: the average rating of the restaurant.
  - `'rating_count'`: the amount of ratings the restaurant has.
  - `'cost'`: the average cost one can expect to spend at the restaurant.
  - `'cuisine'`: the type of cuisine available at the restaurant.
  - `'lic_number'`: the restaurant's license number.
  - `'link'`: the restaurant's website link.
  - `'address'`: the address of the restaurant.
  - `'menu'`: ID number that uniquely identifies the menu.
    
- `'users'`: each row corresponds to a unique user.
  - `'user_id'`: ID number that uniquely identifies each user.
  - `'name'`: the user's name.
  - `'email'`: the user's email address.
  - `'password'`: the user's password.
  - `'age'`: the user's age.
  - `'gender'`: the user's gender.
  - `'marital_status'`: the user's marital status.
  - `'occupation'`: the user's occupation, categorized as: student, employee, self-employed, house wife.
  - `'monthly_income'`: the user's monthly income, presented in ranges.
  - `'education_qualification'`: the user's education qualification, categorized as: uneducated, school, graduate, post graduate, Ph.D
  -  `'family_size'`: the user's family size.
    
- `'orders'`: each row corresponds to a unique user.
  - `'order_date'`: the date the order was placed.
  - `'sales_qty'`: how many items were included in the order.
  - `'sales_amount'`: the total monetary amount for the order.
  - `'currency'`: the currency (Indian Rupees).
  - `'user_id'`: ID number that uniquely identifies each user that placed the order.
  - `'r_id'`: ID number that uniquely identifies which restaurant in which the order was placed.
     
- `'food'`: each row corresponds to a different menu item.
  - `'f_id'`
  - `'item'`: the name of the dish on the menu.
  - `'veg_or_non_veg'`: clarifies whether the dish is vegetarian or not.
     
- `'menu'`: there are multiple rows associated with each menu id.
  - `'menu_id'`: ID number that uniquely identifies the menu.
  - `'r_id'`: ID number that uniquely identifies the restuarant in which the menu can be found.
  - `'f_id'`
  - `'cuisine'`: the type of cuisine.
  - `'price'`: average price.
 
  The data is provided by TripleTen, who scraped it from Zomato.

  ## The Process
  ### Research Questions
  #### 1. Popularity Analysis:
    - Which restaurants receive the most orders?
    - Which restaurants have the highest number of unique customers?
    - What are the characteristics of restaurants with the highest customer ratings?
  #### 2. Profitability Analysis:
    - Which restaurants generate the highest revenue?
    - What is the average revenue per order for the top-performing restaurants?
  #### 3. Factor Analysis:
    - How does the location of a restaurant affect its popularity and profitability?
    - What types of cuisines are most popular and profitable?
    - Does menu diversity influence customer satisfaction and restaurant performance?
 
  ### Hypotheses
  1. Restaurants offering a targeted menu produce more revenue than restaurants with more variety.
  2. Higher customer ratings do not necessarily correspond to higher revenues.
  3. Restaurants with more customer ratings have a higher number of overall orders.

 ### Visualizations
 #### 1. Overview Dashboard:
   - Total Orders by Restaurant: Bar chart showing the number of orders for each restaurant.
   - Total Revenue by Restaurant: Bar chart depicting total revenue generated by each restaurant.
   - Customer Ratings: Scatterplot of customer ratings vs. number of orders.
#### 2. Detailed Analysis Dashboards:
  - Popularity Analysis:
    - Unique Customers by Restaurant: Bubble chart showing the number of unique customers.
    - Repeat Customer Rate: Line chart showing repeat customer trends over time.
    - Average Order Size and Value: Combined bar and line chart displaying average order size and value for the highest revenue restaurants.
  - Profitability Analysis:
    - Revenue per Order: Box plot showing distribution of revenue per order across highest earning restaurants.
  - Factor Analysis:
    - Location Impact: Geographical map showing restaurant locations with markers sized by revenue and colored by popularity.
    - Cuisine Type Analysis: Tree map showing revenue and popularity by cuisine type of top earning restaurants.
    - Menu Diversity: Bar chart showing the relationship between menu diversity and average customer ratings.
  
  ## Results
 The analysis of Zomato Restaurant data offers key insights into the factors affecting restaurant performance. It highlights that high customer ratings significantly boost order volumes, especially when ratings exceed 3.5, emphasizing the need for continuous efforts to enhance customer satisfaction. Revenue generation is influenced by strategic pricing, with success achieved either through high sales of lower-priced items or fewer sales of higher-priced ones. The findings also stress the importance of customer loyalty and effective menu strategies, noting that focused menus and specialized cuisines generally receive higher ratings and foster greater loyalty.

Additionally, the study reveals that nationwide chains benefit from their extensive market presence, while regional strategies and seasonal promotions can further optimize performance. Future research should explore customer demographics, operational efficiency, and competitor performance to refine strategies and drive ongoing improvements.

Please have a look at my Tableau workbook: https://public.tableau.com/views/RestaurantAnalysis_17185382314290/PDFStory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
