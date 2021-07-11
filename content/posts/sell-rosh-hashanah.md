+++
title = "Sell Rosh Hashanah, Buy Yom Kippur?"
date = "2014-09-26T09:18:46-06:00"
tags = ["trading"]
+++
With yesterday's 1.6% sell off in the major indices, and the fact that it happened to coincide with the start of Rosh Hashanah, some traders were dredging up the ["Sell Rosh Hashanah, Buy Yom Kippur"](http://www.bespokeinvest.com/thinkbig/2013/9/4/sell-rosh-hashanah-buy-yom-kippur.html) adage to try to the explain the market action.  Like many of these old adages, it's hard to know whether there's any quantitive data that actually supports their use.  Much of the time, even if these strategies did work at some time in the past, they rarely do today.  But there's no way to know without crunching the data, so that's what we did.
<!--more-->

What was found by analyzing data from the S&P 500 index [(SPX)](http://www.bloomberg.com/quote/SPX:IND) from 1950 to 2013, was that there's little evidence to justify the strategy of selling Rosh Hashanah and buying Yom Kippur.  Over that 64 year period, the mean return for that 9 day period was basically zero.  The market didn't tend to go up or down. It was just a random walk.  There was one noticeable outlier in the midst of all this well behaved data, and that was the year 2008.  In that one exceptional year, the SPX was down an amazing 17.8% over those nine days.  But it was a pretty exceptional year for other reasons as well.

<div class="table">
<table class="table table-responsive table-striped">
<thead>
<tr class="header">
<th></th>
<th>1950 to 2013</th>
<th>Excluding 2008</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Maximum</td>
<td>0.058686056</td>
<td>0.0586860556</td>
</tr>
<tr class="even">
<td>3rd Quartile</td>
<td>0.010087528</td>
<td>0.0107616799</td>
</tr>
<tr class="odd">
<td>Mean</td>
<td>-0.003352942</td>
<td>-0.0005871179</td>
</tr>
<tr class="even">
<td>Median</td>
<td>-0.002184052</td>
<td>-0.0012134584</td>
</tr>
<tr class="odd">
<td>1st Quartile</td>
<td>-0.016973419</td>
<td>-0.0154244534</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>-0.177599826</td>
<td>-0.0550011089</td>
</tr>
<tr class="odd">
<td>Std Deviation</td>
<td>0.030481498</td>
<td>0.0211335060</td>
</tr>
<tr class="even">
<td><a href="https://en.wikipedia.org/wiki/Skewness">Skewness</a></td>
<td>-2.793708622</td>
<td>0.1961559384</td>
</tr>
<tr class="odd">
<td><a href="https://en.wikipedia.org/wiki/Kurtosis">Ex. Kurtosis</a></td>
<td>15.016974260</td>
<td>0.3007369142</td>
</tr>
</tbody>
</table>
</div>

A [Q-Q plot](https://en.wikipedia.org/wiki/Q-Q_plot) is a graphical method for comparing a given set of data to a normal distribution. In the plot on the left below, the majority of the data shows a strong correspondence to the normal distribution.  The exception is the data point from 2008 which is highlighted in red in the lower left corner of the plot. In the plot on the right, the outlier from the year 2008 has been removed, better showing how nicely the data corresponds to a normal distribution.

The reason this is important, is that the one data point from 2008 significantly changes the mean, skewness, and kurtosis of the returns.  That one datapoint might lead one to believe that the distribution of returns is highly negatively skewed with long tails.  However, excluding that one year from the other 63 years, shows a significantly different situation.  If fact, the overwhelming majority of data points show the mean, skewness, and kurtosis to be very close to zero, if not slightly positive.

<a href="/images/2014/rh2yk.png"><img src="/images/2014/rh2yk.png" alt="Rosh Hashanah to Yom Kippur" title="Rosh Hashanah to Yom Kippur" height="50%" width="50%"><a/><a href="/images/2014/rh2yk-outlier.png"><img src="/images/2014/rh2yk-outlier.png" alt="Rosh Hashanah to Yom Kippur" title="Rosh Hashanah to Yom Kippur" height="50%" width="50%"><a/>
