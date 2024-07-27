# TripleTen Restaurant Analysis - Tableau
This was the final project for the TripleTen Business Intelligence Analytics Program. We had the option to use either Tableau or PowerBI to complete this project.

## Restaurant Analysis
The project task was to analyze restaurant data to identify the most popular and profitable restaurants and understand the factors contributing to their success.

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

  ### The Process
  I cleaned and standardized the restaurant data, merged datasets based on common keys, and created calculated fields for key metrics. Using Tableau, I developed an overview dashboard and detailed analysis dashboards to visualize total orders, revenue, customer ratings, and the impact of factors such as location, cuisine type, and menu diversity.

  ## Results
  The analysis identified the most popular and profitable restaurants, highlighting key factors contributing to their success. Findings were summarized in an executive report, providing insights into top-performing restaurants and recommendations for future research.

Please have a look at my Tableau workbook: https://public.tableau.com/views/RestaurantAnalysis_17185382314290/PDFStory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
