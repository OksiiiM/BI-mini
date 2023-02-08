# BI-mini
_______________________________________________
## Introduction
The project is part of BI course in Oldenburg University. 

## Goals of the project
The main goal is to practice all the BI process and to answer specific business questions provided in P05 BI mini project. 
The project consist of five main steps

1. Review the given dataset
2. Create a star schema model for the given dataset
3. Create a database schema, that is based on the designed schema model
4. ETL-Process
5. Visualization and KPIs 

## Data
BI mini project is based on data provided by OLU about IMDb-data. Data consist of three fiels in .tsv format about "movies", "actors" and "crew".
The data description is following:
#### Actor.tsv  – Contains the following information about actors:
* nconst (string) - unique value,  identifier of the name/person
* primaryName (string)– name by which the person is most often credited
* birthYear – in YYYY format
* deathYear – in YYYY format if applicable, else '\N'
* primaryProfession (array of strings)– the top-3 professions of the person
* knownForTitles (array of tconsts) – titles the person is known for

#### Movies.tsv - Contains the following information for movies:
* titleId (string) - a tconst, an unique identifier of the title, repeated in this dataset multiple times for titles in each language
* ordering (integer) – a number to uniquely identify rows for a given titleId
* title (string) – contains the titles in different languages
* region (string) - the region for this version of the title
* language (string) - the language of the title
* types (array) - Enumerated set of attributes for this alternative title. 
* attributes (array) - Additional terms to describe this alternative title, not enumerated
* isOriginalTitle (boolean) – 0: not original title; 1: original title

#### Newcrew.tsv – Contains the director and writer information for all the titles in IMDb:
* tconst (string) - unique value, identifier of the title
* directors (array of nconsts) - director(s) of the given title
* writers (array of nconsts) – writer(s) of the given title

The conection between the data is the following:

<img width="482" alt="Start Schema" src="https://user-images.githubusercontent.com/124779198/217551216-38dbd12a-dd35-4fa8-bd41-a0d0004f3808.png">

## Processes 
* The database is created in PostgreSQL and connected to DBeaver.
* Cleaning of the Data is done in Jupyter Notebook, Python.
* All the SQL queries are executed in DBeaver.


