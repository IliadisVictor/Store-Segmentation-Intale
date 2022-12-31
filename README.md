# Business Intelligence Class - Developing Strategies for Intale

This is a project to develop market segments based on Intale's clientele with the goal of identifying unexploited business opportunities in the small retail market of Greece. The goal is for Intale to use the insights mined here to expand their services and offer a more customized experience catered to the needs of each store owner that uses the Intale CRM. Intale was established in 2010, and since then it is proud to have hundreds of kiosks and mini-markets using their software "Intale Point" to manage and control their cash register, shifts, warehouse, suppliers and customers.

## Data 

Intale provided two different datasets. The first one contained information about invoices with the exact date-time a product was purchased in what quantities, in which store and the revenue it generated. Here are some example transactions from dataset 2:

| StoreId | DateTime                | InvoiceId | InvoiceGlobalId | CategoryId | Quantity | Revenue |
|---------|-------------------------|-----------|-----------------|------------|----------|---------|
| 6463    | 2021-10-13 15:51:33.000 | 292262    | 6463_292262     | 115        | 2        | 4       |
| 4139    | 2021-10-23 20:30:38.000 | 839785    | 4139_839785     | 28         | 1        | 4.6     |
| 5078    | 2021-10-08 20:34:33.000 | 647668    | 5078_647668     | 28         | 1        | 4.6     |

The second dataset contains information about the sales of each product for a store in a specific month and again, the revenue that specific category generated. Some example sales reports:

| Period | Date_Year | Date_MonthName | StoreId | CategoryId | Quantity | Revenue |
|--------|-----------|----------------|---------|------------|----------|---------|
| MATYA  | 2020      | January        | 4209    | 41         | 135      | 132.5   |
| MAT    | 2021      | February       | 5114    | 31         | 13       | 27.1    |
| MAT    | 2021      | November       | 5400    | 41         | 2        | 2       |

The data can be found in the folder Data. It should be mentioned that there are three more sheets in the excel file. The category sheet provides the name of the category for category IDs seen in dataset 1 and 2. The store's sheet provides geographical information for each store, as well as its type, small kiosk or mini-market. The period sheet explains the months included in the two periods coded as MAT and MATYA seen only in dataset 1. 

## Segments - Clustering
For each dataset, clustering was conducted with the help of Pandas and Rapid Miner. During the procedure Kmodes, Kmeans and KPrototypes was tested after doing the necessary preprocessing for each. 



### Clustering Dataset 1 
Clustering Basis using K-Prototypes 

1. Store Type – String ( Mini-Market , Kiosk)
2. Location - String 6 Geographical Locations
3. 4 Variables for 4 Seasons – Percentage of yearly sales that occurred on that season .
4. AVG Retail Price – Total revenue divided by total items sold
5. AVG Monthly Revenue – Grouped Sales Revenue by Month and calculated the average.
6. AVG Items Sold - Grouped Items sold by Month and calculated the average.
7. Categories Variety – Amount of different categories sold .
8. Categories Concentration – How many categories amount for 80% of revenue.




### Clustering Dataset 2

Clustering Basis using K-Means( Elbow method to decide on amount of clusters)

1. Average Daily Transactions
2. Average Revenue/Transactions
3. Average No of Categories per Transaction
4. Average Items per Transaction
5. Weekend Revenue (as percentage of Total Revenue) – 2 variables, one for weekdays and one for weekends
6. Off-Peak (7:00-23:00) Revenue (as Percentage of Total Revenue) – 2 variables, one for peak and one for off-peak hours

## Some of the proposed strategies based on Dataset 1

### Opportunity for Cross - Selling 

A rather large percentage of the stores especially the ones found in the more rural parts of Greece avoid selling newspapers and tickets. These specific products have a miniscule profit margin. As a result many owners have stopped selling them, ignoring the opportunity to establish themselves, for say, as the spot to buy tickets in the area, profiting from the cross selling that will surely happen when customers flock to the store. 

### The opportunities given by Covid to mini-markets

The fear of being around people caused by the Covid crisis created the opportunity for mini-markets to be more competitive against supermarkets. A positive correlation was found between the number of different categories a mini-market offers and its total revenue. The fear of contracting covid drove customers to smaller mini-markets in order to fulfil their needs without being in danger. The proposal was for mini-markets to ask their suppliers for a larger breadth of categories, in an attempt to claim some of the purchases previously made in larger vendors, like cleaning products. 

## Some of the proposed strategies based on Dataset 2

### Opportunities for a Large Kiosk in Central Location

Most of the sales in kiosks found in central locations had most of their sales on working early hours, probably exactly before people went to work. The proposal was to include packaged coffee and puff pastry products to replace the visit a greek would probably make in a coffee shop for his breakfast and coffee before heading to work. 



**For the full report on the proposed strategies and the technical appendix please see the uploaded pdf** 
