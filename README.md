# Project Charter

## Problem Description


### Basics
* **Credit Default Swaps** are an insurance policy against a borrower's ability to repay a loan. An owner of a default swap pays a monthly premium to an insurer of the creditor while the borrower is paying their loan payments on time. If the debtor defaults, the owner of the default swap is compensated by the creditor's insurer.
* The video below captures the basics of CDS

[![Credit Default Swaps Explained](https://img.youtube.com/vi/QTXn_FRRcnI/0.jpg)](https://youtu.be/QTXn_FRRcnI)


### CDS in the Housing Market
* CDS contracts played a crucial role in the 2007-2008 Housing Market Crash as Hedge Fund Managers purchased millions of dollars worth of Swaps against the Housing Market filled with *subprime mortgages* and reaped hundreds of millions when the bubble burst visualized below.
  ![alt text](image.png)

  [Source: Credit Default Swap and Its Role in the 2008 Financial Crisis](https://finecoiitg.wordpress.com/2018/08/16/credit-default-swap-and-its-role-in-the-2008-financial-crisis/)

### CDS Index
* A **Credit Default Swap Index** is a standardized, tradable financial instrument. It is a collection of Credit Default Swaps of varying bonds that has enabled liquidity in the CDS market a standard swap lacks.
* In the 15 years since, modelling Credit Default Swap Indices has never been more crucial to forecast future credit events.


## Project Scope
* SpreadSight is a Time Series Forecasting model for the two major Credit Default Swap Indexes in the North American Market
  * CDX.NA.IG (Investment Grade), composed of 125 CDS contracts for low-risk Corporate loans
  * CDX.NA.HY (High Yield), composed of 100 CDS contracts for high-risk Corporate loans

### Main Goals

* The main deliverable will be a deployed forecasting model using *Serverless Application Model* (SAM) through Amazon Web Services using AWS Lambda and S3. See Planned Cloud Architecture for more information.

* Our client will be delivered a daily forecasting report using Amazon Simple Email Service featuring visualizations of 1 day, 7 day, 30 day trends for IG and HY spreads.

* A Tableau Dashboard visualizing our main insights

### Stretch Goals

* A deployed model that scrapes the features daily to forecast on present data

* A Web Interface that allows users to view the most recent data and the forecasted trends on any given day

## Metrics
* The models will be evaluated using the industry standard backtesting strategies for Financial Forecasting: *Root Mean Squared Error, Mean Absolute Error,* and *Mean Absolute Scaled Error*.


## Plan
* Phase 1: **Data Collection** 02/20/24 - 02/22/24
* Phase 2: **Data Exploration** 02/22/24 - 02/28/24
* Phase 3: **Data Preprocessing** 02/28/24 - 03/11/24
* Phase 4: **Local Model Development** 03/11/24 - 03/19/24 
* Phase 5: **Local Model Evaluation** 03/19/24 - 03/20/24
* Phase 6: **Remote Resources Development** 03/20/24 - 4/13/24
* Phase 7: **Remote Model Deployment** 04/13/24 - 04/21/24

## Personnel
* Who are on this project:
	* Temple University:
		* **Project Lead:** Colby Eigen (Data Science '24)
      * **Lead Analyst:** Alan Uthuppan (Computer Science and Data Science '24)
  * Clients
    * Stephen MacNeil
    * Jovan Andeljkovic

## Architecture
* We collected our original dataset from a Bloomberg Terminal at the Temple University Fox School of Business.
* The data includes daily values from August 8, 2012 to February 16, 2024
* We have selected our features based off reviews of prior publications and our desire to combine Merton's Credit Risk Determinants into our Model.
* Potential Models include ARIMA, Seasonal ARIMA, Vector Autoregressive, Ensemble Methods such as Random Forest, and Boosting Methods.
  * *Reccurent Neural Networks will be explored as time permits*

  ### Data Table
| **Feature** | **Description** |
|-------------------|-----------------|
| SPX Index      | The Standard & Poor's 500, or S&P 500, is a stock market index measuring the stock performance of 500 large companies listed on U.S. stock exchanges. It's widely regarded as a key gauge of large-cap U.S. equities, and a factor in Merton's model. |
| VIX Index   | The Volatility Index, or VIX, represents the market's expectations for volatility over the coming 30 days. It is used to gauge the level of fear or stress in the stock market. Although a calculated Volatility for each entity in the IG and HY indices would be superior, it is impossible as many borrowers in each index lack publicly traded options. |
| 30 YR Mort  | The 30-year mortgage rate is the interest rate on a loan to finance the purchase of real estate, typically a home, over 30 years. It's a standard measure of home loan costs in the U.S. It is not explained in Merton's model, but we are using it as a feature because of the direct correlation between Credit Defaults and Mortgage Rates.|
| 5 YR Mat    | US Treasury interest rate on a five-year government or corporate bond, indicating the investment return from a bond maturing in five years. Considered as SPOT interest rate in Merton's model. |
| CDX IG      | The CDX Investment Grade Index is a credit default swap index that tracks the credit risk of a basket of investment-grade corporate bonds, used for hedging or speculating on credit conditions. |
| CDX HY      | The CDX High Yield Index tracks the credit risk of a basket of high-yield bonds, used by investors to manage risk or speculate on the credit conditions of lower-rated corporate bonds. |

### Planned Cloud Architecture

  ![alt text](Architecture1.png)


## Personnel
* Who are on this project:
	* Temple University:
		* **Project Lead:** Colby Eigen (Data Science '24)
      * **Lead Analyst:** Alan Uthuppan (Computer Science and Data Science '24)
      * **Analyst:** Saimon Shrestha (Data Science '24)
  * Clients
    * Stephen MacNeil
    * Jovan Andeljkovic

## Communication
* For development, we will be implementing our project in Python code using VSCode as our IDE and GitHub for version control
* Our team members will communicate through Jira and Discord to ensure a streamlined workflow.
* These same methods will be used to communicate project updates to our clients, Stephen MacNeil and Jovan Andjelkovic