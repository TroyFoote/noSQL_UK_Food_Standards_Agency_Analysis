# Project Title: NoSQL-Challenge - UK-Food Analysis

## Project Description

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

### Part 1: 

### Requirements

*MongoDB*
*NoSQL_setup_starter.ipynb*
*establishments.json*
*PyMongo*
*Pretty Print*

### Database & Jupyter Notebook Set Up

1. Import data from the establishments.json file from your Terminal. Name the database *uk_food* and the collection *establishments*. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook. 
2. Import the requured libraries
3. Create an instance of Mongo Client
4. Confirm the database has been created and loaded correctly.
    Confirm *UK_food* database and *establishments* collection are listed in MongoDB
    Find and display one document from the *establishments* collection using *find_one* and display with *pprint*

### Part 2: 

### Requirements

*MongoDB*
*NoSQL_setup_starter.ipynb*
*establishments.json*
*PyMongo*
*Pretty Print*

### Update the Database
Use *NoSQL_setup_starter.ipynb*
Make the following changes to the *establishments* collection:

1. Add the following restaurant informtion into the database

        {
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}

2. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
3.  Update the new restaurant with the BusinessTypeID you found.
4.  check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
5.  Use update_many to convert latitude and longitude from string values to decimal numbers.

### Part 3: 

### Requirements

*MongoDB*
*NoSQL_analysis_starter.ipynb*
*establishments.json*
*PyMongo*
*Pretty Print*

### Exploratory Analysis

Use *NoSQL_analysis_starter.ipynb*

NOTES FOR THIS SECTION:

    Use count_documents to display the number of documents contained in the result.
    Display the first document in the results using pprint.
    Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a RatingValue greater than or equal to 4?
3. What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

HINTS
The London Local Authority has a longer name than "London" so you will need to use $regex as part of your search.
You will need to compare the geocode to find the nearest locations. Search within 0.01 degree on either side of the latitude and longitude.
You will need to use the aggregation method to answer this.


### References
UK Food Standards AgencyLinks to an external site. (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GBLinks to an external site.. Contains public sector information licensed under the Open Government Licence v3.0Links to an external site.
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).

