# Farmigo_Database
To better track insights about customers and sales history we need to build a database of Farmigo data into a single file for ingestion. Farmigo data has been processed in a few repos but to be consistent it would be best to have a single source of truth that all repos pull from. 

## Requirements

The potential data sets to pull from will be: Anonymized Members (not just the member information but also the Shares they are associated with), Member Deliveries (individual anonymized member sales), Weekly Aggregate Deliveries, All Item (snapshot from Tuesday before store opens), All Subscriptions (snapshot from Tuesday before store opens), and BoxBuilder (snapshot from Friday).
