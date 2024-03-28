# Zuber (SQL)

## Introduction

Zuber, a new ride-sharing company is launching in Chicago. Working with a database, data from competitors will be analyzed and a hypothesis about the impact of weather on ride frequency will be tested.

## Goal

Determine if ride times increase with changes in weather.

## Key Findings

The null hypothesis that the average duration is the same on rainy and dry Saturdays is rejected. This was done using a two sided t-test. Instead, the test found that rainy and dry Saturdays have a different ride duration time.

## Data Description

A database with info on taxi rides in Chicago is provided on the TripleTen platform with multiple tables:

1. `neighborhoods` table: data on city neighborhoods

    - name: name of the neighborhood
    - neighborhood_id: neighborhood code

2. `cabs` table: data on taxis

- cab_id: vehicle code
- vehicle_id: the vehicle's technical ID
- company_name: the company that owns the vehicle

3. `trips` table: data on rides

- trip_id: ride code
- cab_id: code of the vehicle operating the ride
- start_ts: date and time of the beginning of the ride (time rounded to the hour)
- end_ts: date and time of the end of the ride (time rounded to the hour)
- duration_seconds: ride duration in seconds
- distance_miles: ride distance in miles
- pickup_location_id: pickup neighborhood code
- dropoff_location_id: dropoff neighborhood code
4. `weather_records` table: data on weather
- record_id: weather record code
- ts: record date and time (time rounded to the hour)
- temperature: temperature when the record was taken
- description: brief description of weather conditions, e.g. "light rain" or "scattered clouds"

![database](pics/database.png)

## Project Steps

### Step 1. Parse Data

- Find weather data in Chicago by parsing appropriate html
- This portion can be found [here](steps/parse.ipynb)

### Step 2. Exploratory Data Analysis (SQL)

- Find the number of taxi rides for each taxi company for November 15-16, 2017.

- Find the number of rides for every taxi company whose name contains the words "Yellow" or "Blue".

- Find the number of rides of the two most popular companies.

- This process can be found [here](steps/eda-sql.ipynb)

### Step 3. Hypothesis Testing  (SQL)

Find the duration of rides from the the Loop to O'Hare International Airport changes on rainy Saturdays.

- Retrieve the identifiers of the O'Hare and Loop neighborhoods from the neighborhoods table.

- retrieve the weather condition records from the weather_records table and find good and bad weather days.

- Find airport trips and obtain the weather conditions and duration for each ride.

- This process can be found [here](steps/hyp-sql.ipynb)

### Step 4. Exploratory data analysis

- Use datasets collected from SQL (step 2)
- Continue EDA in [python](steps/zuber.ipynb) 

### Step 5. Testing Hypothesis (Python)

- Use datasets collected from SQL (step 3)
- Test hypothesis that duration is similar despite weather found [here](steps/zuber.ipynb)