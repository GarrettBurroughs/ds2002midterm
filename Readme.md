# DS 2002 Midterm - Sakila Rental Data Warehouse
**Garrett Burroughs** 

This repository hosts the midterm project for DS 2002. This project is an ELT process that takes data from multiple soruces (A MySQL database, a MongoDB cluster, and an API endpoint), and conglomerates them into a data warehouse that uses a star schema to represent a rental fact.  

# Submission
For grading purposes, look at [notebook/midterm.ipynb](notebook/midterm.ipynb) For the ETL process and [notebook/prepare_data.ipynb](notebook/prepare_data.ipynb) for the code that sets up the data in the different sources. More information about this repository can be read below.


## Running
**Note:** These are instructions if you wish to run the project completely on your own with your own databases, clusters, and endpoints. The project is configured to work with pre-existing databases and endpoints out of the box.

To run this project, you must have python and jupyter installed as well as run `pip install -r requirements.txt`. If the databases and endpoints are not yet setup, you should first run the data files in `sakila-db` to  set up the MySQL database. Once the database is set up, run the code in the `notebook/prepare_data.ipynb` which will produce JSON data to be stored at an API endpoint, and store the data at the mongodb cluster. Ensure to modify the `atlas_cluster_name` `atlas_user_name` and `atlas_password` as well as `mysql_uid` `mysql_pwd` and `mysql_url`. 

## Files 
**notebook/prepare_data.ipynb:** The code that extracts the data from the database to be put in different sources <br />
**notebook/midterm.ipynb:** The code that runs the ETL process <br />
**notebook/films.json:** The json data stored at the api endpoint <br />
**sakila-db/:** The sakila database files used for this project  <br />
**create_date_dim.sql:** The SQL file used to create the date dimension

