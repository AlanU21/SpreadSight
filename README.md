# Project Charter

## Problem Description

* Credit Default Swaps are an insurance policy against a debtor's ability to repay a loan. They played a crucial role in the 2007-2008 Housing Market Crash as Hedge Fund Managers purchased millions of dollars worth of Swaps against the Housing Market and reaped hundreds of millions when the bubble burst.
* A Credit Default Swap Index is a standardized, tradable financial instrument. It is a collection of Credit Default Swaps for varying creditors that has enabled liquidity in the CDS market a standard swap did not.
* In the 15 years since, modelling Credit Default Swap Indices has never been more crucial to forecast future credit events.

## Project Scope
* SpreadSight is a Time Series Forecasting model for the two major Credit Default Swap Indexes in the North American Market
  * CDX.NA.IG (Investment Grade)
  * CDX.NA.HY (High Yield)

* The main deliverable will be a deployed forecasting model using *Serverless Application Model* (SAM) through Amazon Web Services.

* Our client will be delivered a daily forecasting report featuring visualizations of 1 day, 7 day, 30 day, 90 day trends for IG and HY spreads.

  
## Metrics
* The models will be evaluated using the industry standard backtesting strategies for Financial Forecasting: *Root Mean Squared Error, Mean Absolute Error, and Mean Absolute Scaled Error*.


## Architecture
* Data
  * We collected our original dataset from a Bloomberg Terminal at the Temple University Fox School of Business.
  * 

* What tools and data storage/analytics resources will be used in the solution e.g.,
  * ASA for stream aggregation
  * HDI/Hive/R/Python for feature construction, aggregation and sampling
  * AzureML for modeling and web service operationalization
* How will the score or operationalized web service(s) (RRS and/or BES) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
  * How will the customer use the model results to make decisions
  * Data movement pipeline in production
  * Make a 1 slide diagram showing the end to end data flow and decision architecture
    * If there is a substantial change in the customer's business workflow, make a before/after diagram showing the data flow.

## Plan
* Phase 1: **Data Collection**
* Phase 2: **Data Exploration**
* Phase 3: **Data Preprocessing**
* Phase 4: **Local Model Development**
* Phase 5: **Local Model Evaluation**
* Phase 6: **Remote Resources Development**
* Phase 7: **Remote Model Deployment**

## Personnel
* Who are on this project:
	* Temple University:
		* **Project Lead:** Colby Eigen (Data Science '24)
      * **Lead Analyst:** Alan Uthuppan (Computer Science and Data Science '24)
  * Clients
    * Stephen MacNeil
    * Jovan Andeljkovic

## Communication
* For development, we will be implementing our project in Python code using VScode as our IDE and GitHub for version control
* Our team members will communicate through Jira, Discord, and text message to ensure a streamlined workflow.
* These same methods will be used to communicate project updates to our clients, Stephen MacNeil and Jovan Andjelkovic