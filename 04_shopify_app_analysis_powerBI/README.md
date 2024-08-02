# TripleTen Shopify App Analysis in PowerBI
This Power BI project is part of the TripleTen Business Intelligence Analytics program. As my first experience with Power BI, the project involved creating specific charts and KPI cards according to the given requirements. The deliverables included submitting screenshots to verify that each task had been completed accurately.

## Shopify App
This project involves a comprehensive analysis of the Shopify app landscape using data scraped from publicly available Shopify websites. Leveraging Power BI, the goal is to uncover key factors influencing the success of Shopify apps. The analysis is divided into three main parts: examining overall app statistics, reviewing user feedback, and evaluating app performance metrics. Each part involves creating specific visualizations and KPIs to present insights effectively. By systematically addressing these components, the project aims to provide a detailed understanding of the factors contributing to app success on the Shopify platform.

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
#### Part 1: App Landscape
- KPI Card - Unique Apps Count
  - Added a KPI Card visual and set it to display the unique count of apps from the `apps` table.
- Line Chart - Review Count Over Time
  - Added a Line Chart visual with the Y-axis showing the sum of `review_count` from the `apps` table and the X-axis displaying the `lastmod date` from the `apps` table.
- Scatterplot - Reviews Count vs. Average Rating
  - Added a Scatterplot visual and set the X-axis to show `reviews_count` from the `apps` table and the Y-axis to display `average rating` from the `apps` table.
  - Inserted a Text Box next to the Scatterplot to annotate the interpretation of the data.

#### Part 2: Reviews
- KPI Card - Average Helpful Reviews
  - Created a Column in the `Reviews` table with the DAX expression: `helpful_reviews = rating * (1 + helpful_count)`.
  - Added a Card visual to the `Reviews` sheet to display the average value of the `helpful_reviews` column.
- Scatterplot - Developer Answered vs Rating
  - Created a new Column in the `Reviews` table with the Dax expression: `developer_answered = IF(ISBLANK(developer_reply), 0, 1)`.
  - Added a Scatterplot visual to compare the average rating on the Y-axis with the `developer_answered` column on the X-axis.

#### Part 3: App Reviews
- Bar Chart - Developer vs. Sum of Ratings
  - Established a relationship between the `Reviews` table and the `Apps` table using `app_id` from `Reviews` and `id` from `Apps`.
  - Set the relationship as many-to-one (many from `Reviews` to one from `Apps`).
  - Added a Bar Chart visual to the sheet with `developer` on the X-axis and the sum of `rating` on the Y-axis.
- Bar Chart - Developer vs. Average Helpful Reviews
  - Added another Bar Chart visual and set `developer` on the X-axis and the average of `helpful_reviews` on the Y-axis.
- Bar Chart - Developer Responsiveness
  - Added a Bar Chart visual to the sheet and set `developer` from the `apps` table on the X-axis and the `developer_answered` column on the Y-axis.
  - Added a Filter to include only rows where `reviews_count` was greater than 500.

## Results
This process helped systematically analyze the Shopify app landscape, review patterns, and app performance metrics.
![Screenshot 2024-08-02 082154](https://github.com/user-attachments/assets/abc6f5c1-35a9-44c8-8887-7f06e4de2293)
![Screenshot 2024-08-02 082319](https://github.com/user-attachments/assets/e5c737f2-be74-41fd-ab69-2cc3472bc3d5)
![Screenshot 2024-08-02 082354](https://github.com/user-attachments/assets/3d7f6c3a-ad5c-4591-97b4-c560369b84c9)


