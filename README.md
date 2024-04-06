# AirBnB MongoDB Analysis

A little assignment to practice importing and analyzing data within a MongoDB database.

Replace the contents of this file with a report, as described in the [instructions](./instructions.md).

<h1>
(Use this Assignment as 1 of my 2 late assignment extensions)
</h1>

## The origin of your data set - what is it and where does it come from. Include a link to the URL of the source.

## What format the original data file was in (CSV, JSON, or other).

Display some of the raw data from the original data file (the first 20 rows is enough - feel free to clip the text in fields to prevent line-wrapping). Use Markdown's ability to display tables - see the examples in the Markdown guide linked above.
Describe any problems that were present in the data and the scrubbing tasks that were necessary to prepare your data set for import - include any scrubbing done in Python, a text editor, or any other tool. Be specific with examples of the problems in the original data and the way in which those were solved. Feel free to show small snippets of relevant code - see the examples of code "syntax highlighting" in the Markdown guide linked above.

## show exactly two documents from the listings collection in any order

returns the first two documents from the listings collection as they are stored in the database

## Code

```

db.listings.find().limit(2)

```

## Query Results

### Document 1

```json
{
  "_id": "ObjectId('660ebf08b6515eb2057e4dd7')",
  "id": 9060873,
  "listing_url": "https://www.airbnb.com/rooms/9060873",
  "scrape_id": "NumberLong('20231212015436')",
  "last_scraped": "2023-12-12",
  "source": "city scrape",
  "name": "Condo in Amsterdam · ★4.60 · 1 bedroom · 1 bed · 1 bath",
  "description": "",
  "neighborhood_overview": "",
  "picture_url": "https://a0.muscache.com/pictures/miso/Hosting-9060873/original/35fa0e6c-397b-4145-9027-53e0d7c439bf.jpeg",
  "host_id": 47265643,
  "host_url": "https://www.airbnb.com/users/show/47265643",
  "host_name": "Magali",
  "host_since": "2015-10-23",
  "host_location": "Amsterdam, Netherlands",
  "host_about": "",
  "host_response_time": "N/A",
  "host_response_rate": "N/A",
  "host_acceptance_rate": "86%",
  "host_is_superhost": "f",
  "host_thumbnail_url": "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_small",
  "host_picture_url": "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_x_medium",
  "host_neighbourhood": "",
  "host_listings_count": 1,
  "host_total_listings_count": 1,
  "host_verifications": "['email', 'phone']",
  "host_has_profile_pic": "t",
  "host_identity_verified": "t",
  "neighbourhood": "",
  "neighbourhood_cleansed": "Oud-Oost",
  "neighbourhood_group_cleansed": "",
  "latitude": 52.3565573,
  "longitude": 4.9175314,
  "property_type": "Entire condo",
  "room_type": "Entire home/apt",
  "accommodates": 2,
  "bathrooms": "",
  "bathrooms_text": "1 bath",
  "bedrooms": "",
  "beds": 1,
  "amenities": "[]",
  "price": "$232.00",
  "minimum_nights": 2,
  "maximum_nights": 365,
  "minimum_minimum_nights": 2,
  "maximum_minimum_nights": 3,
  "minimum_maximum_nights": 365,
  "maximum_maximum_nights": 365,
  "minimum_nights_avg_ntm": 2.4,
  "maximum_nights_avg_ntm": 365,
  "calendar_updated": "",
  "has_availability": "t",
  "availability_30": 4,
  "availability_60": 4,
  "availability_90": 5,
  "availability_365": 23,
  "calendar_last_scraped": "2023-12-12",
  "number_of_reviews": 5,
  "number_of_reviews_ltm": 3,
  "number_of_reviews_l30d": 0,
  "first_review": "2022-11-13",
  "last_review": "2023-09-15",
  "review_scores_rating": 4.6,
  "review_scores_accuracy": 4.6,
  "review_scores_cleanliness": 4.4,
  "review_scores_checkin": 4.4,
  "review_scores_communication": 4.6,
  "review_scores_location": 4.6,
  "review_scores_value": 4.4,
  "license": "0363 AD77 7A50 99E1 5492",
  "instant_bookable": "f",
  "calculated_host_listings_count": 1,
  "calculated_host_listings_count_entire_homes": 1,
  "calculated_host_listings_count_private_rooms": 0,
  "calculated_host_listings_count_shared_rooms": 0,
  "reviews_per_month": 0.38
}
```
