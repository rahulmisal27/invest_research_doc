Portfolio Performance Evaluation
===============================

Setting up allocations
----------------------

..
    
    ``Portfolio management requires understanding the needs of clients and trying to help them to maintain target allocations.``

Let me show you why this can be harder than it sounds. I'm in the 05_01_Begin Excel file. Now what we have here is a pretty basic portfolio. Three stocks, two bonds, total value in January 2018, $555,000. Throughout the year, the stock portfolio, stock and bond portfolio I should say, mostly stays the same value. At the end of the year, it's worth just under 555,000. But, certain stocks within this portfolio rise or fall dramatically. Stock A goes up a little bit, Stock B goes down some, Stock C goes down some. And then Bond A goes up in value, Bond B stays pretty much static. So, what's the allocation or waiting that we have to each of these different investments? Well we can go through and compute this in Excel pretty easily. We simply take the holdings for each particular investment divided by our total value in January, and then drag and drop this down, and we can do the same thing in December. And voila, this tells us how, even without any trading whatsoever, the allocation changed across these different holdings over the course of the year. So we went from an 18% holding to a 19% holding in, say, Stock A. What was our target there? Maybe our target in Stock A was 18%, Stock B 28, Stock C 22, Bond A was 12, and Bond B was 20. These are arbitrary figures of course, but they're reasonably realistic, and this is the type of approach that an investor might use. Well, based on this, investors might need to make a buy-or-sell decision on each of these individual securities. So we can use Excel to go through and determine which we need to buy and sell based on a simple IF function. If we are below our target at the end of the year, we need to buy more of that stock. If we are above target, we should sell. So in the case of Stock A, we need to sell some of that and use the money to buy B and C, as an example. Similarly, we need to sell Bond A and buy a little bit of Bond B. The reason this is important is that it's a key part of what we call rebalancing. And this helps us to use some of our stock gains to fund greater investment into those stocks that were falling behind, which in turn can help to ensure we keep a diversified portfolio that doesn't get too heavily-weighted towards a single security over time.

Scenario analysis in a portfolio
--------------------------------

..
    
    ``One common challenge that investors often face, is figuring out how to assess the expected return, for their investments under a variety of different scenarios.``

Excel can be very helpful with this. I'm in the 05_02_Begin Excel file. Now what we have here are five different investments, ranging from Ali Baba, to Bond B. So it's a series of stocks and bonds. And we have outlined three different scenarios, and the returns and probabilities of those scenarios. From here, we'd like to go though and figure out what the expected returns are, for each of these different investments. To do that, I'm going to multiply the probability, of each scenario, times the expected return in that scenario, and do this for all three of my scenarios being careful to anchor my probabilities for my scenarios along the way, so that I can easily apply this across the entire portfolio. So we're going to anchor cells, G9, F9, and H9, and multiply by the associated returns above. And when we do, we see that Ali Baba's expected return, across those three different scenarios is 7.5%. I can then go through and apply this to the rest of the portfolio, to determine the expected return for any of those different investments. The nice thing about doing this in Excel, is that if we choose to go through and modify the probability of any of these scenarios occurring, Excel will dynamically update. And that's particularly important, because often it's not necessarily as hard to figure out the return for a stock under a scenario, as it is to actually figure out the probability or likelihood of that scenario. For instance, we can all expect that many big companies will do well if the economy grows rapidly. The question is, what's the probability of the economy growing rapidly? So Excel's dynamic features, allow us to update our expected returns over time, as we get new information. Now you're all set to apply this type of scenario analysis to your own portfolio.

Computing expected risk on a portfolio
--------------------------------------

..
    
    ``One key factor that all investors care about, is the expected returns on their portfolio, especially under conditions like economic recessions or economic expansions. How much can I expect to earn, on average, over time?``

Excel's helpful for answering this question when we're considering the uncertainties that investors face daily. I'm in the zero five zero three begin Excel file. Now what we have here are three different Chinese stocks, Alibaba, Tencent, and JD.com, along with two bonds. We've also got their expected returns based on various economic scenarios. How much will I expect to earn on this portfolio overall? Well, in order to determine that, I simply need to take the weight that I have, or the allocation that I have to each holding and multiply it by the expected return on each of those different securities. This process is a good way to get a handle on what we might expect to happen to our portfolio under various economic conditions. So all we're going to do is go through and multiply each return by the allocation that we have for each security. And when we get all done, voila, we have our expected return. Now I'm just going to clean this up by removing the large number of decimal places that have populated, I'm going to hit control, and then the one key, and change the number of decimal places here from 15 to two, and we see that we have an expected return of 8.57%. We could go through and change this if we see bad economic data coming in, then maybe as an example our probability of a recession rises from 30% to 50% and we see the expected return on the portfolio fall from 8 and a half percent to 4.33%. Now you're ready to evaluate your portfolio based on the expected returns and the scenarios you're dealing with.

Computing portfolio Sharpe ratios
---------------------------------

..
    
    ``One of the most common tools that's used in valuating a portfolio is what's called the Sharpe ratio. Sharpe ratio, in essence, lets us go through and examine whether a portfolio is adding value relative to the level of risk it's taking on.`` 

I'm in the 05_04_Begin Excel file. 

..
    
    ``Now the Sharpe ratio is simply the return of the portfolio, minus the risk-free rate, all divided by the standard deviation.``

In essence, it's a metric which tells us are we adding value over and above the risk-free rate relative to the level of risk we're taking on. Higher Sharpe ratios are better. In order to calculate this in Excel, we're simply going to go through and create a new column labeled Rp minus Rf. Now the return on the portfolio Rp is here in collum B, so I'm going to take the collum B metic, minus the risk-free rate, and we're going to extend this across the entire 12 month timeframe. Now in order to calculate our Sharpe ratio, we're going to use the average of these 12 months, divided by the standard deviation for that 12 month period, and there's one more thing we need to do. Now since we're using monthly returns, and we're interested in analyzed Sharpe ratio, because that's how it's traditionally computed, we need to take that Sharpe ratio figure and analyze it. To do that, we're going to multiply by the square root of 12 because there are 12 months in a year. So our formula's going to be the square root of 12, times our average monthly return for Rp minus Rf, divided by the standard deviation for that set of monthly returns. When we get done, we have a Sharpe ratio of 0.85. This tells us that the fund is doing a relatively good job of adding value relative to the risk it's taking on. The higher the Sharpe ratio, the happier we are. Sharpe ratio gives us a really effective tool for making an apples-to-apples comparison that takes into account risk between different portfolio managers. Now you're all set to prepare Sharpe ratios for your own portfolio.

Computing information ratios
----------------------------

..
    
    ``Another common performance metric used in portfolio analysis is the information ratio. The information ratio, unlike the sharp ratio, allows us to go through and capture the difference between a portfolio manager's performance versus the market.``

I'm in the zero five zero five begin Excel file. Now what we have here are portfolio returns for January 2019 through December 2019. And we have our portfolio returns in column B, and then our market returns in column C, and our risk free rate in column D. From the point of view of the sharp ratio, what we're evaluating is how well a portfolio delivers returns versus the risk free rate. The information ratio goes a little bit deeper, though. It says that wait a minute, rather than using an active manager and paying fees, an investor might want to consider whether that active manager is adding value against a low cost passive market index. In essence, the information ratio provides a metric that tells us whether or not the portfolio is adding value compared to the market overall. In other words, does that portfolio manager have skill? Now, we can go through and evaluate this based on the formula that you see below. 

..
    
    ``The information ratio is the difference between our portfolio return and our market return, divided by the standard deviation.``

So I'm going to add another column here, RP minus RM, which will simply be our portfolio return, minus the market return all divided by our standard deviation to get the information ratio. So we're going to go through and take the average now of that set of monthly differences between RP and RM and we'll divide it by the standard deviation of that same subsample. Now, there's one more thing that we have to do here. When we're looking at the information ratio, right now we're simply taking monthly returns. But we want an annualized figure, so we're going to need to multiply this by the square root of twelve, as in twelve months in a year, since we're using monthly returns, and this will give us our annualized information ratio. And there we have it. In this case while the fund manager may have positive returns throughout the year on average, one percent per year, in fact compared to the market, the fund manager seems to be under performing. Now you're prepared to go through and evaluate your own portfolio to see whether or not the information ratio indicates effective management or ineffective management.

Computing Sortino ratios
------------------------

..
    
    ``Another common metric you may wish to calculate when analyzing your portfolio is the Sortino Ratio. The Sortino Ratio is really a ratio developed by industry to allow us to examine whether a portfolio is beating some sort of minimum threshold that's needed by the investor in question.``

I'm in the zero five zero six begin Excel file. 

..
    
    ``Now the formula for the Sortino ratio is simply the return on the portfolio minus the MAR, or Minimum Accepted Return divided by our downside standard deviation. Now, the minimum accepted return, or MAR simply is the level of returns that that particular investor needs to get on a regular basis under their investment objectives.``

So as we've set it up here, I've got the return on the portfolio in column B the MAR in column C, and I'm using a 1% per month MAR, and then our risk free rate in column D, and our holding period return in column E. So to start with, in order to calculate my Sortino ratio, I'm going to create a new column, which will be R-P, Return on the Portfolio minus MAR. So over the course of the 12 months in the year, the R-P minus MAR ranges from anywhere from as high as 3.48% in July, to as little as say, minus 3.4%, or minus 5.11% in May and June. So that's the first step in the Sortino Ratio. But the R-P minus MAR has to be divided by our downside standard deviation. Now what is this? Well, because this is an industry formula, and industry creation, it doesn't necessarily have an exact procedure for calculating it as you might expect, but there's two different, kind of commonly used definitions. One approach to calculating the downside standard deviation is to simply go through and only take those returns where they're negative, where return minus MAR is below zero. And then calculate the standard deviation based on that. The other approach is to take all of the positive R-P minus MARs and replace them with zero. So you'd have as an example negative 2.53 in the first month but then zero in the second month. I'm going to choose to go with the former metric, it seems more in the spirit of what the Sortino Ratio's trying to accomplish, which is to say, are we measuring, or are we adjusting for downside risk being taken by that portfolio manager? So to do that, I'm going to create a simple if statement in column G, saying that if R-P minus MAR is less than zero, then we'll report the number, otherwise we report nothing. And I'm going to drag and drop this across the whole column and so we see we have five different months during the year where we have a downside that we'd want to calculate the standard deviation on. So now we're ready to go through and actually compute that Sortino Ratio. So it's going to be the average across all 12 of these months divided by the standard deviation for this set of metrics and then we're going to annualize it by multiplying by the square root of 12. And the purpose is annualizing it and the reason we multiply by the square root of 12 is that we are using monthly returns at present and we really want some sort of an annual number because that's how portfolio reporting is generally done. And there we have the Sortino Ratio. So the Sortino Ratio in this case indicates the fund manager is not meeting the minimum required return on behalf of investors, they're not living up to that minimum accepted return, the MAR that investors need. And that's how you calculate a Sortino Ratio in Excel. Now you're ready to try doing this in your own portfolio.

Calculating Treynor measures
----------------------------

..
    
    ``One final common performed statistic used in portfolio analysis is the Treynor measure.``

Let's see how it works. I'm in the 05 07 begin Excel file. Now what we have here is a portfolio with 12 months of returns on a monthly basis. We also have the market returns and then the risk free rate associated with this particular portfolio. 

..
    
    ``The Treynor measure, which we want to compute is simply the portfolio return minus the risk free rate divided by beta.``

So I've gone through and computed our expected portfolio return based on the monthly holding period returns raised to the 12 months and then subtracting one from it. That tells me that the expected portfolio return, assuming this is a typical ordinary year, is 11.92%. In order to compute my beta, I'm going to take the covariants on the market and the portfolio divided by the variants on the market, giving me a beta of 0.35. And based on my risk free rate, an annualized 0.25% in this case. Now, one thing that's key, I've got to make sure my units are the same between the expected portfolio return and the risk free rate. So I'm going to change this risk free rate to be a percentage by hitting Control and then number one and it's showing the risk free rate as 25%. I don't want that, so instead I'm going to make it 25 basis points. Now, my Treynor measure is going to show me a figure of 11.92 minus 0.25 all divided by our beta of 0.35. We have a Treynor measure here of 0.33. And again, the higher the Treynor measure, the happier we are. 

..
    
    ``A higher Treynor measure indicates either higher portfolio returns, potentially a lower risk free rate, or more likely, a lower beta. So this is really a measure for how well we're avoiding market risk while at the same time generating returns. Now, you should be able to understand and evaluate the performance of your own portfolio based on the Treynor measure.``

Calculating VaR
---------------

Since the financial crisis in 2008, one critical feature in a lot of investment portfolios is risk management. The ability to understand what our risks are so that we can manage those risks is an area of increasing importance for financial managers and investors these days. I'm in the 05_08_Begin file. 

..
    
    ``Now, the key metric that we use for managing risk in most cases is what's called VAR or value at risk. Value at risk just tells us what is the worst loss that we might suffer under normal circumstances?``

And we typically do this on either what's called a 95% VAR or a 99% VAR basis. And in essence what that means is that if it's a 95% VAR, the loss will only be worse than x amount 5% of the time. If it's a 99% VAR, the loss will only be worse than x 1% of the time. Let me show you how this is calculated. Now believe it or not, in Excel, you actually don't have to have a large sample in order to calculate a VAR. Of course, it's helpful to have more data, right? If we want to understand VAR, the more data we have, the bigger our universe of relevant data is, the better we'll be able to calculate it. But in this case, we just want to understand what our biggest possible loss is under normal conditions. So there's a couple of functions that can help. First, we can simply go through and figure out what our minimum return is. Now I'm using a small subsample of data here. Just 12 months. So it'd be pretty easy to eyeball this but our minimum return during this 12 month period on a monthly basis is negative 4.11% and that occurs in May. If we wanted to compute VAR for this, we'd go through and use the percentile function. Now I'm always inclined to use percentile.inc which just includes all the values in the data set. Alright, so I'm going to go through and copy all of my returns and now I need to pick what percentile I'm looking for. Well in this case, I'm going to start by calculating a 95% VAR so I'm looking for the fifth percentile. Only 5% of the time, will my loss be worse than this. And what we see here is that the 95% VAR is negative 3.17%. Only 5% of the time should our portfolio lose more than 3.17% on a monthly basis given this data. Let's change this to a 99% VAR. Well we can do that very easily by again, using exact the same formula and just changing to 0.01 instead of 0.05. And now we see our VAR is minus 3.92%. Only 1% of the time should we lose more than that. Now notice, 3.92 never appears in this data. Similarly, 3.17 never appears in this data. So Excel is going through and interpreting what our 95 or 99% VARs might be based on the data that is available. That's a nice feature in Excel. Of course the more data we have, the better we'll be able to capture what that VAR truly is. Now you're ready to go through and capture VAR for your own investment portfolio.