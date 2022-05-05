# **Movies-ETL**
Movies ETL (Extract Transform Load)

## **INDEX**

[Overview](#overview)

[Resources](#resources)

[Results](#results)

[Summary](#summary)


## **OVERVIEW**
Amazing Prime Video is looking to develop an algorithm to predict popular movies, and load the database into SQL table.

This analysis for this Project will be performed during the Hackathon. To proper combine the information, we will follow the ETL process, by **E**xtracting the Wikipedia and Kaggle data; **T**ransforming the datasets by cleaning them and joining them together and **L**oading the cleaned dataset into a SQL database.

[:top: Go To Top](#index)

## **RESOURCES**
Data obtained to perform the analysis:

- [Wikipedia Movies](https://github.com/amonjaras/Movies-ETL/blob/main/Resources/wikipedia_movies.json.zip)
- [Movies metadata](https://github.com/amonjaras/Movies-ETL/blob/main/Resources/movies_metadata.csv.zip)

[:top: Go To Top](#index)

## **RESULTS**
After the successful creation of the first dataset, Amazing Prime wants to keep it updated on a daily basis. To succeed with this project we divided the challenge into 4 activities:

- Deliverable 1: [ETL function test](https://github.com/amonjaras/Movies-ETL/blob/main/ETL_function_test.ipynb)
  - Data is extracted from Wikipedia in JSON format and converted into Pandas DataFrame.
  - Data is extracted from Kaggle Metadata and MovieLens CSV files into Pandas DataFrame.

- Deliverable 2: [ETL Clean wiki movies](https://github.com/amonjaras/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb)
  - The TV shows are filtered out from the Wikipedia data and transformed into a DataFrame.
  - A try-except block used to catch errors while extracting IMDB IDs with a regular expression.
  - A list comprehension is used to keep columns with non-null values.
  - The non-null box office data is converted to string values using the lambda and join functions.
  - Transformation of the Wikipedia data by cleaning the box office, budget, release date and running time columns.

- Deliverable 3: [ETL clean Kaggle data](https://github.com/amonjaras/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb)
  - Cleaned the Kaggle metadata.
  - The Wikipedia and Kaggle DataFrames were merged and cleaned.
  - Extracted and cleaned the MovieLens Ratings Data.
  - Finally merged the ratings data with the Wikipedia and Kaggle metadata.

- Deliverable 4: [ETL create database](https://github.com/amonjaras/Movies-ETL/blob/main/ETL_create_database.ipynb)
  - Uploaded the clean and merged data on PostgreSQL.
  - Existing data in Movies table replaced by current data in PostgreSQL.
    - [PostgreSQL movies query](https://github.com/amonjaras/Movies-ETL/blob/main/Resources/movies_query.png)
    - [PostgreSQL ratings query](https://github.com/amonjaras/Movies-ETL/blob/main/Resources/ratings_query.png)

[:top: Go To Top](#index)

## **SUMMARY**
ETL is an extensive process, that if not performed correctly, will create incorrect results.

It is recommendable to keep proper notation about changes or code executed

[:top: Go To Top](#index)




This work belongs to [^1].
Course [^2].
[^note]:
[^1]: Author: Audrey MONJARAS :mexico: :canada:
[^2]: Data Analytics: Unit 8 ETL :books:
