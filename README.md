# airbnb-review-analysis

For this project, we wanted to understand two key problems:

1. How do the features of an airbnb (bedrooms, bathrooms, amenities offered, etc.) affect the average user experience (as reflected by the rating the user leaves on an airbnb?
2. How does average price of a rental unit/home in a neighborhood relate to the average price of an airbnb in the same area?

To understand the first question, we had to combine a variety of airbnb datasets from different cities, using data from insideairbnb.com. Each dataset (stored by convention as the variable `{cityname}Airbnbdf` ) contains the number of bedrooms/bathrooms, amenities (stored as a string of varying amenities), airbnb review score, and other relevant features. Although there are certainly risks in combining together airbnb data from very different cities, we have done a lot to mitigate any unexpected variance in our data (e.g. by normalizing prices over each region, rather than using raw price values) - and that these risks are worth it for the sake of having a large enough dataset to test non-trivial models on.

To understand the second question, we limited ourselves to just looking at New York city, with two datasets: `NYAirbnbdf` which is a very large dataset with detailed information about airbnb listings in New York City, and `NYHousingdf` which contains information about prices of apartments/homes in New York City. By grouping by zipcode, we analyzed how the prices in airbnb listings and prices of apartment listings were related.

