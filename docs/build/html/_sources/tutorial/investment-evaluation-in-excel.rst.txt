Investment Evaluation in Excel
==============================

Computing expected returns on a stock
-------------------------------------

Computing expected future returns is a key task but a difficult one. But investors can make this process a little bit easier using Excel. Let me show you what I mean. I'm in in the 03_01_Begin Excel file. 

Now, let's pretend you hold a single stock and you've gone through and analyzed the company's prospects, and you think there's five possible scenarios that could occur. 

- Under scenario one, the firm loses 10 percent of its value over the next year. 
- Under scenario two, the firm gains one percent in value. 
- In scenario three, the firm gains 10 percent in value. 
- Scenario four, the firm gains 20 percent. 
- And scenario five, the firm gains 30 percent. 

Now these are just kind of made up numbers. Obviously, the rate of return would vary based on what's going on with the company itself. Some companies have really strong prospects, other companies don't. But we can go through and we can think about any stock on this basis. What could happen to the firm and what's the expected outcome if that does happen? Is the stock going to up or down and by how much? We can kind of ballpark it, and if our number is wrong, that's okay. It's probably in the right ballpark. From there, we have to determine the probability of any of these particular events. Now, in this case, I have assigned probabilities ranging from the most probable event, a 10 percent downturn in the stock, to the least probable event, a five percent chance of a 30 percent upside. The key here is we have to make sure that these probabilities all sum to one or 100 percent. Next, we're going to go through and figure out, based on these probabilities, what is our expected return? To do this we just multiply the rate of return in each scenario by the probability of that scenario. And we can do that for all five of our scenarios. Then, in order to figure out the expected return on the stock overall, we simply sum up these five different outcomes. So in this particular case, this stock has a total expected return, based on these scenarios, of 3.25 percent. The nice thing about doing this in Excel is that could go through and alter these. Let's pretend that the company comes out and reports better than expected earnings. Maybe that decreases the likelihood of that downside event and increases the likelihood of some of the upside events for the firm. Well now our expected total return has risen to 5.75 percent. So Excel lets us go through and do some pretty nice modeling when we're trying to think about what might happen to the firm and what's the expected returns overall. 

::
    
    At this point you should be ready to start doing 
    some basic scenario analysis for stocks that you hold.

Using probability to calculate stock returns
--------------------------------------------

Imagine you hold a portfolio with multiple stocks in it. 

::

    Perhaps you're looking for a way to go through and 
    determine what type of return you might expect on that portfolio over time.

How can you do this? Well, Excel can help. Let me show you what I mean. I'm in the zero, three, zero, two begin Excel file. Now let's imagine that you have three different stocks. Stock A, stock B, and stock C. Based on your knowledge of each of these stocks, you've come up with different scenarios for each company, and probabilities associated with each of those scenarios. And from there, you've determined the expected rate of return based on each scenario, and then for the stock as a whole. Now the reality is that when it comes to doing this type of analysis, the hard part is not actually figuring out what the rates of return are. The hard part is that first column, column A. In my experience, the tough part of investments is figuring out the probability of various events happening. We all know as a example that if Facebook has another data breach or if Google has a problem with China or if Amazon runs into new competition from foreign competitors, the stock is going to go down. 

The question is, what are the probabilities of those events? So studying those probabilities and coming up with this first column is going to consume the bulk of your time, but once you've done that, how do you get to an expected return on the portfolio? 

Well, you'll through and determine the rate of return on each stock and then from there, you'll need to determine the weight of each stock within your portfolio. So in this particular case, we have 30% of our portfolio invested in stock number one, 50% of our portfolio invested in stock number two, and 20% of our portfolio invested in stock number three, and the expected returns on these stocks are just derived directly from our probabilities and our scenarios. 

In each case, we've drawn them directly from the calculations we already did, so what's our overall portfolio return? Well, it's just going to be the weight of each of our holdings times the expected return on that stock all summed up. So in this case, this portfolio has an expected return of 8.58%. Now the nice thing about doing this in Excel is we can go through and modify any of these features in order to update our portfolio. So based on this particular scenario, it looks like stock three has the highest expected return. Maybe we would want to increase the weight on that stock to 50% and cut back the weight on stock one and two, accordingly. When we do that, we see that our portfolio return changes from 8.6%, roughly, to about 12.24%. Excel creates a very neat and clean way to go through and not only set up our scenario analysis, but update it over time as we learn more information about any of the firms. 

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

Let me show you how those are computed in Excel. I'm in the 03_03_Begin Excel file. Now, what we have here are two different assets, asset number one, and asset number two, and their returns throughout the year 2019. For asset number one, its returns start off relatively weak. It loses 3.6% in January before bouncing back for several months and then losing more money during the middle of the year. In order to go through and compute the arithmetic mean, we would simply use the AVERAGE function and select all of the numbers in question. Now let's try doing this for asset number two. So in this case, I'm going to use the AVERAGE function, and I'm going to select all of the return statistics that I'm interested in. 

**Now, what does that arithmetic mean indicate or tell us?**

Well what it means is this is the return that an investor could expect on either of these assets in a single ordinary month. So in a typical average month, asset number one will return 1.32%. 

**How does that differ from the geometric mean?**

Well the geometric mean tells us about the average growth rate over time. So, in order to calculate our geometric mean, we're going to need to turn our returns from basic percentages into holding period returns. 

To do that, we'll take the percentages in Columns B and C, and add one to them for Columns D and E. We do that down the entire row. Once we've done that, we're going to need to use the geometric mean formula in Excel. Geometric means go through and multiply all of our returns together, and then subtract one off at the end. So, in order to compute our geometric mean, for asset number two, I'll use the GEOMEAN formula, and then select the returns in question and subtract one at the end. The geometric mean for asset number two is 47.7 basis points. The geometric mean for asset number one is 118 basis points. What does this tell us? This is the growth rate for a typical month in this particular asset held over time. So if an asset manager tells you that their average return a particular month or year is, say, 5%, you might ask them, are you referring to the geometric mean or the arithmetic mean?

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

Let me show you what I'm talking about. I'm in the 03 04 Begin Excel file. Now, we have two different ways to calculate risk in a particular portfolio. Let's focus first on this area in blue over here on the left. We've got a two asset portfolio. Asset number one and asset number two and I've gone through and listed our returns on a monthly basis for each of these two assets. We can use the variance formula in Excel to go through and compute our variance for each of these. Now what is variance you might ask? 

::
    
    Well variance is really a metric that establishes or computes how spread out our returns are.

So if a stock is up 30% one month and down 30% the next, it will have a high variance. A stock that is consistently returning about the same amount every month, will have a very low variance. 

A related metric to variance is what's called standard deviation. 

::
    
    Standard deviation is simply the square root of variance and standard deviation 
    is important because it's often used in the investment industry as a default measure 
    for the risk of a particular stock or portfolio.

So let's go through and try computing the variance and standard deviation for our second asset, shall we? Now in Excel, we've got a couple of different variance formulas. Variance dot P is based on a large population. So if we had a complete history of stock prices we'd use that. In this case we want to use variance dot S, or sample, because we only have a subset of the returns. So our variance on asset number two is 1.48. Our standard deviation can be calculated in a similar fashion. Again we want the standard deviation of the sample rather than the population and for asset two, that's going to come out to 1.22%. Now, that's assuming that we have monthly returns for each of these individual assets but what if we're trying to calculate future expected risk? 


Well in such a scenario, we wouldn't have our monthly returns, would we. So instead, we'd need to come up with scenarios like what you see over here in the green. We have five different scenarios, and the probabilities associated with them as well as the different rates of return associated with these probabilities. Based on that, our expected return on the stock is 3.25%. Now, in order to calculate our expected variance, we're going to need to come through and do the following. We're going to subtract our expected return from our possible rate of return using the columns directly above, see. Column F, we've just taken these possible rates of return, moved to them down below and then we're subtracting from each of those possible rates of return, our expected or average return. From there, we multiply by the probability of that event to get the portion of our variance that this particular scenario makes up. If we do that across all five scenarios, we can then determine our expected variance by summing up all of the variance components. So our variance in this case, is .015. Now in order to get our standard deviation, we're going to take that variance metric, and take the square root of it, which we can do either by raising that value to the one half or taking the square root of the above. Either way, we get a standard deviation of 12.23% which you wouldn't want to do, is go through and try to apply our variance formula here. For one thing, it won't take into account the probabilities of each of these scenarios. Same thing with the standard deviation formula. So in this case because we have scenarios with different weights for the probabilities, we're going to end up with an incorrect variance and standard deviation should we try to use the built-in Excel function. Watch out for this, that's a red flag you want to be aware of as you're calculating your own expected risk statistics.

Finding covariances and correlations
------------------------------------

::
    
    A key part of building a portfolio is making sure that the assets that 
    you have in that portfolio provide diversification.

Diversification helps to reduce the risk in that overall portfolio but how do we know if two assets are complimentary to one another?

How do we know if two assets will provide diversification when compared with one another?


Well, Excel can help us with this and the calculation of what we call correlation and covariance. Let me show you what I'm talking about. I'm in the 0305 begin Excel file. Now what we've got here are return data for two different assets over a period of time throughout the year. We've gone through and calculated the arithmetic means for each. Now what we need to do is go through and determine the covariance of these two assets. 

::
    
    The covariance tells us how much these assets move in sink with one another. 
    A positive covariance means the two assets will tend to move up at the same time.

An extreme example of this would be say, Google class A and class C shares. Two share classes for the same company probably going to rise and fall in sink with one another. They would have a very strong, positive covariance. Two assets in completely different industries, let's say Ford Motor Company and Microsoft Stock, they're much more likely to have a negative covariance or at least a covariance close to zero. So let's see how we calculate these covariances. Well to begin with, we're going to need to, as part of the formula, go through and calculate the return in each month minus the mean for that particular month. So I've done that for you in row two, for columns D and E. What this simply represents is the return in each month minus the mean for that month. 

Now to compute our covariance, we're simply going to multiply the return minus the mean in column D, times the return minus the mean in column E. So in that case, it will simply be D3, times E3 and we can do this for all of the sales, all the way down for all months. In order to get our covariance overall, our single number then the formula's just going to be the sum of these individual monthly covariance components divided by the number of months minus one. So in this case with 12 months in a year, that will be the sum of all these covariances divided by 11. Why do you subtract off one might you ask? Well this is a statistical thing but it's really related to your sample size. So your covariance overall is -5.06. That tells you that these two assets tend to move in opposite directions. 

Now we could actually have skipped some of these steps and gone straight to the Excel covariance formula in this case. The covariance formula let's us go through and evaluate the covariance on two different assets based on their sets of returns. The key is though, that you've got to have equal weighting on these assets across all months. When I do that, I get exactly the same result. Now the other factor that you might consider here, it's great that we got the same result when we did it manually versus with Excel, but neither of these numbers are especially meaningful to me. A covariance of -5.06, is that big or small? Well I don't know. Correlation helps to rectify this problem. The correl formula in Excel, we use very similar to how we did the covariance. The nice thing about correlations are that the smallest possible correlation, the one that would indicate two assets provide maximum diversification of one another, is negative one. The highest possible correlation is positive one, meaning two assets always move in sink with one another. So correlation measures movement in either direction between two assets bounded by negative one on the lower side and positive one on the upper side. In this case, our correlation is -0.75. These two assets tend to move in opposite directions and we can see that if we kind of eyeball it up. In month one, asset one is down, asset two is up. Later on, when asset two is down, asset one is consistently up. So these two assets provide excellent diversification for one another. Now you're ready to go through and check correlation and covariance on your own pairs of assets in a portfolio.

Computing standard deviation and variance of a portfolio
--------------------------------------------------------

We've already seen how to calculate variance and standard deviation on a single asset, but most of the time we're interested in calculating variance and standard deviation on multiple assets, meaning on a portfolio that we're investing in. How do we do that? Let me show you. I'm in the zero three zero six begin Excel file. 

Now, in this case we've gone through and computed our covariances and our correlation for these two stocks, asset number one and asset number two, which have the returns that we see here. In order to get our portfolio variance though, we need to take into account the benefits that the diversification factor between these two stocks provides. So I'm going to need to go through and compute a few more things. I need to determine the arithmetic mean of each of these stocks. We've got it as 1.32 for asset number one. We are going to compute it briefly for asset number two. And that'll ensure that we have the correct covariance between our two assets. Now I need to compute the variance of this particular asset, which I'll just do using the var formula in Excel. And similarly, I'm going to use the standard deviation formula. Now, we could also use standard deviation dot S but if you're using an older version of Excel, STDEV open parentheses is fine as well. Now, once we've done that I need to go through and compute my portfolio variation. How do I do that? 

Well, let me show you. We're going to use the formula here in D20. So our portfolio variance is simply equal to the variance for asset number one times the weight of asset number one all raised to the second power plus the variance of asset number two times the weight of asset number two squared and then plus the covariance between these two terms, between these two assets shown over here, multiplied by each of those weights. When we go through and do that, what do we get? We get a portfolio standard deviation of 3.19%. Now, what's interesting is this tells us the portfolio's standard deviation gives us a metric for how risky this portfolio is. It's the square root of our variance. Maybe we could've taken a shortcut. What if we were just take the average of our standard deviations for these two assets above? Would that give us the same thing? The answer is no. Instead, what this shows is that if we just average the standard deviation of each of the two components, that's going to overstate the standard deviation for the portfolio as a whole, making that portfolio look riskier than it really is. Now you're prepared to go through and determine the portfolio variance on a two-asset portfolio on your own.

Computing beta of an asset
--------------------------

Often times, when you're evaluating a portfolio, you may need to go through and determine what the beta is on a particular asset within that portfolio. 

::
    
    Beta helps us to determine how risky a particular stock is 
    in relation to the market overall, which in turn helps us determine 
    whether or not that stock belongs in our portfolio.

It's a good alternative method versus correlation or covariance, which can be computationally intensive. Let me show you how to determine your beta in Excel and I'm actually going to show you two different methods. I'm in the zero, three, zero, seven begin Excel file. 

Now what we've got here are two different assets and their respective returns for a year on a month-by-month basis. We've also got returns for the market overall. So the first I'm going to need to do in order to calculate my beta is to go through and determine the variance of the market overall. So I'm going to use the VAR dot S formula and now I need to determine the covariance between the market and the asset or portfolio, in this case. So I'm going to look at the market's return versus the portfolio returns. This is going to allow me to get the beta on my portfolio overall. If I wanted to get beta on an individual stock, I would instead go through and use that particular stock's returns, but I'm looking for the beta on the overall portfolio. Now in order to compute my beta, I'm going to go through and divide the covariance of the market and the portfolio by the market's variance overall. And my beta here is 0.35. That tells me that when the market moves up 1%, my portfolio moves up 0.35%. When the market falls 1%, my portfolio only falls 0.35%, so this is a pretty safe portfolio. That's one method for computing beta. Let's see the alternative method. Now a second method for determining beta is to go through and use what we call a regression based on the portfolio returns against the market returns. To do that, I need a special add in for Microsoft Excel. I can get that and find it under the data tab. If we don't have this add in, I'm going to come to file, options, add ins, come down to manage Excel add ins and click go, and then I'm going to make sure that the analysis ToolPak is checked. And this will add the data analysis option for Excel. Great, so now I'm ready to run my regression and look at the second method for determining beta. I'm going to scroll down after clicking on data analysis until I get to regression, click okay, and my Y inputs here are going to be my portfolio returns and my X inputs will be my market returns. And I just want to make sure that I'm consistent between the two so they encompass the same number of rows. And I'm going to check labels to make my regression a little bit easier to read, and I'm going to click my output range. And I want it to output onto the same sheet. And then I'm going to click okay, and let's see what happens. When I do this, I can scroll down and it's going to show me a number of metrics here, and if I just clean this up a little bit by highlighting those numbers, clicking control one and then changing these to a two decimal place number, what I see is that the coefficient on market return is 0.35. That's another name for beta. Running the regression of our portfolio of returns against the market returns gives us our beta. That coefficient tells us the relationship between those two groups, the market versus our portfolio. That's two different ways to calculate beta on your portfolio versus the market overall.

Computing risk for a portfolio with many stocks
------------------------------------------------

When dealing with a portfolio with more than two assets it's trickier to compute variance, but Excel can still help you with just a few extra steps. I'm in the 03 08 begin Excel file. Now, there's a lot here so we're going to take it step by step. First I'm going to talk about what the different pieces are, then we'll go through and compute the mean return for this portfolio and finally we'll determine what the variance or risk on the portfolio overall is. So to start with, we have what we call **a variance covariance matrix.** 

This represents all of the pairs of covariances between the different assets in your portfolio. 


The covariance on Apple versus Microsoft, on Apple and General Mills, Microsoft and Caterpillar, et cetera. There's six of them for this single portfolio with four assets in it. We also have our returns for these four assets listed down below, and then the weights which represent our investment holdings in each of these four assets. Now, in order to compute the mean return we could go through and multiply each return by the weight. That's not very efficient to do, especially if we had say a 40 asset portfolio. So alternatively we're going to use a little bit of what's called matrix algebra. I'm going to use the MMULT function and in order to use MMLUT, I'm simply going to highlight my returns and then highlight my weights, and hit enter, and this tells me the mean return on this portfolio is 16.6%. Obviously the higher the return, the happier we are. Similarly, I need to go through and compute my variance, or my risk on the portfolio. We want our variance to be as low as possible. Now, that's where this big formula over here on the right comes in. This formula says that we're going to have to multiply our weights shown here, but as a row, against our variance covariance matrix and then times our weight again, but this time as a column. To do that I'm going to use the MMULT function but I have two different multiplications to do. Weight times covariance matrix, plus covariance matrix times weight. So in this case I'm using two different MMULT functions and my weights currently are not a row as they need to be but they're a column, so I'm using transpose to turn them from a column into a row. Once that's done I'll highlight my variance covariance matrix, then close up that matrix algebra formula and now I'm ready to multiply by my weights one more time, and if I click enter Excel's not going to like it. Excel doesn't do well with multiple sets of MMULT functions embedded with one another. That type of matrix algebra's tough for it, so instead we're going to need to hit shift, control, and enter all at the same time, and when we do that our variance pops up and it's 0.299 and our standard deviation on the portfolio is 0.55. The lower the standard deviation, the happier we are. The higher the return, the happier we are. Now you can go through and compute returns and standard deviation for your portfolio, whether you have four assets or 44 or 444.

Computing asset allocation
--------------------------
::

    Many investors want to analyze portfolios containing a mixture of stocks and bonds.


This is easily done in Excel. I'm in the zero, four, zero, one begin Excel file. Now what we have here are returns for stocks and bonds over the last 90 or so years. We've got data on stock returns from 1928 through 2018 and data on treasury bond returns for that same period. If you'd invested $100 in stocks in 1928, January, and reinvested all of your dividends, by the time we got to 2018, assuming no taxes, of course, you'd have $382850. In treasury bonds, if you'd invested $100 in January 1928, by the time we got to 2018, you'd have $7308. So treasury bonds, obviously, result in a lot less return, but they're much more stable. Stocks seem good over the long run, but there's plenty of years like 1930, 1931 as an example, 1937 or more recently, 2008, 2001, and 2002 where you have hefty negative returns, often times losing 1/3 of your money or more in that single year. For that reason, 

::
    
    it's probably a good idea to balance stocks and bonds together.

So now, we want to determine what the expected portfolio returns looks like. To do that, I've put together this formula that you see here. The rate formula is going to tell us about the growth rate in stocks or bonds. And we're using the starting period value of $100 in stocks and bonds versus the ending period of 383000 and $7300. Now you can certainly copy and paste that formula all the way down, if you'd like, but I'm going to go ahead and recreate it here just so that you see how this is done. So in rate, we need to start with the number of years that we're going to have for our period. In this case, it's 91. If there's any payments along the way, we're reinvesting all dividends, so that's not relevant. The initial investment that we put in, and we've got to put this in as a negative amount because we have a cash outflow. We're investing that money. The future return that we have or the future amount of money that we get, in this case, $383000, and the fact that that money is received at the end of the year. 

Now I'm going to go through and multiply that by the amount that we have in stocks, and that will tell me what my contribution to my overall portfolio return is from stocks. I'll now do the same thing with bonds, but adjusting for the weight in bonds from column I and the bond returns from column E. And that'll let me determine that my portfolio return on a 20-80 mix rather than a 10-90 mix is 5.76%. Now rather than typing this formula in for all 10 of these, I'd certainly rather go down and drag and drop that formula. From there, I'll now be prepared to determine what's my value in five and 10 years? Well, five years in the future, my 90-10 portfolio is worth $12943. 10 years in the future, my 90-10 portfolio is going to be worth, adjusting for the 10-year time frame, $16753. Now what happens if we take these values and expand them all the way down? Well, let's take a look. Now we can see that if we invest the maximum in stocks, five and 10 years down the road, we'll have 15 to 25000 versus only 12 to 17000 five to 10 years down the road. Based on these particular outcomes, we can determine what's the right balance between stocks and bonds for each of us.

Computing cross-sectional momentum
----------------------------------

::
    
    Portfolio management requires deciding on how to balance between different investments 
    in a portfolio, and one good way to do that is by looking at security momentum.

This can be quickly calculated in Excel. I'm in the zero, four, zero, two begin Excel file. Now we have data on five different securities. Microsoft, Apple, JPMorgan, Boeing, and the 30-year treasury bond, and we have pricing data on these from 2014 through 2018. I want to go through and compute 90-day returns that is 90 calendar days or roughly 60 trading days because of course, weekends don't have stocks trading during them. So in order to do that, I'm simply going to look at the final value for Microsoft minus the value from roughly 60 days earlier, 90 calendar days. Now I can apply this same formula across all five of my securities and then down through the entirety of my spreadsheet, or at least until I get to the point where I don't have 90 days of data remaining. So we'll need to limit these values here where we don't have 90 trading days of data. So having erased those, now we've got rolling 90-day historical returns. Doesn't tell me much though, does it? What we want to do instead is go through and assess how strong the performance is for each of these different securities. To do that, I'm going to use the RANK.AVG function. This will let me go through and rank my number, in this case, 9.95% or negative 9.95%, I should say, against the history of Microsoft's previous returns. If I divide that, then, by the total number of returns, this gives me a percentile for Microsoft. So Microsoft's performance, in this case, over the last 90 days, is in the bottom 4%. Only 3% of the time has its 90-day return been worse than for this period. We could apply this same concept across all of our other securities. And then down through our entire spreadsheet. Now once we've done that, something's going to stand out for us. Now notice what happens here. We've got five different securities. Four of them are stocks, one of them is a treasury bond. Notice, all four of the stocks, Boeing, JPMorgan, Apple, and Microsoft tend to do badly at the same points in time. December 2018, a really rough period time for the market. All four of our stocks were in the bottom few percent. You know, say one through 10 terms of their overall percentile. Meaning 90, 95, 99% of the time, they were doing better in past periods than they had been in this period. 

::
    
    The point here is that even though we have relatively low correlations between 
    these securities individually, those correlations can change very rapidly over time.

TLT, the treasury bonds, however, seem to perform in the opposite direction. When stocks were doing very badly, and they were in the bottom few percent, treasury's performance was in the top levels of its percentile. 91% of the time, treasury has done worse than it has at the period ending December 31st, 2018.

Computing correlations between stocks
-------------------------------------
::
    
    One way to reduce risk in a portfolio is to hold a 
    broadly diversified set of investments, but to get diversification, 
    you first have to calculate correlations between asset prices.
    Skip this step and you may find that a portfolio is a lot riskier than you thought it was.

I'm in the zero, four, zero, three begin Excel file. What we've got here are stock prices and 90-day historical returns for five different securities. Microsoft, Apple, JPMorgan, Boeing, and the 30-year treasury bond. We've also go the market's 90-day return over time. Well, what I want to do is go through and calculate my rolling correlations between each of these securities and the treasury bond in order to see how much those move. Then we're going to go through and calculate our correlations versus the market as a whole. So to calculate my correlations, we'll just use the CORREL function. In this case, I'm calculating the correlation between Microsoft and the treasury bond, but if I wanted to calculate the return versus, say, the market, I would just move the relevant column over. Now we've done this across all four of our securities and we're comparing it to TLT, the treasury bond. What happens if we drag and drop this? What do we observe? Well, notice how much variation there is in these correlations. In November 2018, the correlations between each of the different stocks and the treasury bond is low, but generally positive. You know, maybe in the neighborhood of, say, 0.2, 0.3, something like that. By the time we get to December, those correlations have risen dramatically, at least in terms of the absolute value of their magnitude. They are now highly negative. 0.7, 0.8, those types of numbers. So our correlations appear to be highly unstable. Indeed, we'll see the same thing paralleled if we look at the correlations between individual securities and the market as a whole. 


Now notice, we cannot use correlations based on prices. We've got to have our correlations run based on our returns. In this case, we're using 90-day returns, but we could just as easily choose to use 30, 60, 180-day returns. It really depends on what values it is that we are looking for. So in this case, I'm simply going to manually highlight my entire set of returns and I want to compare this to the market as a whole. What happens when I do that? Well, we see Apple has a correlation with the market of 0.77 at the end of the year. Now to make this easier to drag and drop, I'm going to anchor my cells by hitting F4 with the mouse held over the relevant section, and now I'll be able to drag and drop this over to my remaining securities. And the CORREL function should line up exactly. And indeed, it does. Now I can use the fill cell handle to go all the way down to the bottom. Now just for fun, let's go down here and make sure there's none of the errors, which just happens when we have a lack of data points at the bottom because we're just starting out the sample. And what you'll observe, again, is there's a lot of variation in the correlation between different securities. Treasury sometimes has a positive correlation with the market. Other times, it's negative. And the correlation between individual securities and the market as a whole tends to go up in bad times. That's extraordinarily significant. Correlations go to one when the market dives. 

::
    
    Diversification works worst when it is needed most. 
    That's an unfortunate reality as an investor, but it's one that 
    you need to be aware of in considering when you build your portfolio.

Evaluating hedge funds and mutual funds with portfolio attribution
-------------------------------------------------------------------

::
    
    More advanced portfolio analysis should take into 
    account factor models like the Fama and French model.

To do that in Excel, you need to be able to run regressions on a portfolio. Let me show you how this is done. I'm in the 04_04_Begin Excel file. Now what we've got here are returns on a monthly basis for two different hedge funds and two different mutual funds. 

We've also got what are known as factors: 
- the size factor, 
- the value factor, 
- the risk free rate, 
- and the VIX. 
- We've also got our friend beta which is labeled here just market minus risk free. 

Now, what we want to understand is how much of the returns for a hedge fund or a mutual fund are driven by exposure to one of these factors. 
In other words, 
is that hedge fund really picking good stocks or are they just loading up on high beta stocks?\
Are they just loading up on stocks that score well on the size, SMV, and the value, HML, factors?\
How can we do this type of portfolio attribution analysis as it's called?\
Regression analysis is the tool we're going to need. So I'm going to go to the data tab and then click the data analysis button. If you don't have this button, you'll need to come over to file, down to options, add-ins, and then manage Excel add-ins, click go, make sure analysis tool pack is checked for you. Once you do that, you'll be able to get to that data analysis option, scroll down to where it says regression, and click okay. Now, in this case, we want to understand what drive the returns for a particular hedge fund. So I'm going to highlight that hedge fund number one and their returns for the period 1994 through February 2017. We're going to regress this on the factors that we have here: beta, size, value, risk free rate, and VIX as a measure of financial uncertainty. So I'll highlight all five of those columns, all the way down to the 279th row. I'm going to click labels to make this easier to read and then, I'm going to put this into a new worksheet since we'll run the model multiple times. And what do we get? Well, let's clean up the output a little bit and make it easier to read. So I'm going to highlight these numbers down here, change them into two decimal places, drop these last two columns as they're redundant, and then widen some things out so that we can read them a little bit more easily. And, what this shows us, again, changing my numbers to two decimal places, is that 45% of the returns for this particular hedge fund can be attributed to these factors. In particular, the hedge fund seems to be loading up on beta, size, and the risk free rate as factors. We can see that because those particular factors have very high T statistics. At this point, you should be all set to do a regression on your own involving basic attribution analysis.

Valuing a bond in Excel
-----------------------


Bond valuation can be done quickly and effectively in Excel, let's see how it works. I'm in the 04_05 Begin Excel file. Now let's pretend we have a bond, 
in that bond we've got five different major characteristics we care about and this is true of all bonds in fact. ---- --- Maturity, 
- coupon, 
- par value, 
- the discount rate, or yield on the bond, 
- and the price. 

Now generally when we're evaluating a bond, we're trying to use some of these characteristics to predict price or the price that we think the bond should trade in. 

``So maturity is simply the length of time until that bond matures, until it's going to be repaid to the investor. The coupon is the interest rate we receive on the bond and the par value is the amount of money that we'll get back in the future. All three of those are going to be a given. These let us go through and create a schedule of cash flows which is critical to determining what we think the price or yield should be on that bond. So in this case our cash flows are simply equal to the coupon times the par value. I'm going to use this same formula across all 19 of the first 19 out of 20 years. The cash flow for the bond is always going to be coupon times par value. In my final year I get repaid the par value of the bond, plus I get my five percent coupon. Now I understand that obviously bonds are frequently semi-annual we haven't accounted for that here for simplicity and we also assume that we get paid the coupon and the par value at the same point in time in year 20. Again we're just doing this to kind of abstract away from some of that technical detail. It's going to give us an approximation for what we care about though. So next up we're going to need to pick a discount rate in order to get our price or value on the bond.``

What discount rate should we use? Well that's going to depend on the risk of the bond. In this case I'm going to use seven percent. Depending on how risky the bond is, maybe eight or nine should be used, maybe four or five should be used. It really depends on the bond in question. From here we're ready to go through and determine what that bond is worth and to do that I'm going to use the present value formula. So the present value formula requires that I start with my discount rate and then the number of periods in question, the payment that I'll receive during each of those periods, the future value of that particular bond, which is 1000 and then when those payments are received. Once we do all that, the bond is going to be worth according to Excel $788.12. That's how much we should be willing to pay that's the cash outflow for this bond that will then pay us $50 every year plus $1050 at the end. At this point you should be all set to do basic bond valuation all on your own.

Performing scenario analysis
----------------------------

::
    
    Oftentimes, investors want to go beyond basic bond analysis,
     and consider how the bond's value will change under various scenarios.

This can be done easily with Excel. I'm in the 04_06_Begin Excel file. Now, we had a 7% discount rate on this bond and resulting price of $788.12. But what happens if that discount rate changes? What happens as an example if, say the market becomes more concerned about this company and risk rises? If we raise that discount rate to 9%, the value of that bond drops from $788 to $634. On the other hand, if the bond becomes safer and the new discount rate is 4%, now the bond's value rises to $1135.90. What would cause these kinds of discount rates to change? Well, it could be due to idiosyncratic factors related to the company specifically. But, what's more often the case is that the fed raises or lowers rates. So if we're at a 4% rate and the fed lowers rates by 50 basis points, that might lower the discount rate on the bond to only three and a half percent. We can use Excel to quickly and conveniently assess how that'll impact the value of this particular bond. In this kind of case, you want to make sure that you've got the right number of decimal places, of course. 

We could also go through and model how an extension of the bond might impact its value. So, perhaps rather than being a 20-year bond, it's now going to be extended to be a 25-year bond due to a bond restructuring or something similar. What happens to value? With a 25-year bond at a 5% rate, but only a 3.5% discount rate, the value goes up. If that discount rate were again seven, the value falls to $766.93 versus the original $788.12. Finally, let's pretend that we're concerned the bond may not pay back the full amount. Maybe the company is distressed and so it's only going to pay 90 cents on the dollar. What happens to the bond's value in this context? The value drops to $709.31. As you can see, Excel is great for changing those key bond characteristics, and examining how it impacts valuation.