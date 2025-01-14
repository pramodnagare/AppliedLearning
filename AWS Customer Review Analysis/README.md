### Aim: 
Amazon Customer Reviews Analytics

### Description:
This project aimed to develope a data analytics dashboards for Amazon Customer Review Dataset. This is an extension to the project GCP Data Analytics Piepline. It considers the data is avaiable on GCP big-query for instance and then can be queried and visualize using GCP big-query and data studio. We can connect big query database to other analytical tools such as Tableau, Power BI, Microstrategy, Excel, Looker and so on.


### Tags: 
analytics-pipeline, pub-sub, big-query, data-flow, tableau-dashboards

### Dataset: 
Avaialable on https://registry.opendata.aws/amazon-reviews/

### Python Implementation:
**AWS Customer Review Analysis.ipynb**

### Sample data:
It is available in Data folder, you can complete dataset from the link mentioned above

### Best practice:
For querying and analytics is to load small data an build and test query against that. Once query and dashboards are ready then load the complete data to big-query or change the data source for production database and execute the queries. This will save time and money for the enterprise.**


## Uploading Data from Local Machine to GCP Big Query:
**Follow the AWS Customer Review Analysis.ipynb file to setup and upload data to GCP big query database**

**Once Data is uploaded to big-query, we can query our data to perform some quick analytics**

## Quering GCP Big-Query:

**1. Login to GCP Console https://console.cloud.google.com and Navigate to Big Query service**

**2. Select the Project ID and Dataset for the Amazon Customer Reviews**

**3. Explore the Reviews table and related schema which is auto detected while uploading data**

<img src="images/1.png">



### 4. Query your data for first 50 records just the quick look of the data

**Note: Usage of * in SELECT query is not a good practice. The below query is for demo purpose.**

<img src="images/2.png">

**NOTE: Before execution of the query GCP will let you know what size of data it will process for the qiven query and it will bill against that. Also, GCP will cache that data for the future related queries to avoid long execution and related billing **

### 5. Once a query is executed, GCP will show you the result and statistics

<img src="images/3.png">



### 6. Let's try to re-execute the same query to see if execution time

<img src="images/4.png">

**NOTE: You can see that there is no execution time for displaying the result as it was read from caches. You can disable the cache by clicking More --> Query Settings --> Cache Preference --> Uncheck the box Use cached results**



### 7. Query for Average star rating, Total votes and helpful votes by product category

<img src="images/6.png">

**NOTE: You can see the JSON result on the console**

<img src="images/7.png">

**NOTE: To see the Job Information on the console**

<img src="images/8.png">



### 8. Query top 5 product for each category with average star rating is greater than 4.5 and number of review is graeter than 10

**NOTE: You can see the JSON result on the console**

<img src="images/13.png">



### 9. Query top 10 customers to review products and related average star rating

**NOTE: You can see the JSON result on the console**

<img src="images/14.png">



## Analytics:

**Let's perform some analytics on Amazon Customer Reviews with GCP Data Studio**

[Interactive Dashboard Avaiable here](https://datastudio.google.com/embed/reporting/ac4f50d1-f071-4045-a23b-feafa9a80553/page/U6VAB)

**Overall Dashbaord**
<img src="images/18.png">



**Drilling and Filtering on JP Marketplace**
<img src="images/19.png">



**Drilling and Filtering on 2009 Year and Verified purchase**
<img src="images/20.png">

**NOTE: We can improve the query performance using the BI engine service provided by GCP for big query analytics which will be running the complete query execution in memory for high throughput. It is on demand and recommended for big data services**
