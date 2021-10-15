# Targeting areas for an EV charging station company

Roberto Linares



## Abstract

ElectricNow (a California-based company that focus in installing charging stations at home for EVs), that is planning to expand their operations to Washington State, 
and even when their sales are green numbers, their profits margin is being consumed by their broad marketing costs and customer acquisition costs (CAC). 
This is why we will perform an analysis of the EVs, registered (between 2020 and 2021) to circulate in Washington State, with the goal of determining areas in which
to deploy brand tailored marketing campaigns and billboards, thus **reducing in at least** a 10% their associated CAC. 

As a step further for this project, using clustering to create segmentation within the clients, and offer them an improved and more personalized service. 

As non-technical **measure of success** for this project, we will evaluate the average of the CAC after 6 months of the implementation of the project, and it will be compared against
the first six months of the company CAC. 

For a technical evaluation of the clustering algorithm performance, the first step would be to qualitatively evaluate the clusters the model has created, to determine
if the results are meaningful. Further exploring will imply calculating the *Silhouette score* to determine how alike or different the clusters are, as well 
as using the Variance Ratio Criterion (which is defined as the ratio within-cluster dispersion and between-clusters dispersion). 

The risks of this implementation would be:
* By trying to better serve the most popular brands of vehicles, we could be missing out in the opportunities the smaller niche could provide.  
* By having to create too many different designs for Ads, we may defeat the purpose of the increase in revenue from targeted billboards. 
* Rapid changes in the market can cause our clusters to be outdated.

Assumptions are:
* EV owners are actually living in their registered addresses. 
* People would rather to mainly charge their EVs at home instead of using public stations.
* We can measure the success of the project withouth using a 'control group', instead, we would rely on historic data from the company. 
* It is possible to create meaningful groups within the totality of clients, by using publicly available and/or internal data. 



## Design

In order to fulfill the requirements of this project, the main goal was to clearly understand the market share of different EV makers, using the zip code feature of our data to delimitate regions in which one particular maker would be the biggest player, thus, we could tailored our marketing approach accordingly. 

## Data

Main sources of data for this project:
- [Electric Vehicle title and registrations data - Washington State](https://data.wa.gov/Transportation/Electric-Vehicle-Title-and-Registration-Activity/rpr4-cgyd)
- [Economic and population - Washington State](https://ofm.wa.gov)

We were able to extract insights from this data sources mainly in an individual fashion, with little to none merging. 

One row from the Electric Vehicle title and registrations data contains: Clean alternative fuel type, model year, make, model, new or used, transaction date, county, city, zip, electric range.  

## Algorithms

* Data Acquisition: Data was mainly obtained in CSV format. 
* Data Exploration: Observation of the data and its characteristics, looking for unexpected values. 
* Data Cleaning: Done mostly initially.
* Data Visualization: This point was key to better understand the data and drive our initial recommendations to the client. 
* Data Clustering: This would be a future implementation. 



## Tools

* Numpy and Pandas for initial data manipulation. 
* Matplotlib and Seaborn for plotting. 
* Google Sheets for exploring and aggregating data. 
* Tableau was used for visualizations. 

## Communication

Submitted PDF slides and 5 minutes presentation. 
