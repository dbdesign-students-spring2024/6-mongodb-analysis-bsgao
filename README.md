# AirBnB MongoDB Analysis

A little assignment to practice importing and analyzing data within a MongoDB database.

Replace the contents of this file with a report, as described in the [instructions](./instructions.md).

<h1>
(Use this Assignment as 1 of my 2 late assignment extensions)
</h1>

## The origin of your data set - what is it and where does it come from. Include a link to the URL of the source.

The Origin of my dataset is the Amsterdam Airb&b dataset provided by the professor
Link: [Dataset](data/listings.csv)
Source: [Source](https://insideairbnb.com/amsterdam)

## What format the original data file was in (CSV, JSON, or other).

Display some of the raw data from the original data file (the first 20 rows is enough - feel free to clip the text in fields to prevent line-wrapping). Use Markdown's ability to display tables - see the examples in the Markdown guide linked above.
Describe any problems that were present in the data and the scrubbing tasks that were necessary to prepare your data set for import - include any scrubbing done in Python, a text editor, or any other tool. Be specific with examples of the problems in the original data and the way in which those were solved. Feel free to show small snippets of relevant code - see the examples of code "syntax highlighting" in the Markdown guide linked above.

## 1. Show exactly two documents from the listings collection in any order

returns the first two documents from the listings collection as they are stored in the database

## Code

```

db.listings.find().limit(2)

```

## Query Results(First three documents)

```
{ "_id" : ObjectId("660ebf08b6515eb2057e4dd7"), "id" : 9060873, "listing_url" : "https://www.airbnb.com/rooms/9060873", "scrape_id" : NumberLong("20231212015436"), "last_scraped" : "2023-12-12", "source" : "city scrape", "name" : "Condo in Amsterdam · ★4.60 · 1 bedroom · 1 bed · 1 bath", "description" : "", "neighborhood_overview" : "", "picture_url" : "https://a0.muscache.com/pictures/miso/Hosting-9060873/original/35fa0e6c-397b-4145-9027-53e0d7c439bf.jpeg", "host_id" : 47265643, "host_url" : "https://www.airbnb.com/users/show/47265643", "host_name" : "Magali", "host_since" : "2015-10-23", "host_location" : "Amsterdam, Netherlands", "host_about" : "", "host_response_time" : "N/A", "host_response_rate" : "N/A", "host_acceptance_rate" : "86%", "host_is_superhost" : "f", "host_thumbnail_url" : "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_small", "host_picture_url" : "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_x_medium", "host_neighbourhood" : "", "host_listings_count" : 1, "host_total_listings_count" : 1, "host_verifications" : "['email', 'phone']", "host_has_profile_pic" : "t", "host_identity_verified" : "t", "neighbourhood" : "", "neighbourhood_cleansed" : "Oud-Oost", "neighbourhood_group_cleansed" : "", "latitude" : 52.3565573, "longitude" : 4.9175314, "property_type" : "Entire condo", "room_type" : "Entire home/apt", "accommodates" : 2, "bathrooms" : "", "bathrooms_text" : "1 bath", "bedrooms" : "", "beds" : 1, "amenities" : "[]", "price" : "$232.00", "minimum_nights" : 2, "maximum_nights" : 365, "minimum_minimum_nights" : 2, "maximum_minimum_nights" : 3, "minimum_maximum_nights" : 365, "maximum_maximum_nights" : 365, "minimum_nights_avg_ntm" : 2.4, "maximum_nights_avg_ntm" : 365, "calendar_updated" : "", "has_availability" : "t", "availability_30" : 4, "availability_60" : 4, "availability_90" : 5, "availability_365" : 23, "calendar_last_scraped" : "2023-12-12", "number_of_reviews" : 5, "number_of_reviews_ltm" : 3, "number_of_reviews_l30d" : 0, "first_review" : "2022-11-13", "last_review" : "2023-09-15", "review_scores_rating" : 4.6, "review_scores_accuracy" : 4.6, "review_scores_cleanliness" : 4.4, "review_scores_checkin" : 4.4, "review_scores_communication" : 4.6, "review_scores_location" : 4.6, "review_scores_value" : 4.4, "license" : "0363 AD77 7A50 99E1 5492", "instant_bookable" : "f", "calculated_host_listings_count" : 1, "calculated_host_listings_count_entire_homes" : 1, "calculated_host_listings_count_private_rooms" : 0, "calculated_host_listings_count_shared_rooms" : 0, "reviews_per_month" : 0.38 }
{ "_id" : ObjectId("660ebf08b6515eb2057e4dd8"), "id" : 1427610, "listing_url" : "https://www.airbnb.com/rooms/1427610", "scrape_id" : NumberLong("20231212015436"), "last_scraped" : "2023-12-12", "source" : "previous scrape", "name" : "Home in Amsterdam · ★5.0 · 2 bedrooms · 2 beds · 2 baths", "description" : "", "neighborhood_overview" : "", "picture_url" : "https://a0.muscache.com/pictures/8d855b40-ba50-4c06-bb97-a0b84dd6e694.jpg", "host_id" : 7677579, "host_url" : "https://www.airbnb.com/users/show/7677579", "host_name" : "Aukje", "host_since" : "2013-07-23", "host_location" : "Amsterdam, Netherlands", "host_about" : "Hi! I am Aukje. I live with my husband and two kids in Amsterdam.", "host_response_time" : "N/A", "host_response_rate" : "N/A", "host_acceptance_rate" : "50%", "host_is_superhost" : "f", "host_thumbnail_url" : "https://a0.muscache.com/im/pictures/user/c9ab4610-5b55-45bb-9b2c-44d31f056523.jpg?aki_policy=profile_small", "host_picture_url" : "https://a0.muscache.com/im/pictures/user/c9ab4610-5b55-45bb-9b2c-44d31f056523.jpg?aki_policy=profile_x_medium", "host_neighbourhood" : "", "host_listings_count" : 1, "host_total_listings_count" : 1, "host_verifications" : "['email', 'phone']", "host_has_profile_pic" : "t", "host_identity_verified" : "t", "neighbourhood" : "", "neighbourhood_cleansed" : "Geuzenveld - Slotermeer", "neighbourhood_group_cleansed" : "", "latitude" : 52.38277, "longitude" : 4.80351, "property_type" : "Entire home", "room_type" : "Entire home/apt", "accommodates" : 4, "bathrooms" : "", "bathrooms_text" : "2 baths", "bedrooms" : "", "beds" : 2, "amenities" : "[]", "price" : "$120.00", "minimum_nights" : 5, "maximum_nights" : 1125, "minimum_minimum_nights" : 5, "maximum_minimum_nights" : 5, "minimum_maximum_nights" : 1125, "maximum_maximum_nights" : 1125, "minimum_nights_avg_ntm" : 5, "maximum_nights_avg_ntm" : 1125, "calendar_updated" : "", "has_availability" : "f", "availability_30" : 0, "availability_60" : 0, "availability_90" : 0, "availability_365" : 0, "calendar_last_scraped" : "2023-12-12", "number_of_reviews" : 6, "number_of_reviews_ltm" : 1, "number_of_reviews_l30d" : 0, "first_review" : "2020-07-30", "last_review" : "2023-08-06", "review_scores_rating" : 5, "review_scores_accuracy" : 4.67, "review_scores_cleanliness" : 4.83, "review_scores_checkin" : 4.83, "review_scores_communication" : 5, "review_scores_location" : 4.67, "review_scores_value" : 4.83, "license" : "0363 316D 14AF 5201 F18F", "instant_bookable" : "f", "calculated_host_listings_count" : 1, "calculated_host_listings_count_entire_homes" : 1, "calculated_host_listings_count_private_rooms" : 0, "calculated_host_listings_count_shared_rooms" : 0, "reviews_per_month" : 0.15 }
```

## 2. Show Exactly 10 Documents in Any Order, Pretty Print

### Code

```
db.listings.find().limit(10).pretty()

```

This query retrieves ten documents from the listings collection and formats the output for easier reading.

### Result

```json
{
	"_id" : ObjectId("660ebf08b6515eb2057e4dd7"),
	"id" : 9060873,
	"listing_url" : "https://www.airbnb.com/rooms/9060873",
	"scrape_id" : NumberLong("20231212015436"),
	"last_scraped" : "2023-12-12",
	"source" : "city scrape",
	"name" : "Condo in Amsterdam · ★4.60 · 1 bedroom · 1 bed · 1 bath",
	"description" : "",
	"neighborhood_overview" : "",
	"picture_url" : "https://a0.muscache.com/pictures/miso/Hosting-9060873/original/35fa0e6c-397b-4145-9027-53e0d7c439bf.jpeg",
	"host_id" : 47265643,
	"host_url" : "https://www.airbnb.com/users/show/47265643",
	"host_name" : "Magali",
	"host_since" : "2015-10-23",
	"host_location" : "Amsterdam, Netherlands",
	"host_about" : "",
	"host_response_time" : "N/A",
	"host_response_rate" : "N/A",
	"host_acceptance_rate" : "86%",
	"host_is_superhost" : "f",
	"host_thumbnail_url" : "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_small",
	"host_picture_url" : "https://a0.muscache.com/im/pictures/user/1596053e-34e6-429a-9f6b-cfc8b1b8bac1.jpg?aki_policy=profile_x_medium",
	"host_neighbourhood" : "",
	"host_listings_count" : 1,
	"host_total_listings_count" : 1,
	"host_verifications" : "['email', 'phone']",
	"host_has_profile_pic" : "t",
	"host_identity_verified" : "t",
	"neighbourhood" : "",
	"neighbourhood_cleansed" : "Oud-Oost",
	"neighbourhood_group_cleansed" : "",
	"latitude" : 52.3565573,
	"longitude" : 4.9175314,
	"property_type" : "Entire condo",
	"room_type" : "Entire home/apt",
	"accommodates" : 2,
	"bathrooms" : "",
	"bathrooms_text" : "1 bath",
	"bedrooms" : "",
	"beds" : 1,
	"amenities" : "[]",
	"price" : "$232.00",
	"minimum_nights" : 2,
	"maximum_nights" : 365,
	"minimum_minimum_nights" : 2,
	"maximum_minimum_nights" : 3,
	"minimum_maximum_nights" : 365,
	"maximum_maximum_nights" : 365,
	"minimum_nights_avg_ntm" : 2.4,
	"maximum_nights_avg_ntm" : 365,
	"calendar_updated" : "",
	"has_availability" : "t",
	"availability_30" : 4,
	"availability_60" : 4,
	"availability_90" : 5,
	"availability_365" : 23,
	"calendar_last_scraped" : "2023-12-12",
	"number_of_reviews" : 5,
	"number_of_reviews_ltm" : 3,
	"number_of_reviews_l30d" : 0,
	"first_review" : "2022-11-13",
	"last_review" : "2023-09-15",
	"review_scores_rating" : 4.6,
	"review_scores_accuracy" : 4.6,
	"review_scores_cleanliness" : 4.4,
	"review_scores_checkin" : 4.4,
	"review_scores_communication" : 4.6,
	"review_scores_location" : 4.6,
	"review_scores_value" : 4.4,
	"license" : "0363 AD77 7A50 99E1 5492",
	"instant_bookable" : "f",
	"calculated_host_listings_count" : 1,
	"calculated_host_listings_count_entire_homes" : 1,
	"calculated_host_listings_count_private_rooms" : 0,
	"calculated_host_listings_count_shared_rooms" : 0,
	"reviews_per_month" : 0.38
}
{
	"_id" : ObjectId("660ebf08b6515eb2057e4dd8"),
	"id" : 1427610,
	"listing_url" : "https://www.airbnb.com/rooms/1427610",
	"scrape_id" : NumberLong("20231212015436"),
	"last_scraped" : "2023-12-12",
	"source" : "previous scrape",
	"name" : "Home in Amsterdam · ★5.0 · 2 bedrooms · 2 beds · 2 baths",
	"description" : "",
	"neighborhood_overview" : "",
	"picture_url" : "https://a0.muscache.com/pictures/8d855b40-ba50-4c06-bb97-a0b84dd6e694.jpg",
	"host_id" : 7677579,
	"host_url" : "https://www.airbnb.com/users/show/7677579",
	"host_name" : "Aukje",
	"host_since" : "2013-07-23",
	"host_location" : "Amsterdam, Netherlands",
	"host_about" : "Hi! I am Aukje. I live with my husband and two kids in Amsterdam.",
	"host_response_time" : "N/A",
	"host_response_rate" : "N/A",
	"host_acceptance_rate" : "50%",
	"host_is_superhost" : "f",
	"host_thumbnail_url" : "https://a0.muscache.com/im/pictures/user/c9ab4610-5b55-45bb-9b2c-44d31f056523.jpg?aki_policy=profile_small",
	"host_picture_url" : "https://a0.muscache.com/im/pictures/user/c9ab4610-5b55-45bb-9b2c-44d31f056523.jpg?aki_policy=profile_x_medium",
	"host_neighbourhood" : "",
	"host_listings_count" : 1,
	"host_total_listings_count" : 1,
	"host_verifications" : "['email', 'phone']",
	"host_has_profile_pic" : "t",
	"host_identity_verified" : "t",
	"neighbourhood" : "",
	"neighbourhood_cleansed" : "Geuzenveld - Slotermeer",
	"neighbourhood_group_cleansed" : "",
	"latitude" : 52.38277,
	"longitude" : 4.80351,
	"property_type" : "Entire home",
	"room_type" : "Entire home/apt",
	"accommodates" : 4,
	"bathrooms" : "",
	"bathrooms_text" : "2 baths",
	"bedrooms" : "",
	"beds" : 2,
	"amenities" : "[]",
	"price" : "$120.00",
	"minimum_nights" : 5,
	"maximum_nights" : 1125,
	"minimum_minimum_nights" : 5,
	"maximum_minimum_nights" : 5,
	"minimum_maximum_nights" : 1125,
	"maximum_maximum_nights" : 1125,
	"minimum_nights_avg_ntm" : 5,
	"maximum_nights_avg_ntm" : 1125,
	"calendar_updated" : "",
	"has_availability" : "f",
	"availability_30" : 0,
	"availability_60" : 0,
	"availability_90" : 0,
	"availability_365" : 0,
	"calendar_last_scraped" : "2023-12-12",
	"number_of_reviews" : 6,
	"number_of_reviews_ltm" : 1,
	"number_of_reviews_l30d" : 0,
	"first_review" : "2020-07-30",
	"last_review" : "2023-08-06",
	"review_scores_rating" : 5,
	"review_scores_accuracy" : 4.67,
	"review_scores_cleanliness" : 4.83,
	"review_scores_checkin" : 4.83,
	"review_scores_communication" : 5,
	"review_scores_location" : 4.67,
	"review_scores_value" : 4.83,
	"license" : "0363 316D 14AF 5201 F18F",
	"instant_bookable" : "f",
	"calculated_host_listings_count" : 1,
	"calculated_host_listings_count_entire_homes" : 1,
	"calculated_host_listings_count_private_rooms" : 0,
	"calculated_host_listings_count_shared_rooms" : 0,
	"reviews_per_month" : 0.15
}
{
	"_id" : ObjectId("660ebf08b6515eb2057e4dd9"),
	"id" : 4829273,
	"listing_url" : "https://www.airbnb.com/rooms/4829273",
	"scrape_id" : NumberLong("20231212015436"),
	"last_scraped" : "2023-12-12",
	"source" : "city scrape",
	"name" : "Rental unit in Amsterdam · ★4.71 · 1 bedroom · 2 beds · 1 bath",
	"description" : "",
	"neighborhood_overview" : "",
	"picture_url" : "https://a0.muscache.com/pictures/104943349/73c49134_original.jpg",
	"host_id" : 15049236,
	"host_url" : "https://www.airbnb.com/users/show/15049236",
	"host_name" : "Franz",
	"host_since" : "2014-05-03",
	"host_location" : "Amsterdam, Netherlands",
	"host_about" : "I've been told to be a friendly and social person. I have  some piano playing abilities.",
	"host_response_time" : "within a few hours",
	"host_response_rate" : "100%",
	"host_acceptance_rate" : "83%",
	"host_is_superhost" : "f",
	"host_thumbnail_url" : "https://a0.muscache.com/im/pictures/user/ea5b2996-efab-42ae-9590-4d9a043ff969.jpg?aki_policy=profile_small",
	"host_picture_url" : "https://a0.muscache.com/im/pictures/user/ea5b2996-efab-42ae-9590-4d9a043ff969.jpg?aki_policy=profile_x_medium",
	"host_neighbourhood" : "Indische Buurt",
	"host_listings_count" : 1,
	"host_total_listings_count" : 2,
	"host_verifications" : "['email', 'phone', 'work_email']",
	"host_has_profile_pic" : "t",
	"host_identity_verified" : "t",
	"neighbourhood" : "",
	"neighbourhood_cleansed" : "Oostelijk Havengebied - Indische Buurt",
	"neighbourhood_group_cleansed" : "",
	"latitude" : 52.36379,
	"longitude" : 4.93354,
	"property_type" : "Entire rental unit",
	"room_type" : "Entire home/apt",
	"accommodates" : 4,
	"bathrooms" : "",
	"bathrooms_text" : "1 bath",
	"bedrooms" : "",
	"beds" : 2,
	"amenities" : "[]",
	"price" : "$170.00",
	"minimum_nights" : 2,
	"maximum_nights" : 14,
	"minimum_minimum_nights" : 2,
	"maximum_minimum_nights" : 3,
	"minimum_maximum_nights" : 14,
	"maximum_maximum_nights" : 14,
	"minimum_nights_avg_ntm" : 2,
	"maximum_nights_avg_ntm" : 14,
	"calendar_updated" : "",
	"has_availability" : "t",
	"availability_30" : 19,
	"availability_60" : 49,
	"availability_90" : 79,
	"availability_365" : 79,
	"calendar_last_scraped" : "2023-12-12",
	"number_of_reviews" : 51,
	"number_of_reviews_ltm" : 2,
	"number_of_reviews_l30d" : 0,
	"first_review" : "2015-09-21",
	"last_review" : "2023-08-06",
	"review_scores_rating" : 4.71,
	"review_scores_accuracy" : 4.8,
	"review_scores_cleanliness" : 4.65,
	"review_scores_checkin" : 4.87,
	"review_scores_communication" : 4.96,
	"review_scores_location" : 4.57,
	"review_scores_value" : 4.57,
	"license" : "0363 8D14 B764 39D3 8776",
	"instant_bookable" : "f",
	"calculated_host_listings_count" : 1,
	"calculated_host_listings_count_entire_homes" : 1,
	"calculated_host_listings_count_private_rooms" : 0,
	"calculated_host_listings_count_shared_rooms" : 0,
	"reviews_per_month" : 0.51
}

```

## 3.Choose two hosts (by reffering to their host_id values) who are superhosts (available in the host_is_superhost field), and show all of the listings offered by both of the two hosts

Chosen host_id: 11808004, 32116304

### Code

```
db.listings.find({
  "host_id": { $in: [11808004, 32116304] },
  "host_is_superhost": "t"
}, {
  "name": 1,
  "price": 1,
  "neighbourhood": 1,
  "host_name": 1,
  "host_is_superhost": 1
})
```

This query filters listings where the host ID is either 11808004 or 32116304, and show the show the name, price, neighbourhood, host_name, and host_is_superhost for each result.

### Result

```
{ "_id" : ObjectId("660ebf08b6515eb2057e4de3"), "name" : "Rental unit in Amsterdam · ★4.94 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$250.00" }
{ "_id" : ObjectId("660ebf08b6515eb2057e4ded"), "name" : "Condo in Amsterdam · ★5.0 · 1 bedroom · 2 beds · 1.5 baths", "host_name" : "Eva", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$260.00" }
{ "_id" : ObjectId("660ebf09b6515eb2057e5e1d"), "name" : "Rental unit in Amsterdam · ★4.82 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$105.00" }
{ "_id" : ObjectId("660ec6aeb6515eb2057e982d"), "name" : "Rental unit in Amsterdam · ★4.94 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$250.00" }
{ "_id" : ObjectId("660ec6aeb6515eb2057e9837"), "name" : "Condo in Amsterdam · ★5.0 · 1 bedroom · 2 beds · 1.5 baths", "host_name" : "Eva", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$260.00" }
{ "_id" : ObjectId("660ec6afb6515eb2057ea867"), "name" : "Rental unit in Amsterdam · ★4.82 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$105.00" }
{ "_id" : ObjectId("660eca1db6515eb2057ebacc"), "name" : "Rental unit in Amsterdam · ★4.94 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$250.00" }
{ "_id" : ObjectId("660eca1db6515eb2057ebad6"), "name" : "Condo in Amsterdam · ★5.0 · 1 bedroom · 2 beds · 1.5 baths", "host_name" : "Eva", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$260.00" }
{ "_id" : ObjectId("660eca1db6515eb2057ecb06"), "name" : "Rental unit in Amsterdam · ★4.82 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$105.00" }
{ "_id" : ObjectId("6611ab1dc34b7fbd6a5a75ba"), "name" : "Rental unit in Amsterdam · ★4.94 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$250.00" }
{ "_id" : ObjectId("6611ab1dc34b7fbd6a5a75c4"), "name" : "Condo in Amsterdam · ★5.0 · 1 bedroom · 2 beds · 1.5 baths", "host_name" : "Eva", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$260.00" }
{ "_id" : ObjectId("6611ab1dc34b7fbd6a5a85f4"), "name" : "Rental unit in Amsterdam · ★4.82 · 1 bedroom · 1 bed · 1 bath", "host_name" : "Henry", "host_is_superhost" : "t", "neighbourhood" : "Amsterdam, Noord-Holland, Netherlands", "price" : "$105.00" }
```

## 4. Find all the unique host_name values

### Code

```
db.listings.distinct("host_name")
```

This code finds all the unique host names in the collection of documents

### Result(Starting with A and B)

```[
	NaN,
	"23 SouS",
	"A",
	"A.C.",
	"Aad",
	"Aafje",
	"Aafke",
	"Aaliyah",
	"Aalje",
	"Aart",
	"Abbey",
	"Abdullah",
	"Abel",
	"Abigael",
	"Achayla",
	"Acostar Hotel",
	"Ad",
	"Ad & Anna",
	"Adam",
	"Addie",
	"Adelle",
	"Adem",
	"Adi",
	"Adinda",
	"Adriaan",
	"Adrian",
	"Adriana",
	"Adriano",
	"Adrienne",
	"Aemilia",
	"Aernout",
	"Agaath",
	"Agata",
	"Agathe",
	"Agnes",
	"Agnesa",
	"Agnieszka",
	"Agustina",
	"Ahmed",
	"Ahmet",
	"Aicha",
	"Aida",
	"Aike",
	"Aimee",
	"Aimée",
	"Aina",
	"Aisha",
	"Aisyah",
	"Ait",
	"Akhmad",
	"Akiva",
	"Akos",
	"Akshay",
	"Alan",
	"Alba",
	"Alban",
	"Albane",
	"Albert",
	"Albertine",
	"Albertjan",
	"Alberto",
	"Aldin",
	"Aldo",
	"Aleida",
	"Alejandro",
	"Alek",
	"Aleksandar",
	"Aleksandra",
	"Alena",
	"Alessandra",
	"Alessandro",
	"Alessia",
	"Alessio",
	"Aleta",
	"Aletta",
	"Alette",
	"Alex",
	"Alexander",
	"Alexander & Suzanne",
	"Alexandra",
	"Alexandre",
	"Alexandros",
	"Alexandru",
	"Alexine",
	"Alexis",
	"Alfred",
	"Ali",
	"Alice",
	"Alicia",
	"Alies",
	"Alim",
	"Alina",
	"Aline",
	"Aline Barbara",
	"Alison",
	"Alissa",
	"Alistair",
	"Alix",
	"Allard",
	"Almedio",
	"Alp",
	"Alphons",
	"Alvaro",
	"Alëna",
	"Amalia",
	"Aman",
	"Amanda",
	"Amandine",
	"Amar",
	"Amarah",
	"Amber",
	"Ambra",
	"Ambra & Tarik",
	"Amin",
	"Amina",
	"Amir",
	"Amit",
	"Amitesh",
	"Amjad",
	"Amor",
	"Amos",
	"Amsterdam",
	"Amsterdam Amstel BNB",
	"Amsterdam Boutique Apartments",
	"Amsterdam Canal Guest Apartment",
	"Amsterdam East By YAYS",
	"Amsterdam Lake Hotel",
	"Amsterdam Prince Island By YAYS",
	"Amsterdam The Crane By YAYS",
	"Amsterdamnoortje",
	"Amy",
	"Amélie & Warren",
	"An",
	"Ana",
	"Ana Maria",
	"Anabella",
	"Anais",
	"Anamaria & Leonard",
	"Anca",
	"Anca And Denis",
	"Andre",
	"Andrea",
	"Andrea & Felipe",
	"Andreas",
	"Andrei",
	"Andrew",
	"Andries",
	"Andrius",
	"André",
	"André & Inez",
	"Andy",
	"Ane",
	"Anestis",
	"Angel",
	"Angela",
	"Angelica",
	"Angelo",
	"Angie",
	"Angus",
	"Ania",
	"Aniek",
	"Anik",
	"Anil",
	"Anique",
	"Anissa",
	"Anita",
	"Anja",
	"Ank",
	"Anke",
	"Anke & Robert",
	"Anmarie",
	"Ann",
	"Anna",
	"Anna & Benjamin",
	"Anna And Robert",
	"Anna En John",
	"Anna Maria",
	"Anna Sofie",
	"Anna&Marnix",
	"Annabel",
	"Annabelle",
	"Annagreet",
	"Annah",
	"Annalies",
	"Anne",
	"Anne Boe",
	"Anne Lieke",
	"Anne Marijn",
	"Anne Rose",
	"Anne Wil",
	"Anne- Marijn",
	"Anne-Clémence",
	"Anne-Fleur",
	"Anne-Fleur Koning",
	"Anne-Jan",
	"Anne-Marie",
	"Anne-Sophie",
	"Annebelle",
	"Annebet",
	"Anneke",
	"Annelie",
	"Annelieke",
	"Annelien",
	"Annelies",
	"Anneloe",
	"Anneloes",
	"Annely",
	"Annemaartje",
	"Annemarie",
	"Annemarie & Patrick",
	"Annemiek",
	"Annemieke",
	"Annemien",
	"Annerieke",
	"Annerose",
	"Annet",
	"Annetje",
	"Annette",
	"Annick",
	"Anniek",
	"Annika",
	"Annique",
	"Anny",
	"Anoek En Thimo",
	"Anouc",
	"Anouk",
	"Anoushka",
	"Ansje & Walter",
	"Antheabronwasserat",
	"Anthi",
	"Anthony",
	"Antoine",
	"Antoinette",
	"Anton And Julia",
	"Antonin",
	"Antonio",
	"Antonius",
	"Antony",
	"António",
	"Anıl",
	"Ara",
	"Arash",
	"Arcangelo",
	"Archil",
	"Ard",
	"Arda",
	"Ardi",
	"Ardjan & Jose",
	"Areke",
	"Aren",
	"Ari",
	"Arie",
	"Arie Jan",
	"Ariel",
	"Arien",
	"Aris",
	"Arja",
	"Arjan",
	"Arjen",
	"Arko",
	"Arley",
	"Arnaud",
	"Arnd",
	"Arne",
	"Arno",
	"Arno En Maria",
	"Arnold",
	"Arnoud",
	"Aron",
	"Art",
	"Artem",
	"Arthur",
	"Artur",
	"Arturs",
	"Asaf",
	"Ash And Mitch",
	"Ashkaine",
	"Ashley",
	"Ashwanth",
	"Asisa",
	"Asli",
	"Aslınur",
	"Astrid",
	"Atal",
	"Atilla",
	"Augustus",
	"Aukeline",
	"Aukje",
	"Aurelie",
	"Aurélia",
	"Auste",
	"Aveline",
	"Axel",
	"Aydin",
	"Aydın",
	"Ayla & Jake",
	"Ayling",
	"Ayo",
	"Ayse",
	"Aysen",
	"Aysha",
	"Azza",
	"B",
	"B&B  Jordaan",
	"B&B Woestduin",
	"B.J.",
	"Babar",
	"Babet",
	"Babette",
	"Babs",
	"Bakoly",
	"Balazs",
	"Balthasar",
	"Bar",
	"Barak",
	"Barbara",
	"Barbara En Arjan",
	"Barend",
	"Barnaby & Annelie",
	"Barrie",
	"Barry",
	"Bart",
	"Bart & Carolyn",
	"Bart & Manon",
	"Bart & Rachel",
	"Bart-Jan",
	"Bartu",
	"Bas",
	"Bas & Saskia",
	"Bas En Barbara",
	"Bas En Fenne",
	"Bas-Jan",
	"Bastiaan",
	"Bastiaan E.",
	"Bastian",
	"Bauke",
	"Beatrijs",
	"Beatrix",
	"Beau",
	"Beauchamp",
	"Beca",
	"Behdad",
	"Belen",
	"Belinda En Paul",
	"Bella",
	"Belle",
	"Ben",
	"Ben And Amanda",
	"Ben And Fay",
	"Bence",
	"Benck",
	"Benjamin",
	"Benjo",
	"Bennie",
	"Benno",
	"Bente",
	"Benthe",
	"Beppie",
	"Berat",
	"Berber",
	"Berend",
	"Berendien",
	"Beril",
	"Berith",
	"Bernadette",
	"Bernadien",
	"Bernard",
	"Berry",
	"Bert",
	"Betty",
	"Bianca",
	"Bibi",
	"Bieneke",
	"Billy",
	"Bing",
	"Birgit",
	"Birgitte",
	"Birre",
	"Björn",
	"Bjørn",
	"Blair",
	"BnB Assistant",
	"BnB Beheer",
	"Bo",
	"Boas",
	"Boaz",
	"Bob",
	"Bob & Menno",
	"Bobbie",
	"Bobby",
	"Bodine",
	"Boen",
	"Bogdan",
	"Bogy",
	"Boland",
	"Bonnie",
	"Bonny",
	"Boogaard'S BnB",
	"Bop & Eve",
	"Bora",
	"Boris",
	"Bouke",
	"Boy",
	"Bradley",
	"Bradyn",
	"Bram",
	"Branka",
	"Branko",
	"Brechje",
	"Breck",
	"Bregje",
	"Brenda",
	"Brendan",
	"Brent En Esther",
	"Brian",
	"Brigit",
	"Brigitta",
	"Brigitte",
	"Brit",
	"Britt",
	"Britta",
	"Bronte",
	"Bruce",
	"Bruna",
	"Bruno",
	"Buket",
	"Bunk",
	"Burak",
	"Burcu",
	"Béla",
	"Bénine",
```

## 5.Find all of the places that have more than 2 beds in a neighborhood of your choice (referred to as either the neighborhood or neighbourhood_group_cleansed fields in the data file), ordered by review_scores_rating descending.

### Code

```
db.listings.find({
  $and: [
    { "neighbourhood_cleansed": "Oud-Oost" },
    { "beds": { $gt: 2 } },
    { "review_scores_rating": { $ne: null } }
  ]
}, {
  "name": 1,
  "beds": 1,
  "review_scores_rating": 1,
  "price": 1
}).sort({ "review_scores_rating": -1 })
```

The query retrieves listings from the "Oud-Oost" neighborhood with more than two beds and a non-null review score, returning only the name, number of beds, review score, and price of each listing. These results are sorted by review score in descending order to prioritize higher-rated listings.

### Result(Showing first few)

```
{ "_id" : ObjectId("660ebf08b6515eb2057e565d"), "name" : "Condo in Amsterdam · 3 bedrooms · 3 beds · 1 bath", "beds" : 3, "price" : "$320.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ebf09b6515eb2057e5d82"), "name" : "Home in Amsterdam · 3 bedrooms · 3 beds · 3 baths", "beds" : 3, "price" : "$300.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ebf09b6515eb2057e6540"), "name" : "Condo in Amsterdam · ★New · 2 bedrooms · 4 beds · 1.5 baths", "beds" : 4, "price" : "$170.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ebf09b6515eb2057e65ad"), "name" : "Home in Amsterdam · 3 bedrooms · 3 beds · 1.5 baths", "beds" : 3, "price" : "$295.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ec6aeb6515eb2057ea0aa"), "name" : "Condo in Amsterdam · 3 bedrooms · 3 beds · 1 bath", "beds" : 3, "price" : "$320.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ec6afb6515eb2057ea7cc"), "name" : "Home in Amsterdam · 3 bedrooms · 3 beds · 3 baths", "beds" : 3, "price" : "$300.00", "review_scores_rating" : "" }
{ "_id" : ObjectId("660ec6afb6515eb2057eaf89"), "name" : "Condo in Amsterdam · ★New · 2 bedrooms · 4 beds · 1.5 baths", "beds" : 4, "price" : "$170.00", "review_scores_rating" : "" }
```

## 6. Show the number of listings per host

### Code

```
db.listings.aggregate([
  { $group: { _id: "$host_id", host_total_listings_count: { $sum: 1 } } },
  { $project: { host_id: "$_id", host_total_listings_count: 1, _id: 0 } }
])
```

The query aggregates data from the listings collection, grouping entries by host_id and counting the total number of listings per host

### Result (selected Samples)

```
{ "host_total_listings_count" : 4, "host_id" : 16683382 }
{ "host_total_listings_count" : 4, "host_id" : 33755999 }
{ "host_total_listings_count" : 4, "host_id" : 4381603 }
{ "host_total_listings_count" : 5, "host_id" : 12167638 }
{ "host_total_listings_count" : 5, "host_id" : 3031239 }
{ "host_total_listings_count" : 5, "host_id" : 8580012 }
{ "host_total_listings_count" : 5, "host_id" : 53203726 }
{ "host_total_listings_count" : 5, "host_id" : 297593311 }
{ "host_total_listings_count" : 5, "host_id" : 308752067 }
{ "host_total_listings_count" : 5, "host_id" : 5219968 }
{ "host_total_listings_count" : 5, "host_id" : 9846631 }
{ "host_total_listings_count" : 10, "host_id" : 313772063 }
{ "host_total_listings_count" : 25, "host_id" : 51485781 }
{ "host_total_listings_count" : 4, "host_id" : 11335521 }
{ "host_total_listings_count" : 5, "host_id" : 498869432 }
{ "host_total_listings_count" : 5, "host_id" : 82297492 }
{ "host_total_listings_count" : 5, "host_id" : 27278204 }
{ "host_total_listings_count" : 5, "host_id" : 773375 }
{ "host_total_listings_count" : 4, "host_id" : 12781730 }
{ "host_total_listings_count" : 4, "host_id" : 56325407 }
```

## 7. find the average review_scores_rating per neighborhood, and only show those that are 4 or above, sorted in descending order of rating

### Code

```
db.listings.aggregate([
  { $match: { "review_scores_rating": { $gte: 4 } } },
  { $group: {
    _id: "$neighbourhood_cleansed",
    averageRating: { $avg: "$review_scores_rating" }
  }},
  { $sort: { averageRating: -1 } }
])
```

Calculating the average review scores rating per neighborhood, considering only those ratings 4 or above, and sorted in descending order.

### Result

```
{ "_id" : "IJburg - Zeeburgereiland", "averageRating" : 4.878344549125169 }
{ "_id" : "Watergraafsmeer", "averageRating" : 4.869106302916275 }
{ "_id" : "De Baarsjes - Oud-West", "averageRating" : 4.867757455923545 }
{ "_id" : "Oud-Oost", "averageRating" : 4.8664462809917355 }
{ "_id" : "De Pijp - Rivierenbuurt", "averageRating" : 4.8648870536798645 }
{ "_id" : "Slotervaart", "averageRating" : 4.863715469613259 }
{ "_id" : "Noord-Oost", "averageRating" : 4.863032490974729 }
{ "_id" : "Zuid", "averageRating" : 4.858803347280335 }
{ "_id" : "Bos en Lommer", "averageRating" : 4.8559075907590765 }
{ "_id" : "Westerpark", "averageRating" : 4.85061975209916 }
{ "_id" : "Oostelijk Havengebied - Indische Buurt", "averageRating" : 4.848792093704246 }
{ "_id" : "Noord-West", "averageRating" : 4.847317327766179 }
{ "_id" : "Buitenveldert - Zuidas", "averageRating" : 4.840906593406594 }
{ "_id" : "De Aker - Nieuw Sloten", "averageRating" : 4.839267399267399 }
{ "_id" : "Oud-Noord", "averageRating" : 4.836345800122624 }
{ "_id" : "Centrum-Oost", "averageRating" : 4.835154980439362 }
{ "_id" : "Bijlmer-Oost", "averageRating" : 4.819517241379311 }
{ "_id" : "Centrum-West", "averageRating" : 4.818657162566107 }
{ "_id" : "Geuzenveld - Slotermeer", "averageRating" : 4.788263736263736 }
{ "_id" : "Osdorp", "averageRating" : 4.782100000000001 }
```
