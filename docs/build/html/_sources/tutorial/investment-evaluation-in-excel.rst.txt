Investment Evaluation in Excel
==============================

Computing expected returns on a stock
-------------------------------------

- The text explains how to use Excel to compute expected future returns for a single stock.
- The text assumes that there are five possible scenarios for the stock’s performance over the next year, ranging from losing 10 percent to gaining 30 percent in value.
- The text also requires assigning probabilities to each scenario, which can be based on the investor’s analysis of the company’s prospects.
- The text implies that the expected future return is the weighted average of the returns under each scenario, multiplied by their probabilities.

::
    
    At this point you should be ready to start doing 
    some basic scenario analysis for stocks that you hold.

Using probability to calculate stock returns
--------------------------------------------

Imagine you hold a portfolio with multiple stocks in it. 

::

    Perhaps you're looking for a way to go through and 
    determine what type of return you might expect on that portfolio over time.

- The text explains how to use Excel to calculate the expected return for different stocks based on various scenarios and probabilities.
- The text assumes that the investor has some knowledge of the stocks and their potential outcomes, and can assign probabilities to each scenario.
- The text shows how to use Excel to multiply the rate of return in each scenario by the probability of that scenario, and then sum up the results for each stock.
- The text also suggests that the hardest part of this analysis is not the calculation, but the estimation of the probabilities, which requires some insight into the factors that affect the stocks.
- The text explains how to calculate the expected return on a portfolio of stocks using Excel.
- The text assumes that the investor has already estimated the probabilities and expected returns for each stock based on various scenarios.
- The text shows how to use Excel to calculate the expected return for each stock based on its weight in the portfolio, and then sum up the results for all stocks.
- The text also suggests that Excel can be used to modify the portfolio weights and expected returns over time as new information becomes available.

::
    
    Now you're all set to go through and evaluate your own portfolio 
    and start to think about the scenarios you might encounter, 
    the expected rates of return and the resulting return on your overall portfolio.

Computing arithmetic and geometric returns in a portfolio
---------------------------------------------------------

As an investor, one of the most critical tasks you face is going through and computing performance statistics on your portfolio. 

::
    
    Two common performance statistics you'll probably want to be 
    familiar with are the arithmetic mean and the geometric mean.

use the AVERAGE function by selecting the range of cells that contain the returns of each asset. 

**Now, what does that arithmetic mean indicate or tell us?**

Well what it means is this is the return that an investor could expect on either of these assets in a single ordinary month. So in a typical average month, asset number one will return 1.32%. 

**How does that differ from the geometric mean?**

Well the geometric mean tells us about the average growth rate over time. So, in order to calculate our geometric mean, we're going to need to turn our returns from basic percentages into holding period returns. 

- Take the percentages in Columns B and C, and add one to them for Columns D and E.
- Use the GEOMEAN formula in Excel. Geometric means go through and multiply all of our returns together, and then subtract one off at the end.
- To compute the geometric mean for asset number two, use the GEOMEAN formula, and then select the returns in question and subtract one at the end. The geometric mean for asset number two is 47.7 basis points.
- The geometric mean for asset number one is 118 basis points.
- The geometric mean is the growth rate for a typical month in this particular asset held over time. So if an asset manager tells you that their average return a particular month or year is, say, 5%, you might ask them, are you referring to the geometric mean or the arithmetic mean?12

::
    
    If you're trying to understand how fast your money will grow over time,
    you want to look at the geometric mean. If you're trying to understand what a typical, 
    ordinary single month will look like and whether you'll make or lose money in that month, 
    you want to look at the arithmetic mean. Now you should have a good handle on 
    how you go through and calculate arithmetic and geometric means for your own assets.

Computing standard deviation and variance of an asset
-----------------------------------------------------

In addition to calculating your return statistics, as an investor you'll probably need to go through and calculate different metrics for risk. 

::
    
    There's two different ways that you might calculate risk based on a portfolio.

::
    
    Well variance is really a metric that establishes or computes how spread out our returns are.

So if a stock is up 30% one month and down 30% the next, it will have a high variance. A stock that is consistently returning about the same amount every month, will have a very low variance. 

A related metric to variance is what's called standard deviation. 

::
    
    Standard deviation is simply the square root of variance and standard deviation 
    is important because it's often used in the investment industry as a default measure 
    for the risk of a particular stock or portfolio.

- Variance dot P is based on a large population. Variance dot S, or sample, is used when we only have a subset of the returns. In this case, we want to use variance dot S1.
- The standard deviation can be calculated in a similar fashion. Again we want the standard deviation of the sample rather than the population and for asset two, that’s going to come out to 1.22%.


Sure! Here's a summary of the variance and standard deviation calculation process:

To calculate the variance, we need to do the following:
1. Subtract the expected return from each possible rate of return.
2. Square each of these differences.
3. Multiply each squared difference by its probability.
4. Add up all of these products.

The formula for variance is:

$$\sigma^2 = \sum_{i=1}^{n} p_i (r_i - E(r))^2$$

where:
- $\sigma^2$ is the variance
- $p_i$ is the probability of scenario i
- $r_i$ is the rate of return for scenario i
- $E(r)$ is the expected rate of return

To calculate the standard deviation, we take the square root of the variance.

The formula for standard deviation is:

$$\sigma = \sqrt{\sigma^2}$$


Finding covariances and correlations
------------------------------------

::
    
    A key part of building a portfolio is making sure that the assets that 
    you have in that portfolio provide diversification.

Diversification helps to reduce the risk in that overall portfolio but how do we know if two assets are complimentary to one another?

How do we know if two assets will provide diversification when compared with one another?

 Now what we've got here are return data for two different assets over a period of time throughout the year. We've gone through and calculated the arithmetic means for each. Now what we need to do is go through and determine the covariance of these two assets. 

::
    
    The covariance tells us how much these assets move in sink with one another. 
    A positive covariance means the two assets will tend to move up at the same time.

- The text gives an example of two share classes of Google that have a strong positive covariance and two stocks of different industries that have a negative or zero covariance.
- The text demonstrates how to calculate the covariance of two assets using Excel by subtracting the mean from the return in each month and multiplying them together.
- The text shows how to get the overall covariance by summing up the monthly covariances and dividing by the number of months minus one, which is a statistical adjustment for the sample size.
- The text concludes that the two assets in the example have a negative covariance of -5.06, meaning they tend to move in opposite directions.
- The text explains how to use the Excel covariance and correl formulas to get the same results as the manual calculation.
- The text compares covariance and correlation and says that correlation is more meaningful because it is bounded by -1 and 1, indicating the strength and direction of the relationship between two assets.
- The text shows that the two assets in the example have a high negative correlation of -0.75, meaning they move in opposite directions and provide good diversification.

Computing standard deviation and variance of a portfolio
--------------------------------------------------------

** Variance and standard deviation are two of the most common measures of risk.**

** Formula for variance of a portfolio:**

$$\sigma^2 = \sum_{i=1}^{n} w_i^2 \sigma_i^2 + \sum_{i=1}^{n} \sum_{j=1}^{n} w_i w_j \sigma_i \sigma_j \rho_{ij}$$

where:
- $\sigma^2$ is the variance of the portfolio
- $w_i$ is the weight of asset i in the portfolio
- $\sigma_i^2$ is the variance of asset i
- $\rho_{ij}$ is the correlation between assets i and j

** Formula for standard deviation of a portfolio:**

$$\sigma = \sqrt{\sigma^2}$$

Steps to calculate the standard deviation of a portfolio:
1. Calculate the variance of each asset in the portfolio.
2. Multiply the variance of each asset by its weight in the portfolio.
3. Multiply the covariance of each pair of assets by their weights in the portfolio.
4. Add up all of these products.
5. Take the square root of the result.


Computing beta of an asset
--------------------------

Often times, when you're evaluating a portfolio, you may need to go through and determine what the beta is on a particular asset within that portfolio. 

::
    
    Beta helps us to determine how risky a particular stock is 
    in relation to the market overall, which in turn helps us determine 
    whether or not that stock belongs in our portfolio.


- Add up the value (number of shares multiplied by the share price) of each stock you own and your entire portfolio.
- Based on these values, determine how much you have of each stock as a percentage of the overall portfolio.
- Multiply those percentage figures by the appropriate beta for each stock.
- Add up the weighted beta figures.
- Running the regression of our portfolio of returns against the market returns gives us our beta. 
- That coefficient tells us the relationship between those two groups, the market versus our portfolio. That's two different ways to calculate beta on your portfolio versus the market overall.

Computing risk for a portfolio with many stocks
------------------------------------------------

 we'll go through and compute the mean return for this portfolio and finally we'll determine what the variance or risk on the portfolio overall is. So to start with, we have what we call **a variance covariance matrix.** 

This represents all of the pairs of covariances between the different assets in your portfolio. 

variance covariance matrix is a square matrix that has the variance of each asset on the diagonal and the covariances between each pair of assets off the diagonal.


Computing asset allocation
--------------------------
::

    Many investors want to analyze portfolios containing a mixture of stocks and bonds.

::
    
    it's probably a good idea to balance stocks and bonds together.

To calculate the expected portfolio returns in Excel, you can use the following formula:

::
    
    Ep = w1E1 + w2E2 + w3E3

where w n refers to the portfolio weight of each asset and E n its expected return1.

You can use this formula to determine the growth rate in stocks or bonds and calculate the portfolio’s overall rate of return using Microsoft Excel.

Computing cross-sectional momentum
----------------------------------

::
    
    Portfolio management requires deciding on how to balance between different investments 
    in a portfolio, and one good way to do that is by looking at security momentum.

::
    
    The point here is that even though we have relatively low correlations between 
    these securities individually, those correlations can change very rapidly over time.

**Steps to compute security momentum:**

1. Calculate the returns for each security over a given period of time.
2. Rank the securities based on their returns.
3. Select the top 10 securities and invest in them.
4. Repeat the process every month.

Computing correlations between stocks
-------------------------------------
::
    
    One way to reduce risk in a portfolio is to hold a 
    broadly diversified set of investments, but to get diversification, 
    you first have to calculate correlations between asset prices.
    Skip this step and you may find that a portfolio is a lot riskier than you thought it was.


Now notice, we cannot use correlations based on prices. We've got to have our correlations run based on our returns. 

::
    
    Diversification works worst when it is needed most. 
    That's an unfortunate reality as an investor, but it's one that 
    you need to be aware of in considering when you build your portfolio.

Evaluating hedge funds and mutual funds with portfolio attribution
-------------------------------------------------------------------

::
    
    More advanced portfolio analysis should take into 
    account factor models like the Fama and French model.


We've also got what are known as factors: 
- the size factor, 
- the value factor, 
- the risk free rate, 
- and the VIX. 
- We've also got our friend beta which is labeled here just market minus risk free. 

Now, what we want to understand is how much of the returns for a hedge fund or a mutual fund are driven by exposure to one of these factors. 
In other words, 
is that hedge fund really picking good stocks or are they just loading up on high beta stocks?

Are they just loading up on stocks that score well on the size, SMV, and the value, HML, factors?

How can we do this type of portfolio attribution analysis as it's called?

Regression analysis is the tool we're going to need. So I'm going to go to the data tab and then click the data analysis button. 

**Steps to perform regression analysis in Python:**

1. Load the data into a Pandas DataFrame.
2. Use the statsmodels.formula.api.ols function to run the regression.
3. Use the summary function to view the results.


Valuing a bond in Excel
-----------------------

Bond valuation can be done quickly and effectively in Excel, let's see how it works. Now let's pretend we have a bond, 
in that bond we've got five different major characteristics we care about and this is true of all bonds in fact. 
- Maturity 
- coupon
- par value 
- the discount rate, or yield on the bond
- and the price of the bond.

Now generally when we're evaluating a bond, we're trying to use some of these characteristics to predict price or the price that we think the bond should trade in. 

``So maturity is simply the length of time until that bond matures, until it's going to be repaid to the investor. 
The coupon is the interest rate we receive on the bond and the par value is the amount of money that we'll get back in the future. All three of those are going to be a given. These let us go through and create a schedule of cash flows which is critical to determining what we think the price or yield should be on that bond. So in this case our cash flows are simply equal to the coupon times the par value. I'm going to use this same formula across all 19 of the first 19 out of 20 years. The cash flow for the bond is always going to be coupon times par value. In my final year I get repaid the par value of the bond, plus I get my five percent coupon. Now I understand that obviously bonds are frequently semi-annual we haven't accounted for that here for simplicity and we also assume that we get paid the coupon and the par value at the same point in time in year 20. Again we're just doing this to kind of abstract away from some of that technical detail. It's going to give us an approximation for what we care about though. So next up we're going to need to pick a discount rate in order to get our price or value on the bond.``

What discount rate should we use? 
Well that's going to depend on the risk of the bond.

- If it's a very safe bond, we might use a low discount rate.
- If it's a very risky bond, we might use a high discount rate.

** Formula to compute present value of a bond:**

$$PV = \sum_{t=1}^{n} \frac{CF_t}{(1 + r)^t}$$

where:
- $PV$ is the present value of the bond
- $CF_t$ is the cash flow in period t
- $r$ is the discount rate
- $n$ is the number of periods

**Steps to calculate the present value of a bond in Python:**

1. Load the data into a Pandas DataFrame.
2. Use the numpy.pv function to calculate the present value of each cash flow.
3. Sum up the present values to get the total present value of the bond.


Performing scenario analysis
----------------------------

::
    
    Oftentimes, investors want to go beyond basic bond analysis,
     and consider how the bond's value will change under various scenarios.

**Steps to perform scenario analysis in Python:**

1. Load the data into a Pandas DataFrame.
2. Use the numpy.pv function to calculate the present value of each cash flow.
3. Sum up the present values to get the total present value of the bond.
4. Change the discount rate to reflect the new scenario.
5. Repeat steps 2 and 3 to calculate the present value of the bond under the new scenario.
