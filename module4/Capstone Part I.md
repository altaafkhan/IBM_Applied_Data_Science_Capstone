# 1.0 Introduction/Business Problem
## 1.1 Background
Sydney, the state capital of New South Wales also the largest city in Australia. A place that I have called home for 18 years now. A lively metropolis with lots of restaurants and bars to choose from. 

## 1.2 Problem
The city is packed on Friday evenings with people who work in the Central Business District (CBD) having a few drinks or a meal with their work colleagues, friends or family. The problem I am trying to solve with this project is, with so many options available for bars and restaurants, which ones are worth spending Friday evening’s at based on rating and price within a 3 kilometer radius of the CBD. 

## 1.3 Audience
My target audience is professionals who work in the city and don’t mind paying mid to high range for venues to relax and unwind after the working week. 


# 2.0 Data
Overview of data sources, what data elements are available and how I will be using it for the Capstone Project. 

## 2.1 Sources
1. Australian postcode and suburb (locality) data, mainly for Sydney. Source: [Matthew Proctor](https://www.matthewproctor.com/australian_postcodes). Turns out this data is not freely available on Australia Post website or on Wikipedia. Luckily, I came across this website that publishes a full downloadable list, which was last updated on 16th May 2020. 
2. [Foursquare](https://foursquare.com/city-guidedata) for restaurants and bars reviews

## 2.2 Data Description
### 2.2.1 Australian Locality & Postcode Data
I have included a data dictionary for the locality and postcode data set. However, I will only be using the following for my analysis:
- Postcode
- Locality
- State
- Longitude
- Latitude 
- SA3 Name

|Field    |Description    |Example|Updated|
|:--------|:--------------------------------------------------------------------------------------------------------------------------------------------|:---------|:------|
|id       |Primary Key from source database                                                                                                             |4483      |Regularly|
|postcode |The postcode in numerical format - 0000 to 9999                                                                                              |2000      |Regularly|
|locality |The locality of the postcode - typically the city/suburb or postal distribution centre                                                       |Sydney    |Regularly|
|state    |The Australian state in which the locality is situated                                                                                       |NSW       |Regularly|
|long     |The longitude of the locality - defaults to 0 when not available                                                                             |151.256649|Regularly|
|lat      |The latitude of the locality - defaults to 0 when not available                                                                              |-33.859953|Regularly|
|dc1      |The Australia Post distribution Centre servicing this postcode - defaults to blank when not available                                        |SYDNEY    |Infrequently|
|type1    |The type of locality, such as a delivery area, post office or a "Large Volume Recipient" such as a GPO, defaults to blank when not available |Delivery Area|Regularly|
|SA3      |The SA3 Statistical Area code                                                                                                                |11703     |Adhoc|
|SA3 Name |The name of the SA3 Statistical Area                                                                                                         |Sydney Inner City|Adhoc|
|SA4      |The SA4 Statistical Area code                                                                                                                |117       |Adhoc|
|SA4 Name |The name of the SA4 Statistical Area                                                                                                         |Sydney - City and Inner South|Adhoc|
|Region   |Designated Regional Area                                                                                                                     |R1         |     |
|Status   |A note indicating whether the data is new, removed or updated - new column Nov 2018                                                          |Updated 19-May-2020|Regularly|

### 2.2.2 Foursquare Data
Data retrieved using Foursquare contains a log of details of venues. I will mainly be using the following attributes;
- Name 
- Location: Latitude, Longitude, Locality
- Category – since I will be narrowing the venues down to restaurants and bars
- Ratings
- Likes 


## 2.3 Methodology:
- Extract data from both sources
- Transform the data to include elements such as latitude, longtitude, restarutant/bar ratings on Foursqaure, etc. I will require for analysis. 
- Exploratory data analysis.
- Clustering suburbs (localities) and performing analysis on them.
- Visual representation of cluster analysis to understand trending hotspots.
- Results and conclusion.

A detailed step by step methodology report will be prepared during the second part of this project.
