# Movies-ETL

Create an ETL pipeline from raw data to a SQL database.
Extract data from disparate sources using Python.
Clean and transform data using Pandas.
Use regular expressions to parse data and to transform text into numbers.
Load data with PostgreSQL.
Britta is excited to prepare for the hackathon. In data analysis, a hackathon is an event where teams of analysts collaborate to work intensively on a project, using data to solve a problem. Hackathons generally last several days, and teams work around the clock on their projects.

Britta needs to gather data from both Wikipedia and Kaggle, combine them, and save them into a SQL database so that the hackathon participants have a nice, clean dataset to use. To do this, she will follow the ETL process: extract the Wikipedia and Kaggle data from their respective files, transform the datasets by cleaning them up and joining them together, and load the cleaned dataset into a SQL database.


Challenge

Background
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs your help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. You’ll need to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

Deliverable 1: Write an ETL Function to Read Three Data Files
Deliverable 1 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, write a function that reads in the three data files and creates three separate DataFrames.

Deliverable 1 Requirements
You will earn a perfect score for Deliverable 1 by completing all requirements below:

An ETL function is written to read in the three data files.
The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
​The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
​The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.

Deliverable 2: Extract and Transform the Wikipedia Data
Deliverable 2 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.

Deliverable 2 Requirements
You will earn a perfect score for Deliverable 2 by completing all requirements below:

The TV shows are filtered out, and the wiki_movies_df DataFrame is created.
A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
The extraction and transformation of the Wikipedia data in the ETL function does the following:
A list comprehension is used to keep columns with non-null values.
The non-null box office data is converted to string values using the lambda and join functions.
A regular expression is used to match the six elements of "form_one" of the box office data.
A regular expression is used to match the three elements of "form_two" of the box office data.
The following columns are cleaned in the Wikipedia DataFrame:
The box office column
The budget column
The release date column
The running time column
​The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.

Deliverable 3: Extract and Transform the Kaggle Data
Deliverable 3 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, you’ll merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, you’ll merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.

Deliverable 3 Requirements
You will earn a perfect score for Deliverable 3 by completing all requirements below:

The extraction and transformation of the Kaggle metadata using the ETL function does the following:
The Kaggle metadata is cleaned.
The Wikipedia and Kaggle DataFrames are merged.
The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df:
Unnecessary columns are dropped.
A function is used to fill in the missing Kaggle data.
The movies_df DataFrame is filtered to keep specific columns.
The movies_df DataFrame columns are renamed.
The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
The ratings counts are cleaned.
The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame.
The empty values in the movies_with_ratings_df DataFrame are filled with “0”.
The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file.


Deliverable 4: Create the Movie Database
Deliverable 4 Instructions
Use your knowledge of Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.

Deliverable 4 Requirements
You will earn a perfect score for Deliverable 4 by completing all requirements below:

The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png.
The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png.
The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file. 
