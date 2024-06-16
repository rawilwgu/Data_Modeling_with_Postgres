### Purpose
The purpose of this database is to simply queries into their JSON based data. Sparkify is interested in what songs their users listen to, thus they need a database and ETL pipeline that allows them to look up this information efficiently.

### Running the scripts
To perform the ETL, you would first need to run create_tables.py in the terminal with the command "python create_tables.py". From there, run the ETL file that extracts the files and inserts them into the database using "python etl.py". 

### Files
The data folder contains the log files in JSON format that are extracted and loaded into the data store through jupyter.

ETL.ipynb tests the individual pieces of code for the ETL process.

test.ipynb does more exact testing to confirm the datatypes, not null constraints, and primary keys. It confirms that the data loads correctly and that the tables are created correctly.

create_tables.py will create the tables from the sql_queries.py file.

etl.py will extract, transform, and load all of the data from the data folder into the database.

README.md is this current file, describing the functions and process.

sql_queries.py has all the individual queries to create the tables, perform inserts, and run queries for the extraction and load process.

### Schema

The schema is a star schema, with the songplays table being in the fact table center of the other dimension tables. This format is the best format for queries. It provides a route through simple joins to look up the songs that users are listening to.