# Cyclistic-marketing-program

author: Maryna Volynets

date: 2024-09-21

---

Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, we want to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, we will design a new marketing strategy to convert casual riders into annual members.

### We need to answer the following questions:

1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

### Data sources description

We use Cyclistic’s historical trip data to analyze and identify trends (Cyclistic trip data beetwen 2024-01-01 and 2024-12-31) 
from [here](https://divvy-tripdata.s3.amazonaws.com/index.html). It is organised in 12 csv-format spreadsheets naming with year and month. 
This is public data that we can use to explore how different customer types are using Cyclistic bikes. There are no personally identiable information or 
another privacy information.

### Cleaning and manipulation of data

 We used RDBMS PostgreSQL for data exploration and cleaning. Data was imported into PostgreSQL from csv files. We have a problem with data type columns 
 "start_lat", "start_lng", "end_lat", "end_lng". At first we defined text data type for these columns and than changed it for float data type. 
 We cleaned the data from duplicates, and removed records with empty values in the station coordinates, removed rows where the trip start time is later than 
 or equal to the trip end time. We also found that some stations had exactly the same coordinates but different names and removed them, considering such data 
 to be erroneous. All manipulation described in [this file](https://github.com/Maryna-Volynets/Data-Analysis-Portfolio/blob/main/Cyclistic-marketing-program/Data_Cleaning_Analysis_Queries.sql).
 
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

We used Tableau for visualization our [results](https://public.tableau.com/app/profile/maryna.volynets/viz/My-first-project/My-First-Project).

### Conclusions and Recommendations

1. Annual members use Cyclistic more frequently, but at shorter intervals than casual riders. Annual members make the most trips from Tuesday to Thursday, while casual riders make the most trips from Friday to Sunday.


2. Casual riders are likely to purchase an annual membership to Cyclistic to use bikes for everyday needs.


3. Cyclistic can use advertising messages to send to casual riders' smartphones with offers to purchase an annual membership on favorable terms for using the program on weekdays.



