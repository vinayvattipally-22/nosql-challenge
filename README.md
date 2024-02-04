# README for "Eat Safe, Love" Analysis

## Part 1: Database and Jupyter Notebook Set Up

### Importing Data
The data provided in the establishments.json file was imported into a MongoDB database named uk_food with a collection called establishments. The import command used was:

`mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray`

### MongoDB Connection
The analysis was conducted using a Jupyter Notebook. The MongoDB database connection was established using the pymongo library in Python. The establishments collection within the uk_food database was used for further analysis.

## Part 2: Update the Database

### Adding a New Restaurant
An exciting new halal restaurant, "Penang Flavours," was added to the database. The restaurant details, including business name, address, local authority, and geographical coordinates, were included in the new entry.

### Finding BusinessTypeID
A query was executed to find the BusinessTypeID for the category "Restaurant/Cafe/Canteen." The results were displayed, showing the relevant information.

### Updating BusinessTypeID for Penang Flavours
The BusinessTypeID for "Penang Flavours" was updated with the correct value, ensuring data consistency in the collection.

### Removing Establishments in Dover
Establishments within the Dover Local Authority were identified and subsequently removed from the database to meet the analysis requirements.

### Updating Data Types
Data types for latitude, longitude, and RatingValue were corrected using the update_many operation to ensure accurate numerical representation.

## Analysis
The analysis involved querying the database to extract relevant information, such as establishments in London with a RatingValue greater than or equal to 4, the top 5 establishments with a RatingValue of 5 sorted by the lowest hygiene score near "Penang Flavours," and the count of establishments with a hygiene score of 0 in each Local Authority area.

Results were presented in both raw form and as Pandas DataFrames for clarity and ease of interpretation.

## Conclusion
The "Eat Safe, Love" analysis provided valuable insights into food establishment hygiene ratings in the UK. The database was updated with new data, and necessary corrections were made to enhance data integrity. The analysis results can inform decision-making processes related to food safety and restaurant choices.

* Note: The provided README focuses on the key actions taken during the analysis, and detailed code snippets have been omitted for simplicity.