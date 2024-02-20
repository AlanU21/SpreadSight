# Project Charter

## Business Background

* Credit Default Swaps are an insurance policy against a debtor's ability to repay a loan. They played a crucial role in the 2007-2008 Housing Market Crash as Hedge Fund Managers purchased trillions of dollars worth of Swaps against the Housing Market and reaped billions when the bubble burst.
* In the 15 years since, modelling Credit Default Swap Indices has never been more crucial to forecast future credit events.

## Project Scope
* SpreadSight is a Time Series Forecasting model for the two major Credit Default Swap Indexes in the North American Market
  * CDX.NA.IG (Investment Grade)
  * CDX.NA.HY (High Yield)

* The main deliverable will be a deployed forecasting model to Amazon Web Services

## Personnel
* Who are on this project:
	* Temple University:
		* Colby Eigen (Data Science '24)
      * Alan Uthuppan (Computer Science and Data Science '24)
      * Saimon Shrestha (Data Science '24)
  
## Metrics
* The models will be evaluated using the industry standard Financial Forecasting Root Mean Squared Error.

## Plan
* Phase 1: Data Collection
* Phase 2: Data Exploration
* Phase 3: Data Preprocessing
* Phase 4: Local Model Development
* Phase 5: Local Model Evaluation
* Phase 6: Remote Resources Development
* Phase 7: Remote Model Deployment

## Architecture
* Data
  * What data do we expect? Raw data in the customer data sources (e.g. on-prem files, SQL, on-prem Hadoop etc.)
* Data movement from on-prem to Azure using ADF or other data movement tools (Azcopy, EventHub etc.) to move either
  * all the data, 
  * after some pre-aggregation on-prem,
  * Sampled data enough for modeling 

* What tools and data storage/analytics resources will be used in the solution e.g.,
  * ASA for stream aggregation
  * HDI/Hive/R/Python for feature construction, aggregation and sampling
  * AzureML for modeling and web service operationalization
* How will the score or operationalized web service(s) (RRS and/or BES) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
  * How will the customer use the model results to make decisions
  * Data movement pipeline in production
  * Make a 1 slide diagram showing the end to end data flow and decision architecture
    * If there is a substantial change in the customer's business workflow, make a before/after diagram showing the data flow.

## Communication
* Our team members will communicate through Jira, Discord, and text message to ensure a streamlined workflow.
* These same methods will be used to communicate project updates to our clients, Stephen MacNeil and Jovan Andjelkovic
