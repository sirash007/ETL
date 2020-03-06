# ETL
ETL Project 1.5

Ashwin Patel
Anastasia Bolboceanu
Vallie Tracy
Extract Transform Load (ETL) Project
Data analytics Bootcamp
March 7, 2020 
Proposal: To establish how many contributions per city and how many hospitals are in the same city.
Data analysis and management requires data integration. These data may come in different formats and sources 
such as csv files, json, files, or html tables. Integration of various datasets is a key for data analysis. In other words, identifying the dataset, extracting and reading the data, cleaning and structuring it in the desired format, and loading the clean data into a database for storage is imperative for analysis and management. Integrating this is an important part of working with data. For this ETL project we will use opensecrets.org website, which contains financial information about U.S. politics (we looked specifically at Minnesota)....and the Hennepin County website-from where we will collect data concerning the density of Hospitals in MN.
Data source:
mndivs.csv -> opensecrets.org
Minnesota_Hospitals.csv -> Hennepin County website 

Data Format
Both opensecrets.org and Hennepin County websites list files in a CSV format. There is a total of two CSV files. 
These datasets contain information about the annual amount of contributions, location of hospitals by city, state 
and address, and different other factors showing the financial situation of hospitals. 
Data Extraction and Cleanup/Transformation
We will use pandas to extract and clean these csv files. Cleaning the data required to strip away any unnecessary 
variables. The data sets will require us to use the y-axis labels as our columns and we will transpose the dataset using Jupyter Notebook. Finally, we pushed the dataset into MySQL database and joined the two tables using their respective"City" columns. We did the data cleaning process for the "Minnesota_Hospitals" extracting the columns we considered most important. We renamed the columns, dropped the duplicates and set an index. We encountered a challenge of reading the csv file named "mndivs_df". To encode we had to use a special code "ISO-8859-1". Then, while working in SQL- creating tables - we had to pay extra attention at the spelling of the columns' names. We had to use double quotes for the name of the columns. Also, at the begining we encoutered difficulties transfering the data from dataframe to SQL tables because we didn't follow the exact name and order of the columns. 
Data Storage into a Database
We used relational database, MySql database, for storage and created a connection using Jupyter Notebook. 
We then created a database, pushed and joined the tables using "City" column as key for joining the CSV files. 
