# TripleTen Manhattan Airbnb Spreadsheets Project
This is the 1st project I worked on in the TripleTen Business Intelligence Analytics program. I really enjoyed learning the ins and outs of spreadsheets.

## Potential Investment Properties in Manhattan
The goal of the project was to clean the data and analyze the vacation rental market in the Manhattan borough of New York City, focusing on identifying the types of properties that should be targeted for investment. 

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
First, I explored the dataset's sheets, cleaned the data, and created an assumptions and change log. Finally, I analyzed the data using visualizations and pivot tables.

## Results
I presented my research findings using bar charts and pivot tables, identifying the Manhattan neighborhoods with the highest potential for profitable investments.

Please have a look at the spreadsheet included for a full description of the results.
