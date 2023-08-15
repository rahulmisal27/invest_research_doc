Setting up investment analysis
=============================

Setting up time series data on a stock
--------------------------------------

- Go to finance.yahoo.com and type in the ticker symbol for Microsoft (MSFT).
- Click on Historical Data and select the time period and frequency you want (e.g., daily data for the last five years).
- Click on Download Data and open the file in Excel.
- The file contains columns for the date, open, high, low, close, and adjusted close prices of Microsoft stock.
- The adjusted close price reflects the dividends paid out by Microsoft over time, while the close price does not.

Computing holding period returns
----------------------------------

- To calculate the 30-day holding period return for a given date, subtract the stock price on that date from the stock price 30 days later, and divide by the stock price on that date.
- To calculate the rolling 30-day returns, drag and drop the formula for the 30-day holding period return to the bottom of the sheet using the fill cell handle.
- To calculate the mean 30-day return, use the average function in Excel and select the range of cells that contain the 30-day returns. This will give you the typical or average 30-day return for Microsoft stock.


Computing time series momentum: Market timing
---------------------------------------------

`Rather than just looking at simple rolling historical returns, investors often want to compare these returns across different securities over time.`

- To understand the risk and returns of a stock over time, you can look at the relative price of the stock compared to its own history.
- To calculate the percentile rank of a rolling 30-day return for a given date, use the RANK.EQ function in Excel to rank that return against all other rolling 30-day returns over a certain period.
- Divide the rank by the total number of returns to get the percentile rank of that return.
- The percentile rank tells you how strong or weak that return is compared to other returns over that period. For example, if a return is in the 80th percentile, it means that it is larger than all but 20% of all other returns over that period.

Compute rolling P/E and P/B multiples for a stock
-------------------------------------------------

`Investors often select stocks based on various valuation multiples, or metrics, like PE ratios, but you want to compute a set of historical ratios for your firm over time to give you a better sense for whether a particular stock is cheap or not. The problem is that these ratios or multiples will change over time as the company changes.`


Building a discounted cash flow model
-------------------------------------

`One of the more sophisticated fundamental valuation methods used by investment pros is called a dividend discount model.` 
`In order to compute that growth rate, we would look at Microsoft's net income at the beginning of our sample period.`
`we can go through and use the geometric mean formula to determine what that growth rate is over time.`
`Finally, we're making assumption about what the discount rate is. Our discount rate is based on the level of risk we think is entailed by Microsoft.`

**Discounted cash flow model formula:**

``DCF = (EPS1 * (1 + g)) / (r - g)``

``DCF = (EPS1 * (1 + g)) / (r - g) + (EPS2 * (1 + g)^2) / (r - g)^2 + ... + (EPSn * (1 + g)^n) / (r - g)^n``

`EPS1 = EPS in year 1`

`EPS2 = EPS in year 2`

`EPSn = EPS in year n`

`g = growth rate`

`r = discount rate`

`EPS = Earnings per share`

`The DCF model is a way of valuing a company based on its future cash flows. The model uses a variety of assumptions about how fast the company will grow, how profitable it will be, and how much cash it will generate. The model then discounts those cash flows back to the present day using a discount rate. The discount rate is a measure of the risk of the company. The higher the risk, the higher the discount rate. The lower the risk, the lower the discount rate.`



Building a dividend discount model
----------------------------------

Another common valuation method used by investment professionals is 

`the DCF or discounted CF, or discounted cash flow model.`

This model uses projections about free cash flow or profitability of the firm to go through and determine the value of the stock on a fundamental basis.  we're going to need to make a few more assumptions. We need to assume a discount rate. This discount rate is the rate of risk in the company. The higher the risk, the higher the discount rate. The lower the risk, the lower the discount rate. We also need to assume a terminal growth rate. This is the rate at which we think the company will grow in perpetuity. Finally, we need to assume a terminal value. This is the value of the company at the end of our projection period.

`That terminal value will be based on Microsoft's 2023 free cash flow, and its growth rate and its discount rate.`

`Then finally, we've got our cash less debt. This is the amount of cash on hand at the company's balance sheet level less the debt it has on hand. We can use all of these pieces to determine our discounted cash flow value.`

**Dividend discount model formula:**

``DCF = (FCF1 * (1 + g)) / (r - g)``

``DCF = (FCF1 * (1 + g)) / (r - g) + (FCF2 * (1 + g)^2) / (r - g)^2 + ... + (FCFn * (1 + g)^n) / (r - g)^n``

`FCF1 = FCF in year 1`

`FCF2 = FCF in year 2`

`FCFn = FCF in year n`

`g = growth rate`

`r = discount rate`

`FCF = Free cash flow`

`Terminal value = FCFn * (1 + g) / (r - g)`

`The DDM model is a way of valuing a company based on its future cash flows. The model uses a variety of assumptions about how fast the company will grow, how profitable it will be, and how much cash it will generate. The model then discounts those cash flows back to the present day using a discount rate. `
