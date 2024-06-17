Overview

This project consists of a Python script that integrates weather data with police and fire incident data from Phoenix, AZ. It utilizes APIs to fetch data, processes it, and stores the data in a PostgreSQL database. The project also includes steps for cleaning and merging data.
Requirements

    Python 3.x
    pandas
    requests
    requests_cache
    retry_requests
    SQLAlchemy
    psycopg2

    Script Execution

    Database Connection: The script reads the database password from the CSV file and constructs a connection string to connect to the PostgreSQL database.

    Date Range Setup: The script sets up a date range to fetch data, using the current date and a date from a week ago.

    Weather Data Fetching: The script fetches weather data using the Open-Meteo API and processes the response into a pandas DataFrame.

    Police Data Fetching: The script constructs an SQL query to fetch police data from the Phoenix Open Data API within the specified date range and converts the response to a pandas DataFrame.

    Fire Data Fetching: Similarly, the script fetches fire incident data from the Phoenix Open Data API within the specified date range and converts the response to a pandas DataFrame.

    Data Cleaning: The script cleans the data by dropping rows with None values in critical columns and converting date columns to datetime objects.

    Data Storage: The cleaned data is stored in the PostgreSQL database.

    Data Merging: The script merges police incident data with weather data based on the hour of the incident and the hour of the weather data.
