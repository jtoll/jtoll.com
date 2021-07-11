+++
title = "Volatility of VIX"
date = "2014-10-13T17:44:37-06:00"
tags = ["trading", "volatility"]
+++
The S&P 500 index [(SPX)](http://www.bloomberg.com/quote/SPX:IND) has been down five of the past six trading sessions and along with that has come a significant increase in the [VIX](http://www.bloomberg.com/quote/VIX:IND) implied volatility index.  But the most interesting aspect of the selloff is not the current level of the VIX, but the size of the increase and the speed with which it's taken place, or in other words, the volatility of implied volatility.

<!--more-->
<a href="/images/2014/vix-20141013.png"><img src="/images/2014/vix-20141013.png" alt="VIX [2014]" title="VIX [2014]" height="100%" width="100%"></a>

Over the past six days, the VIX has moved from 14.55 to 24.64 and is now 4.033&sigma; above its 50-day SMA.  If the daily returns for the VIX followed a normal distribution one would expect a move of this size to happen extremely infrequently.  But in fact, the distribution of returns for the VIX varies quite a bit from a normal distribution, exhibiting a positive [skewness](https://en.wikipedia.org/wiki/Skewness) of 0.7242861 and a fairly significant [excess kurtosis](https://en.wikipedia.org/wiki/Kurtosis) of 3.854248.  This [Q-Q plot](https://en.wikipedia.org/wiki/Q-Q_plot) quickly shows the deviation of the distribution of VIX returns from the normal distribution.  The areas on either end, where it deviates from the diagonal line, depict the long tails associated with excess kurtosis.

<a href="/images/2014/vix-qqline-20141013.png"><img src="/images/2014/vix-qqline-20141013.png" alt="VIX Q-Q plot" title="VIX Q-Q plot" height="100%" width="100%"></a>

While still rare to see the VIX over 4&sigma;<sup>1</sup> above its 50-day SMA (it has only happened 9 times since 2007), it's not quite as rare as normally expected.  From a qualitative standpoint, this strong move upward in the VIX from rather anemic levels appears to imply a real concern that recent market weakness might translate into a return to higher average levels of market volatility.

<div class="table">
<table class="table table-responsive table-striped">
<thead>
<tr class="header">
<th>Date</th>
<th>VIX</th>
<th>SMA</th>
<th>Standard Deviation</th>
<th>Score</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>2007-06-07</td>
<td>17.06</td>
<td>13.3520</td>
<td>0.8958248</td>
<td>4.139202</td>
</tr>
<tr class="even">
<td>2007-07-27</td>
<td>24.17</td>
<td>15.3064</td>
<td>2.1814185</td>
<td>4.063228</td>
</tr>
<tr class="odd">
<td>2010-05-06</td>
<td>32.80</td>
<td>18.3180</td>
<td>2.9121554</td>
<td>4.972949</td>
</tr>
<tr class="even">
<td>2010-05-07</td>
<td>40.95</td>
<td>18.7350</td>
<td>4.3233803</td>
<td>5.138340</td>
</tr>
<tr class="odd">
<td>2011-03-16</td>
<td>29.40</td>
<td>18.3332</td>
<td>2.6252381</td>
<td>4.215541</td>
</tr>
<tr class="even">
<td>2011-08-04</td>
<td>31.66</td>
<td>19.4800</td>
<td>3.0122505</td>
<td>4.043488</td>
</tr>
<tr class="odd">
<td>2011-08-08</td>
<td>48.00</td>
<td>20.4168</td>
<td>5.2558420</td>
<td>5.248103</td>
</tr>
<tr class="even">
<td>2014-07-31</td>
<td>16.95</td>
<td>11.8870</td>
<td>1.0645786</td>
<td>4.755873</td>
</tr>
<tr class="odd">
<td>2014-10-13</td>
<td>24.64</td>
<td>14.1808</td>
<td>2.5934461</td>
<td>4.032935</td>
</tr>
</tbody>
</table>
</div>


<small><strong>Footnote:</strong>  
<sup>1</sup> [Chebyshev's inequality](https://en.wikipedia.org/wiki/Chebyshev%27s_inequality#Probabilistic_statement) provides a bound on the likelihood of observations greater than 4&sigma; from the mean.
</small>
