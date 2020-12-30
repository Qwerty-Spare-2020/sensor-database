# sensor-database

Problem for R1 Batch (Enrolment Numbers BT19CSE001 to BT19CSE030):
Sensor Database
Physical Environment Sensor Network: A sensor network consists of spatially dispersed and dedicated sensors for monitoring and recording physical conditions of environment like temperature, sound, humidity, wind, and so on for multiple stations (you can consider different areas in city). The data from all sensors is collected at central location. Each sensor records the corresponding data at continuous time interval daily. Each sensor is represented by sensor ID (integer), sensor type, data it senses, time interval during which it senses the conditions continuously. Two sensors are said to be neighbours and can communicate if they are located at distance of 1000m apart. Solve the following question
Write a function create_data_structure () which will formulate the above mentioned sensor network in software. Data fields in the structure should include-
sensor_ID (integer)
sensor_type (char)
sensor_location(charater)(or sensor station)
duration(time interval ex. 5 min- it means that a sensor senses the temperature, humidity etc. after every 5 min.)
nearby_sensors (mostly array containing sensor_ID and distance in meters)
Central repository is the location where data from all sensors is collected and it should include following things-
sensor_ID
 Date
 Time
data(integer or float)
Retrieve_info() functions retrieves the data for sensors specified by following conditions
Depending on sensor type (retrieves till date data)
Depending on specified date for specific sensor type
Depending on specific time interval for specific sensor type
for specified date (single day)
for specified date range (multiple dates)
Implement above functions for particular station as well as for all stations.
Write a function find_communicating_neighbours () which should find all the neighbours of specified sensor. This function should check neighbourhood conditions mention above and should create the chain of neighbours. Ex. If node B and E is neighbour of A. C and D are neighbours of B. Then output should be like
A🡪B -> C
          -> D	
🡪E
Adapt the data structure created by create_data_structure () for sensor type which records multiple quantities. Ex. Air quality index (AQI) sensor which records entities like PM10, PM 2.5, nitrogen dioxide, sulphur dioxide, carbon monoxide, ground level ozone etc. and tries to find out Air quality level and pollution level. AQI is measures based on the average quantity of a particular entity measured over a standard time interval. Standard time interval for measuring averages is different for different entities (24 hours for most of the entities, 8 hrs.  For PM 2.5). There should be provision for storing standard time interval for each independent entity in existing data structure. Final AQI is the highest of the AQI values calculated separately for each entity. AQI value for finding health status is as follows
AQI
Status
1-50
Good
51-100
Satisfactory
101-200
Moderately polluted
201-300
Poor
301-400
May cause respiratory illness
401-500
Severe
501 onwards
Hazardous


Write a function to report or display the month during which maximum AQI is reported for all years for all stations.
Write a function to find out the date on which particular health status is recorded (input health status and station from user i.e. for which health status user wants to go)  
 Write a function to display the dates on which hazardous health status is recorded for all stations.
