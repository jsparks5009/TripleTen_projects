# TripleTen Manhattan Airbnb Spreadsheets Project
This is the 1st project I worked on in the TripleTen Business Intelligence Analytics program. I really enjoyed learning the ins and outs of spreadsheets.

## Potential Investment Properties in Manhattan
This project involves analyzing the vacation rental market in the Manhattan borough of New York City using Airbnb data. The goal is to provide insights to a client interested in investing in vacation rental properties. The analysis covers data exploration, data cleaning, filtering listings, identifying popular neighborhoods and property sizes, calculating occupancy rates, and estimating potential revenue for investment properties.

### The Data
The data was spread across two sheets:
- listings: each row corresponds to one property listing.
  - `'id'`: Airbnb's unique identifier for the listing.
  - `'listing_url'`
  - `'scrape_id'`: Inside Airbnb "Scrape" this was part of.
  - `'last_scraped'`: UTC. The date and time this listing was "scraped".
  - `'source'`: One of "neighbourhood search" or "previous scrape".
  - `'name'`: Name of the listing.
  - `'description'`: Detailed description of the listing.
  - `'neighborhood_overview'`: Host's description of the neighborhood.
  - `'picture_url'`: URL to the Airbnb hosted regular sized image for the listing.
  - `'host_id'`: Airbnb's unique identifier for the host/user.
  - `'host_url'`: The Airbnb page for the host.
  - `'host_name'`: Name of the host. Usually just the first name(s).
  - `'host_since'`: The dat the host/user was created.
  - `'host_location'`: The host's self reported location.
  - `'host_about'`: Description about the host.
  - `'host_response_time'`: 
  - `'host_response_rate'`
  - `'host_acceptance_rate'`: That rate at which a host accepts booking requests.
  - `'host_is_superhost'`
  - `'host_thumbnail_url'`: 
  - `'host_picture_url'`
  - `'host_neighborhood'`
  - `'host_listings_count'`: The number of listings the host has (per Airbnb calculations).
  - `'host_total_listings_count'`: The number of listings the host has (per Airbnb calculations).
  - `'host_verifications'`
  - `'host_has_profile_pic'`
  - `'host_identity_verified'`
  - `'neighborhood'`:The neighbourhood as geocoded using the latitude and longitude.
  - `'neighborhood_group'`: The neighbourhood as geocoded using the latitude and longitude.
  - `'latitude'`: Uses the World Geodetic System (WGS84) projection for latitude and longitude.
  - `'longitude'`: Uses the World Geodetic System (WGS84) projection for latitude and longitude.
  - `'property_type'`: Slef selected property type.
  - `'room_type'`: All homes are grouped into the following three room types:
  - `'accommodates'`: The maximum capacity of the listing.
  - `'bathrooms'`: The number of bathrooms in the listing.
  - `'bathrooms_text'`: The number of bathrooms in the listing.
  - `'bedrooms'`: The number of bedrooms.
  - `'beds'`: The number of bed(s).
  - `'amenities'`
  - `'price'`: Daily price in local currency.
  - `'minimum_nights'`: Minimum number of night stay for the listing (calendar rules may be different).
  - `'maximum_nights'`:  Maximum number of night stay for the listing (calendar rules may be different).
  - `'minimum_minimum_nights'`: The smallest minimum_night value from the calendar (looking 365 nights in the future).
  - `'maximum_minimum_nights'`: The largest minimum_night value from the calendar (looking 365 nights in the future).
  - `'minimum_maximum_nights'`: The smallest maximum_night value from the calendar (looking 365 nights in the future).
  - `'maximum_maximum_nights'`: The largest maximum_night value from the calendar (looking 365 nights in the future).
  - `'minimum_nights_avg_ntm'`: The average minimum_night value from the calendar (looking 365 nights in the future).
  - `'maximum_nights_avg_ntm'`: The average maximum_night value from the calendar (looking 365 nights in the future).
  - `'calendar_updated'`
  - `'calendar_last_scraped'`
  - `'number_of_reviews'`: The number of reviews the listing has.
  - `'number_of_reviews_ltm'`: The number of reviews the listing has (in the last 12 months).
  - `'number_of_reviews_130d'`: The number of reviews the listing has (in the last 30 days).
  - `'first_review'`: The date of the first/oldest review.
  - `'last_review'`: The date of the last/newest review.
  - `'review_scores_rating'`
  - `'review_scores_accuracy'`
  - `'review_scores_cleanliness'`
  - `'review_scores_checkin'`
  - `'review_scores_communication'`
  - `'review_scores_communication'`
  - `'review_scores_location'`
  - `'review_scores_value'`
  - `'license'`: The licence/permit/registration number.
  - `'instant_bookable'`: Whether the guest can automatically book the listing without the host requiring to accept their booking request.
  - `'calculated_host_listings_count'`: The number of listings the host has in the current scrape, in the city/region.
  - `'calculated_host_listings_count_entire_homes'`: The number of Entire home/apt listings the host has in the current scrape.
  - `'calculated_host_listings_count_private_rooms'`: The number of Private room listings the host has inthe current scrape.
  - `'calculated_host_listings_count_shared_rooms'`: The number of Shared room listings the host has in the current scrape.
  - `'reviews_per_month'`: The number of reviews the listing has over the lifetime of the listing.

- calendar: The calendar file records the price, availability and other details from the listing's calendar for each of the next 365 days.
  - `'listing_id'`
  - `'date'`: The date in the listing's calendar.
  - `'available'`: Whether the date is available for a booking.
  - `'price'`: The price listed for the day.
  - `'adjusted_price'`
  - `'minimum_nights'`: Minimum nights for a booking made on this day.
  - `'maximum_nights'`: Maximum nights for a booking made on this day.

TripleTen provided the NYC Airbnb data set.

### The Process
#### Part 1: Data Exploration and Cleaning
The initial phase involved downloading the NYC Airbnb dataset and examining its various sheets. Key columns were identified for analysis, and potential data cleaning challenges were noted. The data cleaning process included:
- Freezing rows and columns for easier navigation.
- Resizing columns and wrapping text.
- Adding filters to the dataset.
- Creating documentation tabs to keep a history of data cleaning steps.

#### Part 2: Identifying Target Properties
To focus the analysis on relavant listings, the following steps were taken:
- Filtering out listings with a minimum night requirement greater than seven days, as the analysis focused on vacation rentals.
- Removing listings with no reviews in the last 12 months, considering them inactive.
- Cleaning neighborhood names to ensure consistency in text format.

A pivot table was created to identify the top 10 neighborhoods based on the number of reviews in the last 12 months. Another pivot table was used to determine the most popular property sizes (number of bedrooms) in these neighborhoods. This analysis helped prioritize specific neighborhoods and property sizes for the client.

#### Part 3: Calculating Occupancy Rates
The calendar sheet provided data on listing's availability for 30 days. To calculate occupancy rates: 
- The `'available'` column was converted into a numeric occupied column (1 for occupied, 0 for available).
- A `'day_of_week'` column was added using the WEEKDAY() function to analyze occupancy trends by day.
- A pivot table was created to calculate the average occupancy rate for each listing, which was used to determine the occupancy percentage.

Additional analysis included creating a pivot table to show average occupancy rates by day of the week, providing insights into the most popular days for rentals. 

#### Part 4: Estimating Revenue
To estimate annual revenue for investment properties:
- Properties were filtered to include only those representative of potential investments (e.g., actively rented properties, high review ratings, excluding super luxury or extremely low-priced listings).
- A VLOOKUP() formula added the average occupancy rate to the listings sheet.
- A pivot table calculated the average price and occupancy rate for the recommended neighborhood and property size.
- Annual revenue was estimated using the formula: `Annual Revenue = 365 days * Average Price * Occupancy Rate`.

#### Part 5: Analyzing Key Attributes:
For top neighborhoods, additional insights were provided on attributes impacting property performance:
- The impace of superhosts on pricing.
- The effect of instant booking on occupancy rates.
- The correlation between doorman presence and review scores.
- The relationship between review ratings and pricing.

#### Part 6: Documentation and Formatting
The final stage involved organizing and formatting the spreadsheet to ensure it was polished and professional:
- An Executive Summary sheet with an overview of recommendations and a Table of Contents.
- Detailed documentation of data cleaning steps and assumptions made during the analysis.
- Consistent formatting, including borders, cell background colors, font styles, and sizes, to enhance readability.
- Hiding unnecessary columns to streamline the spreadsheet.

## Results
This comprehensive analysis provides the client with actionable insights into the Manhattan vacation rental market, helping them make informed investment decisions. 
Below are the pivot tables demonstrating that 2-bedroom apartments in Hell's Kitchen, Manhattan, offer the best investment returns based on the Airbnb data.

Please have a look at the spreadsheet included for a full description of the results. https://docs.google.com/spreadsheets/d/1J72s5ViuHjbGtrWPspd9Rjd_j7Zruu4IKgzTSZTstew/edit?usp=sharing

![Top Ten Most Popular Neighborhoods for Vacation Rentals](https://github.com/user-attachments/assets/d17a4520-45e9-423f-971d-fded285df788)

![Instant Booking](https://github.com/user-attachments/assets/457423f1-a86a-47f5-9d0a-4362f6005c49)

![Histogram of Cost of Rental](https://github.com/user-attachments/assets/01426439-96ed-40f4-a414-912d0862e50d)

![Day of the Week Percentage Occupied](https://github.com/user-attachments/assets/92fbb0e9-6e1c-4d6c-9b96-a430037a4592)

![Bedrooms and Number of Reviews](https://github.com/user-attachments/assets/022f694a-33cd-4d16-b29f-b8bb8d60cf16)

![Average Price Comparison Superhost](https://github.com/user-attachments/assets/6aa5d59f-6689-47e1-91eb-761c7a4071f2)

![Average Price Comparison Building Staff](https://github.com/user-attachments/assets/249da703-7d69-44e9-b034-fbb7f11751e3)

![Average Cost based on Reviews](https://github.com/user-attachments/assets/60f3f30a-1e8b-4f03-996d-1af173d9bfbe)

![Average Cost and Occupancy Rate](https://github.com/user-attachments/assets/5e486565-bdf5-46cb-b953-804775ea2a21)

![Highest Average Annual Revenue Estimate](https://github.com/user-attachments/assets/40839f58-678d-47cc-877b-37587ee0f836)
