# DS4A_Women_Summit

#### Project Goal:
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

#### Airline_traffic_stock_EDA_Sakshi.ipynb </br>

Sakshi created 5 columns for the flight_traffic table: 
- departure_delay (Actual_departure - Scheduled_departure), 
- arrival_delay (Actual_arrival - Scheduled_arrival) , 
- elapsed_delay (Actual_elapsed - Scheduled_elapsed ), 
- flight cancelled or not, 
- flight diverted or.

After combining flight_traffic and stock_price tables, she calculated the average departure_delay, arrival_delay, elapsed_delay for each airline_id, and the total numbers of flights cancelled or diverted on each day. She plotted those along stock prices for various airlines to find if there is any correlation among stock_price and any of these factors.
She found out that there is almost zero correlation of stock prices with these factors.
Based on this EDA, her assumption is that we cannot regress stock prices on these factors, and
delay/cancellation patterns do not have a substantial impact on stock / financial performance. 

#### Airline_EDA_Kessie.ipynb </br>
Kessie plotted the numbers of delays caused by the airline, weather, air_system, security and aircraft across different airlines. Her hypothesis is that airline delays can cause aircraft delay for the next flight. She also added event_original and event_destination columns which indicate whether there was an event at the original and destination airport on each day. In general, April, July and October have more delays and cancellations. Besides, she also plotted how the stock performance overtime for each airline. Based on the observation, AS airline has the highest stock price. In addition, she took the difference stock price between the previous date and the current date, and she was planning to use this difference as the response variable y for the regression model. 

#### EDA_NJ.ipynb </br>
Niharika calculated the total fares for each airline. She found that American Airlines Inc. has the highest fares for the entire year in 2017. She also plotted the difference between the numbers of flights that got cancelled/diverted vs the numbers of flights that did not get cancelled/diverted across different airlines. 

 
