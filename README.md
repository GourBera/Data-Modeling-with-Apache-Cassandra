# Data Modeling with Apache Cassandra

Project 2: Udacity Data Engineering Nanodegree

### **Introduction**
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.


>They'd like to implement data modeling with Apache Cassandra and ETL pipeline using Python.
>> - Data modelling Apache Cassandra to run queries
>> - Building ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.
>> - Create and Test tables by running analytics queries and verify the results.



### **Project Datasets**

> **event_data**

The directory of CSV files partitioned by date. Below are examples of filepaths to two files in the dataset: 


>> event_data/2018-11-08-events.csv

>> event_data/2018-11-09-events.csv

<img src="image_event_datafile_new.jpg">


### **Create queries for following questions **

> **1. Give me the artist, song title and song's length in the music app history that was heard during  sessionId = 338, and itemInSession  = 4**

> **2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182**
    
> **3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'**


### **Project Template**

> The project template includes one Jupyter Notebook file:

>> Process the event_datafile_new.csv dataset to create a denormalized dataset
>> Model the data tables keeping in mind the queries you need to run
>> Based on provided queries model data tables
>> Load the data into tables create in Apache Cassandra and run queries and validate


### **Project Template**
Steps to follow to complete each component of this project

> **Modeling NoSQL database or Apache Cassandra database**

>> 1. Design tables to answer the queries outlined in the project template
>> 2. Write Apache Cassandra CREATE KEYSPACE and SET KEYSPACE statements
>> 3. Develop your CREATE statement for each of the tables to address each question
>> 4. Load the data with INSERT statement for each of the tables
>> 5. Include IF NOT EXISTS clauses in CREATE statements to create tables only if the tables do not already exist. Also include DROP TABLE statement for each table, this way it can run drop and create tables whenever we want to reset database and test ETL pipeline
>> 6. Test by running the proper select statements with the correct WHERE clause



### **Build ETL Pipeline**

>> 1. mplement the logic in section Part I of the notebook template to iterate through each event file in event_data to process and create a new CSV file in Python
>> 1. Make necessary edits to Part II of the notebook template to include Apache Cassandra CREATE and INSERT statements to load 
>> 1. processed records into relevant tables in your data model
>> 1. Test by running SELECT statements after running the queries on your database
