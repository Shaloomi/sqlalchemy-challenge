
 # SQLAlchemy Homework - Surfs Up!

# Background
From sandy beaches with emerald-blue water and palm trees under tranquil skies to the rugged, black shoulders of volcanoes that continue to reshape the earth, the Hawaiian Islands teem with diversity. Beyond the terrain itself, the islands present a bedazzling variety of plants, animals and people, a colorful intermingling of different races and ethnic groups, epitomizing the U.S. experience of immigration, collaboration and living together.

This repository is designed to make a climate analysis on Honolulu, Hawaii, to help clients trip planning, and outline what they need to do in there vacation.
# Step 1 - Climate Analysis and Exploration
This project used a Python and SQLAlchemy to make climate analysis, and data exploration of the climate database. All of the following analysis completed by using SQLAlchemy ORM queries, Pandas, and Matplotlib. The complete climate analysis, and data exploration with python pandas notebook file found here starter notebook, and the SQLAlchemy file is also provided here hawaii.sqlite.

- SQLAlchemy engin created create_engine to connect to the sqlite database. engine = create_engine("sqlite:///Resources/hawaii.sqlite") inspector = inspect(engine)`

- To reflect the tables into classes, and save a reference to those classes called Station and Measurement an SQLAlchemy automap_base() is used.

# Precipitation Analysis
 - A query is designed to retrieve the last 12 months of precipitation data, and only the date and prcp values is slected.

 - The query results also loded into a Pandas DataFrame and the index is seted in to the date column, and sorted the DataFrame values by date.

 - Finally the result ploted by using the DataFrame plot method.The plot looks as follows:
 histogram.png
  -  By using the Pandas the summary statistics for the precipitation data was performed, and diplayed.
 #Station Analysis
- A query is designed to calculate the total number of stations, and 9 stations found. To find the most active station list, and observation counts is sorted in descending order. Station USC00519281 has the highest number of observations.

- A query is created to retrieve the last 12 months of temperature observation data (TOBS) and filter by the station with the highest number of observations. The Plot for the results as a histogram with bins=12 were created and it looks as follows.
 
 histogram.png
  
  
# Step 2 - Climate App
After the initial analysis was completed, a Flask API designed based on the queries already developed.

- The following routes are created by using Flask. To look and run the code click the following link:app.py

# Routes
 - /

   - Home page.

   - List all routes that are available.

- /api/v1.0/precipitation

  - Convert the query results to a dictionary using date as the key and prcp as the value.

  - Return the JSON representation of your dictionary.

- /api/v1.0/stations

  - Return a JSON list of stations from the dataset.
- /api/v1.0/tobs

  - Query the dates and temperature observations of the most active station for the last year of data.

  - Return a JSON list of temperature observations (TOBS) for the previous year.

- /api/v1.0/<start> and /api/v1.0/<start>/<end>

  - Return a JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.

  - When given the start only, calculate TMIN, TAVG, and TMAX for all dates greater than and equal to the start date.

  - When given the start and the end date, calculate the TMIN, TAVG, and TMAX for dates between the start and end date inclusive. 
 
 
 
 

