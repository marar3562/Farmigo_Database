# Farmigo_Database
Farmigo is Fair Share's Point of Sale (PoS) system for members. It contains critical information for the organizaiton, like customer information, item information, which items start in member shares (boxbuilder), etc. This repo was created to collect Farmigo data to support additional customer specific insights and more granular insights about business operations. Farmigo data has been processed in a few repos but to be consistent it would be best to have a single source of truth that all dashboards pull from. 

![alt text](process_image.png "Stepped Process for Frrmigo Data Process")

## Requirements

There are seven data sets I settled on collecting from Farmigo, but there are technically more potential files we could collect:
1. Member Groups (each member and their weekly share assignment and location for pickup)
2. Member Deliveries (items each member purchased each week with quantity and price)
3. Member Information (more detailed member information, like member balance, join date, etc.)
4. Member Payments (dated payments to Fair Shares for future shares)
5. Subscription Options (running order items, like weekly milk or eggs, but also share tradeable items)
6. Box Builder (items added to each member group to start each week)
7. Item Information (all items and the details behind each, like price, description, image link, etc.)

Item Information and Subscription Option files are collected on Tuesdays (before members purcahse items), but all other files are collected on Friday (after member sales). Tuesday files are collected on that day to capture a snapshot of what inventory or prices start at before members purchase items.

A big part of this process is anonymizing member data. I created a process for anonymizing member data so that we could collect these CSV files in Github. I did not want personal member names or emails in Github so that was the priority BEFORE CSV files ended up in Github. We anonymize members by a combination of First/Last Name and email address. This is not a perfect process, but it is a good starting point. A future project might be to create a more condensed member table that combines multiple member accounts that should be shared. 
