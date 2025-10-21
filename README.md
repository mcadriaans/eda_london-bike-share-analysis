# London Bike Share Analysis (2015-2017)

![image](https://github.com/user-attachments/assets/edb90b1e-203d-439f-8a0d-b12def24bba3)

Welcome to the London Bike Share Analysis repository. This project aims to analyze bike share data to uncover insights and answer key business questions. The repository includes an interactive Tableau dashboard, a Python notebook for Exploratory Data Analysis (EDA), and a markdown file with SQL business questions and answers.

## What is bike sharing?
Bike sharing is a transportation service in which bicycles are made available for shared use to individuals on a short-term basis, typically for a small fee or for free in some cases. It offers a convenient and eco-friendly way to navigate urban areas, providing an alternative to traditional modes of transport like cars and public transit.


## Project Overview
This project explores the London Bike Share dataset from 2015 to 2017. The analysis encompasses data cleaning, visualization, and statistical analysis to understand bike-sharing usage patterns in London.

## Repository Contents
* Exploratory Data Analysis Notebook (EDA.ipynb): Jupyter Notebook containing data exploration, cleaning, and initial analysis.
* Tableau Dashboard: Provides interactive visualizations of bike-sharing data + Guide to navigating the dashboard.
* SQL markdown which documents questions and answers to key business questions about the bike share data.

## Dataset 
*The London bike sharing dataset provides information on bike-sharing activity in London, capturing details such as the number of bike shares, weather conditions, temperature, humidity, wind speed, holidays, weekends, and meteorological seasons. This dataset helps analyze and understand factors affecting bike-sharing trends and patterns over time.*

### Source: 
The data was acquired from 3 sources:
>* https://cycling.data.tfl.gov.uk/ 'Contains OS data © Crown copyright and database rights 2016' and Geomni UK Map data © and database rights [2019] 'Powered by TfL Open Data'
>* freemeteo.com - weather data
>* https://www.gov.uk/bank-holidays



### Column details

| Column         | Description                               | Additional Information                              |
|----------------|-------------------------------------------|-----------------------------------------------------|
|**timestamp**   | Date and time data was grouped            |                                                     |
|**cnt**         | Count of new bike shares                  |                                                     |
|**t1**          | Actual temperature in Celsius             |                                                     |
|**t2**          |"Feels like" temperature in Celsius        |                                                     |
|**hum**         | Humidity in percentage                    |                                                     |
|**wind_speed**  | Wind speed in kilometers per hour         |                                                     |
|**weather_code**| Weather condition category                |1:clear, 2:scattered clouds, 3:broken clouds, 4:cloudy, 7:rain, 10:thunderstorm, 26:snowfall, 94:freezing fog |     
|**is_holiday**  | Boolean indicating if the day is a holiday| 1 for holiday, 0 for non-holiday                    |
|**is_weekend**  | Boolean indicating if the day is a weekend|1 for weekend, 0 for weekday                         |
|**season**      | Meteorological season                     | 0 for spring, 1 for summer, 2 for fall, 3 for winter|

## Technologies Used

*   Python (with libraries like Pandas, NumPy, Matplotlib, Seaborn)
*   SQL (PostgreSQL)
*   Tableau
*   Markdown

##  Project Structure

```bash
├── 📁 data
    └── bike_sharing.csv
├── 1.London_bike_sharing _EDA.ipynb          # Jupyter notebook for exploratory data analysis (EDA)         
├── 2.SQL_Exploratory_Analysis.md             # Markdown file documenting SQL-based insights or queries run on the dataset
├── 3.London_bike_sharing_Dashboard.md        # Link to Tableau Dashboard
├── 4.London_bike_sharing_Dashboard_Guide.pdf # PDF guide explaining how to use or interpret the dashboard
└── README.md                                 # Project overview, setup instructions, and context — You’re reading it!
```

## Key Findings

This analysis of London's bike-sharing data from 2015-2017 revealed critical insights into usage patterns, demand drivers, and operational implications:
* The service facilitated nearly **20 million bike rentals** over the two-year period, underscoring its significance in London's public transport.
Ridership demonstrated **positive year-over-year growth** from 2015 to 2016, indicating increasing adoption and importance.
* Bike rentals peak significantly during **weekday commute times (8 AM and 5 PM)**, with Thursday being the busiest day of the week.
* Average **weekday rentals (29,213/day) are ~26% higher** than average weekend rentals (23,242/day), confirming that commuting is the primary driver of service usage, rather than leisure. Holidays generally see the lowest usage.
* **Summer is consistently the most popular season**, with bike rentals peaking during warmer months and declining significantly in colder periods.
* A **strong positive correlation exists between temperature and bike rentals**, where ridership increases with rising temperatures.
* **Clear weather conditions and broken clouds are optimal** for bike sharing, while rain, snow, and thunderstorms deter usage.
* The **optimal humidity range for bike sharing is 61-80%**. However, both the highest and lowest daily rental volumes surprisingly occurred at very high humidity levels (82% and 88.5% respectively).
    * This suggests that while high humidity can be a deterrent, other powerful factors (like temperature or events) can override this discomfort, particularly for peak demand.
* Hourly bike rental demand is highly concentrated, with **only the top 10% of hours classifying as "High Traffic."** This highlights the importance of precise resource allocation during predictable peak windows.
--------------------------------------------------------------------------------------------------------------------------------------------------------
