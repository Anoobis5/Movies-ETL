# Movies-ETL

## Project Overview

For this project, we were tasked with creating an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables while refactoring some code to take in Wikipedia data, Kaggle metadata, and MovieLens rating data. We will perform ETL processes (Extract, Transform, and Load) by adding the data to a PostgreSQL database. This will enable the participants of a hackathonn to draw from a clean and structured data to perform analyses with their algorithms. Our data plan breakdown to set up the data is as follows:

1. We wrote an ETL function to read the three data files (Wiki `data, Kaggle data, and MovieLens metadata)
2. Extract and Transform our Data for clean upload.
4. Load our transformed data into a PostgreSQL Movie-Data database

## Project Summary

First we needed to the Wikipedia JSON file, the Kaggle metadata, and the MovieLens ratings data files to a Pandas DataFrame and display it in our ETL_function_test.ipynb file. 

![Deliverable_1_code_block](https://user-images.githubusercontent.com/84881187/127754425-412329c2-4bd7-4b4b-82bb-472a3b4634a8.PNG)

Using this file, we are able to refactor our code so that we can transform the Wikipedia data so that we can merge it with the Kaggle metadata. We used a regular expression string to drop the duplicates. Once we cleaned the data we then refactored our code once again to clean the Kaggle data so that we can merge the Wikipedia and Kaggle DataFrames. Now that we have cleaned our data, we can add our movies DataFrame and MovieLens rating CSV data to our SWL database. 

After extracting, transforming, and loading our data we performed queries to ensure that all of the rows successfully output to the database:

![movies_query](https://user-images.githubusercontent.com/84881187/127754095-f7b25c56-03ec-44a6-a381-7fa07843f789.PNG)
*Our movies table has 31 columns hold a range 6048 different movies.

![ratings_query](https://user-images.githubusercontent.com/84881187/127754096-72d0f7e5-fdf7-43d2-a15d-f08de725bd1f.PNG)
*The ratimgs table has 5 different columns hold a range of 26,024,289 rows of individual users

After having cleaned the data, imorting all of the ratings rows took 1276.116042137146 total seconds, or 21.2 mins when we ran the code. By cleaning the data, Britta and her participants will have cleaned and structured data to use for the algorithms in the hackathon. 


![time_elapsed_block](https://user-images.githubusercontent.com/84881187/127754431-87883b84-35ff-4ac9-bbd7-06d26e79075e.PNG)

