# Project Charter

## Business Background

* Credit Default Swaps are an insurance policy against a debtor's ability to repay a loan. An owner of a default swap pays a monthly premium to the creditor while the debtor is paying their loan payments. If the debtor defaults, the owner of the default swap is compensated by the creditor.
* CDS contracts played a crucial role in the 2007-2008 Housing Market Crash as Hedge Fund Managers purchased millions of dollars worth of Swaps against the Housing Market filled with subprime mortgages and reaped hundreds of millions when the bubble burst.
* A Credit Default Swap Index is a standardized, tradable financial instrument. It is a collection of Credit Default Swaps of varying debtors that has enabled liquidity in the CDS market a standard swap lacks.
* In the 15 years since, modelling Credit Default Swap Indices has never been more crucial to forecast future credit events.

## Project Scope
* SpreadSight is a Time Series Forecasting model for the two major Credit Default Swap Indexes in the North American Market
  * CDX.NA.IG (Investment Grade)
  * CDX.NA.HY (High Yield)

* The main deliverable will be a deployed forecasting model using *Serverless Application Model* (SAM) through Amazon Web Services.

* Our client will be delivered a daily forecasting report featuring visualizations of 1 day, 7 day, 30 day trends for IG and HY spreads.

## Personnel
* Who are on this project:
	* Temple University:
		* **Project Lead:** Colby Eigen (Data Science '24)
      * **Lead Analyst:** Alan Uthuppan (Computer Science and Data Science '24)
  * Clients
    * Stephen MacNeil
    * Jovan Andeljkovic
  
## Metrics
* The models will be evaluated using the industry standard backtesting strategies for Financial Forecasting: *Root Mean Squared Error, Mean Absolute Error,* and *Mean Absolute Scaled Error*.

## Plan
* Phase 1: **Data Collection**  
* Phase 2: **Data Exploration** 
* Phase 3: **Data Preprocessing** 
* Phase 4: **Local Model Development** 
* Phase 5: **Local Model Evaluation**  
* Phase 6: **Remote Resources Development**
* Phase 7: **Remote Model Deployment**

## Architecture
* We collected our original dataset from a Bloomberg Terminal at the Temple University Fox School of Business.
* The data includes daily values from August 8, 2012 to February 16, 2024
* We have selected our features based off reviews of prior publications and our desire to combine Merton's Credit Risk Determinants into our Model.
* Potential Models include ARIMA, Seasonal ARIMA, Vector Autoregressive, Ensemble Methods such as Random Forest, and Boosting Methods.
  * *Reccurent Neural Networks will be explored as time permits*
    ___
| **Feature** | **Description** |
|-------------------|-----------------|
| SPX Index      | The Standard & Poor's 500, or S&P 500, is a stock market index measuring the stock performance of 500 large companies listed on U.S. stock exchanges. It's widely regarded as a key gauge of large-cap U.S. equities. |
| VIX Index   | The Volatility Index, or VIX, represents the market's expectations for volatility over the coming 30 days. It is used to gauge the level of fear or stress in the stock market. |
| 30 YR Mort  | The 30-year mortgage rate is the interest rate on a loan to finance the purchase of real estate, typically a home, over 30 years. It's a standard measure of home loan costs in the U.S. |
| 5 YR Mat    | US Treasury interest rate on a five-year government or corporate bond, indicating the investment return from a bond maturing in five years. |
| CDX IG      | The CDX Investment Grade Index is a credit default swap index that tracks the credit risk of a basket of investment-grade corporate bonds, used for hedging or speculating on credit conditions. |
| CDX HY      | The CDX High Yield Index tracks the credit risk of a basket of high-yield bonds, used by investors to manage risk or speculate on the credit conditions of lower-rated corporate bonds. |



## Communication
* Our team members will communicate through Jira, Discord, and text message to ensure a streamlined workflow.
* These same methods will be used to communicate project updates to our clients, Stephen MacNeil and Jovan Andjelkovic
