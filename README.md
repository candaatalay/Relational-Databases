# Relational-Databases


## Table of Content

- Project Description
- Installation
- Entity-relationship model
- Security and Backup
- End Product
- Further Study




## Project Descritpion 

This project is a replica of a dashboard I was building for work, in real life example I worked with different datasets provided by different teams in then company to build an internal tool. Original data was stored on [BigQuery](https://cloud.google.com/bigquery), created a combined table on Sheets and presented the final data on and [Looker Studio](https://datastudio.google.com/).

Here, I created a mock version of similar data with 5 made up customers and 3 products, to show a similar process to the creation of dashbaord. 

## Installation

mock_database is built completely on PostgreSQL 15.1, for download instrutions [visit this link](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads).

## Functinalities

This data is mainly used to see the used quota of each customer, by matching collections with the contract owners (customer id) as well as providing extra details about the product they purchased in the contract. 
In the final dashboard a functionality for account managers to add comments regarding the contract is added, refeering to comments_collected. It is added as a column later to the contract_dataset.  

## Entity-relationship model 
![alt text](https://github.com/candaatalay/Relational-Databases/blob/main/Database%20ER%20diagram.jpeg)

## Security and Backup

Since the data contains sensative information, security is necessary. This is achieved by restricted access to original data and not allowing tempering with the original data, only with the backup. 
For backup, table is exported with [Google Cloud Console](https://cloud.google.com/cloud-console) by BigQuery API. Alongside that snapshots of table is also stored in BigQuery.

## End Product
Once the data normalization is done final data is presented in Looker Studio with a drop down list and corresponding consumption information, total quota and graph of usages over months appears.
[alt text](https://github.com/candaatalay/Relational-Databases/blob/main/end_product.PNG)


## Further Work
