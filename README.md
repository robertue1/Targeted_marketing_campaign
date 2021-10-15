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

In order to fulfill the requirements of this project, after performing EDA and creating visualizations, we were able to tackle 



To reach the prediction goal of this project, we decided to analyze features like budget, runtime, MPPA rating, the distributor, and the genres a movie belongs to.
Since there were categorical non-ordinal features, the implementation of dummy variables was needed. Once different models' performances were compared, 
we chose Lasso as the tool for making predictions and to determine which factors have positive or negative correlations with the target. 

## Data

Main sources of data for this project:
- [BoxOfficeMojo](http://boxofficemojo.com/)
- [Wikipedia](https://en.wikipedia.org/wiki/Main_Page)

From BoxOfficeMojo we were able to extract the bulk of the data, but, as it is almost always the case, data was missing. That is why, Wikipedia was used 
to impute the missing values. 

One row of data for this project holds: Title, domestic opening, domestic lifetime gross, worldwide lifetime gross, budget, duration, release date, 
distributor, and genre for each one of the movies. 

## Algorithms

* Data Acquisition: Data was mainly obtained in CSV format. 
* Data Exploration: Observation of the data and its characteristics, looking for missing or unexpected values. 
* Data Cleaning: Done initially.
* Data Transformation: Creating dummy variables for the categorical non-ordinal features and standardization of the numeric ones for use in the regularized models.
* Data Visualization: Studying the performance of the models via graphs. 


## Models

Linear and Polynomial regression, Ridge and Lasso. 

Model Evaluation and Selection

Initially, a simple train/validation/test was used for the selection of the model, but then, we used a more rigorous Cross-Validation scheme. 
The best performing model was used, but due to the magnitude of features we were considering, a Lasso implementation was done to make the predictions. 


## Tools

* BeautifulSoup and Selenium for web-scraping (data acquisition)
* Numpy and Pandas for data manipulation
* Scikit-learn for modeling
* Matplotlib and Seaborn for plotting

## Communication

Submitted PDF slides and 5 minutes presentation. 
