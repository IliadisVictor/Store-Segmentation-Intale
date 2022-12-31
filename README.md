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

