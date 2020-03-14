# DS4A_Women_Summit

Project Goal:
In this project, we are trying to see if delay/cancellation patterns impact stock / financial performance at all. 

#### Data:
Airline Travel -- includes datasets for commercial airline traffic, passenger fares, major US events, weather, and airline stock prices
 
 * airlines.csv: Mapping of airline codes to names.
 * airports.csv: Important details (name, state, identifier, latitude, longitude, etc.) on various US airports.
 * events_US.csv: Public events from around the US throughout 2017.
 * fares.csv: Airline fare distributions for each quarter-route-airline combination in 2017 with a bucket size of $10.
 * flight_traffic.csv: Information about delays for US domestic flights in 2017.
 * stock_prices.csv: Daily closing stock prices of various US airlines from late-2016 to early-2018.
 * weather.csv: Weather data (temperature, wind, precipitation, cloud cover, etc.) collected at various US airports every 6 hours through 2017.


### Run

In a terminal or command window, navigate to the top-level project directory and run one of the following commands:


```bash
Airline_traffic_stock_EDA_Sakshi.ipynb
EDA_NJ.ipynb
Airline_EDA_Kessie.ipynb
```

### Summary

* Airline_traffic_stock_EDA_Sakshi.ipynb
In order to have insights, I combined data from 2 tables: flight_traffic.csv and stock_prices.csv
Flight_traffic has data for each flight with columns like airline_id, origin and destination airports, and various other statistics like :
Actual_departure, scheduled_departure-> departure_delay
Actual_arrival, scheduled_arrival -> arrival_delay
Actual_elapsed, scheduled_elapsed -> elapsed_delay
Flight: cancelled or not
Flight: diverted or not

Also, stock_prices 
Have columns like day, airline_id and stock_price that day.

I combined those tables and got 
For each airline_id: average departure_delay, arrival_delay, elapsed_delay.
Also Total no. of flights cancelled or diverted on each day
And plotted those along stock prices for various airlines to find is there any correlation among stock_price and any of these factors.
I found out there is almost zero correlation of stock prices with these factors.
So, my analysis is that we cannot regress stock prices on these factors. 
So, delay/cancellation patterns do not have a substantial impact on stock / financial performance.

 
