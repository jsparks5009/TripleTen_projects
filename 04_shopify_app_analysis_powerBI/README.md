# TripleTen Shopify App Analysis in PowerBI
This is the PowerBI project for the TripleTen Business Intelligence Analytics program. This was my first time using PowerBI.

## Shopify App
The task of the project was to use Power BI to conduct a comprehensive analysis of the Shopify app landscape to identify key success factors.

### The Data
The data was made up of one file, spread across four different sheets:

- `'reviews'`: each row corresponds to one review on the shopify app.
  - `'app_id'`: ID number that uniquely identifies the app.
  - `'author'`: the username of the individual who authored the review.
  - `'rating'`: The rating given by the reviewer.
  - `'posted_at'`: the date (day-month-year) the review was written.
  - `'body'`: the full text of the review.
  -  `'helpful_count'`: the number of people who found the review to be helpful.
  -  `'developer_reply'`: the full text of the developer's reply.
  -  `'developer_reply_posted_at'`: the date (day-month-year) the developer replied to the reviewer.

- `'apps-categories'`: each row corresponds to a unique app.
  - `'app_id'`: ID number that uniquely identifies the app.
  - `'category_id'`: ID number that identifies the category.

- `'apps'`: each row corresponds to a unique app.
  - `'id'`: ID number the uniquely identifies the app.
  - `'developer'`: the name of the company that developed the app.
  - `'rating'`: the average rating of the app.
  - `'reviews_count'`: the number of reviews the app has received.
  - `'description'`: a description of what the app does.
  - `'tagline'`: the tagline for the app.
  - `'pricing_hint'`: the cost of the app and whether or not additional charges apply.
  - `'lastmod'`: the date the app was last modified (month/day/year)

- `'categories'`: each row corresponds to a unique app.
  - `'id'`: ID number that uniquely identifies the app.
  - `'title'`: identifying the category title for the app.
    
 The data used was scraped from publicly available Shopify websites.

 ### The Process
 I explored and cleaned the shopify.xlsx dataset, merging DataFrames to create a unified dataset. Using Power BI, I created visualizations including KPI Cards, Line Charts, Scatterplots, and Bar Charts to analyze key metrics and trends.

 ## Results
 Presented findings effectively through a series of visualizations, making complex data understandable.
