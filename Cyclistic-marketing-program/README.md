
author: Maryna Volynets

date: 2025-03-03

# [Cyclistic Bike-Share Marketing Analysis](https://github.com/Maryna-Volynets/Data-Analysis-Portfolio/tree/main/Cyclistic-marketing-program)

---

Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, we want to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, we will design a new marketing strategy to convert casual riders into annual members.

## Project Overview
This project analyzes Cyclistic bike-share data for 2024 to identify behavioral differences between annual members and casual riders and provide data-driven marketing strategies to increase membership conversion and revenue.

### We need to answer the following questions:

1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

## Tools Used
- PostgreSQL — data cleaning and analysis
- SQL — querying and aggregation
- Tableau — data visualization
- GitHub — project documentation

### Data sources description

We use Cyclistic’s historical trip data to analyze and identify trends (Cyclistic trip data between 2024-01-01 and 2024-12-31) 
from [here](https://divvy-tripdata.s3.amazonaws.com/index.html). It is organised in 12 csv-format spreadsheets naming with year and month. 
This is public data that we can use to explore how different customer types are using Cyclistic bikes. There are no personally identifiable information or 
another privacy information.

### Cleaning and manipulation of data

 We used RDBMS PostgreSQL for data exploration and cleaning. Data was imported into PostgreSQL from csv files. We have a problem with data type columns 
 "start_lat", "start_lng", "end_lat", "end_lng". At first we defined text data type for these columns and then changed it for float data type. 
 Duplicates and inconsistent records were removed to ensure data accuracy and reliability of analysis. Some stations had identical coordinates but different names. These cases were reviewed and treated as potential inconsistencies in station naming.
 All manipulation described in [this file](https://github.com/Maryna-Volynets/Data-Analysis-Portfolio/blob/main/Cyclistic-marketing-program/Data_Cleaning_Analysis_Queries.sql).
 
 ### Data analysis: identify trends and relationships
 
Using SQL, we defined:

  1. **Annual members made 3 612 001 trips** in 2024 and **casual riders - 2 099 030**. The average trip duration for **annual members is 12 minutes**, while for **casual riders it is 21 minutes**.

![image](https://github.com/user-attachments/assets/8958d356-a71f-4186-8c08-0656f197e57f)

  3. **Annual members** make most trips on weekdays, especially **Tuesday through Thursday**, while **casual riders** use Cyclistic bikes most often from **Friday through Sunday**.

![image](https://github.com/user-attachments/assets/48c3c744-d679-4ba0-a7d4-261058de0cb6)

  4. Annual members and casual riders made most trips in **September**.

![image](https://github.com/user-attachments/assets/e8dd8ac3-1f02-4421-b07c-bfd0e9bf81a2)

  5. Most trips **(22 965) were started annual members from Kingsbury St & Kinzie St**, located in Chicago near the East Bank Club (Chicago’s premier health club). Most trips **(44 633) were started casual riders from Streeter Dr & Grand Ave station**, located in Chicago at the Addams (Jane) Memorial Park, on the shores of Lake Michigan. We assume that annual members use Cyclistic bikes for commuting or errands, while casual riders use Cyclistic bikes for bike ride.

![image](https://github.com/user-attachments/assets/dab4c191-3c8f-4491-804e-257ca6cb630a)


### Data visualization

The interactive dashboard was created in Tableau to explore ride patterns and user behavior:
[results](https://public.tableau.com/app/profile/maryna.volynets/viz/My-first-project/My-First-Project).

## Key Findings
- Annual members completed more trips than casual riders in 2024.
- Casual riders had longer average ride durations.
- Members used bikes mostly on weekdays, while casual riders used them more on weekends.
- Casual riders were concentrated near recreational and tourist areas.

## Recommendations
1. Launch weekend-to-weekday conversion campaigns targeting casual riders who frequently ride on weekends.
2. Promote annual memberships near high-traffic tourist and recreational stations, especially Streeter Dr & Grand Ave.
3. Offer limited-time discounts or trial membership plans for casual riders with repeated usage.
4. Use digital ads and in-app notifications focused on cost savings, convenience, and weekday commuting benefits.
