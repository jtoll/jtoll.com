+++
title = "Systematic Scalping: A reference approach to daily gamma scalping"
date = "2015-05-01T15:37:57-06:00"
tags = ["trading", "greeks"]
+++
As a follow-up to my previous article on ["Gamma Scalping Cypress Semiconductor"](/post/gamma-scalping-cy/), I take a look at an alternative approach to gamma scalping.  The initial article elicited many questions regarding the timing or triggers that prompt delta hedging.  In this article I compare our initial, ad lib hedging results with a more systematic strategy that hedges (i.e. neutralizes) the position delta once-a-day at the closing price.  This more systematic approach will serve as a reference to evaluate the efficacy of the ad lib approach to hedging.
<!--more-->

To recap the results from the previous example paper trading in CY, the end result was that after two months of gamma scalping, the position paid for itself, but only made a very small profit.  While there were several opportunities along the way to take a fairly significant profit and close the position, the intention from the outset was to hold the position through to expiration to explore all aspects of the trading process.

Delta hedging is theoretically a continuous process.  In practice, it typically happens far less often.  It's not surprising then that this analysis shows that overall profitability is highly dependent upon the delta hedging strategy employed versus the implied volatility paid for the option position.

The initial long option position was entered into two days prior to an earnings announcement. The timing was purely coincidental, as this was a teaching exercise, but it did provide an interesting set of circumstances to explore the strategy.  Given the timing, I was concerned that volatility and therefore option prices were inflated, meaning that the 0.44 implied volatility would be simply too high of a price.  Ex post, the realized volatility for the two-month period was 0.315, showing that concern was well justified.

The result from the systematic daily hedging strategy was a loss of $2455, considerably worse than the ad lib hedging strategy which managed a slight profit of $133.  Nearly all the blame for that loss can be attributed to simply paying too high of an implied volatility to establish the long option position.  If instead of paying a 0.44 implied volatility, I had paid a 0.315 implied volatility, which matches the realized volatility for that period, the call options would have only cost $0.72 instead of $1.00.  The result from daily hedging at this lower volatility would have then been a net loss of $4, which is basically breakeven.

In summary, what was shown from this ex post analysis is that I was rightly concerned that option prices (i.e. implied volatility) were high prior to earnings.  I also found that for this particular example my original ad lib hedging strategy, which seemed somewhat disappointing in only generating a small profit, actually generated almost $2600 of additional value relative to the reference daily hedging strategy.  In other words, the ad lib hedging compensated for paying over 25% too much for the initial options position.  Simply put, that's a huge win!


<div class="table">
<table class="table table-responsive table-striped">
<caption>Systematic Daily Hedging</caption>
<thead>
<tr class="header">
<th>Date</th>
<th>Price (CY)</th>
<th>Days</th>
<th>Opt. Value</th>
<th>Opt. Delta</th>
<th>Hedge</th>
<th>Daily Adj.</th>
</tr>
</thead>
<tbody>
<tr><td>2015-01-20</td><td>14.01</td><td>59</td><td>1.0026905</td><td>0.5404727</td><td>-5400</td><td>-5400</td></tr>
<tr><td>2015-01-21</td><td>14.16</td><td>58</td><td>1.0769686</td><td>0.5641687</td><td>-5600</td><td>-200</td></tr>
<tr><td>2015-01-22</td><td>14.82</td><td>57</td><td>1.4742268</td><td>0.6639539</td><td>-6600</td><td>-1000</td></tr>
<tr><td>2015-01-23</td><td>15.26</td><td>56</td><td>1.7715120</td><td>0.7241128</td><td>-7200</td><td>-600</td></tr>
<tr><td>2015-01-26</td><td>15.27</td><td>53</td><td>1.7542445</td><td>0.7291968</td><td>-7300</td><td>-100</td></tr>
<tr><td>2015-01-27</td><td>15.17</td><td>52</td><td>1.6735642</td><td>0.7173215</td><td>-7200</td><td>100</td></tr>
<tr><td>2015-01-28</td><td>14.95</td><td>51</td><td>1.5103368</td><td>0.6879020</td><td>-6900</td><td>300</td></tr>
<tr><td>2015-01-29</td><td>15.20</td><td>50</td><td>1.6782096</td><td>0.7240202</td><td>-7200</td><td>-300</td></tr>
<tr><td>2015-01-30</td><td>14.73</td><td>49</td><td>1.3444371</td><td>0.6569752</td><td>-6600</td><td>600</td></tr>
<tr><td>2015-02-02</td><td>14.26</td><td>46</td><td>1.0248298</td><td>0.5808125</td><td>-5800</td><td>800</td></tr>
<tr><td>2015-02-03</td><td>14.51</td><td>45</td><td>1.1658195</td><td>0.6243123</td><td>-6200</td><td>-400</td></tr>
<tr><td>2015-02-04</td><td>14.50</td><td>44</td><td>1.1498611</td><td>0.6232312</td><td>-6200</td><td>0</td></tr>
<tr><td>2015-02-05</td><td>14.22</td><td>43</td><td>0.9722710</td><td>0.5739954</td><td>-5700</td><td>500</td></tr>
<tr><td>2015-02-06</td><td>14.67</td><td>42</td><td>1.2387716</td><td>0.6537778</td><td>-6500</td><td>-800</td></tr>
<tr><td>2015-02-09</td><td>14.32</td><td>39</td><td>0.9897673</td><td>0.5934679</td><td>-5900</td><td>600</td></tr>
<tr><td>2015-02-10</td><td>14.73</td><td>38</td><td>1.2383233</td><td>0.6687060</td><td>-6700</td><td>-800</td></tr>
<tr><td>2015-02-11</td><td>14.70</td><td>37</td><td>1.2080252</td><td>0.6647852</td><td>-6600</td><td>100</td></tr>
<tr><td>2015-02-12</td><td>14.75</td><td>36</td><td>1.2311183</td><td>0.6750438</td><td>-6800</td><td>-200</td></tr>
<tr><td>2015-02-13</td><td>14.76</td><td>35</td><td>1.2274037</td><td>0.6783712</td><td>-6800</td><td>0</td></tr>
<tr><td>2015-02-17</td><td>14.65</td><td>31</td><td>1.1099416</td><td>0.6644573</td><td>-6600</td><td>200</td></tr>
<tr><td>2015-02-18</td><td>14.80</td><td>30</td><td>1.2006860</td><td>0.6950144</td><td>-7000</td><td>-400</td></tr>
<tr><td>2015-02-19</td><td>14.87</td><td>29</td><td>1.2387319</td><td>0.7103890</td><td>-7100</td><td>-100</td></tr>
<tr><td>2015-02-20</td><td>14.95</td><td>28</td><td>1.2851545</td><td>0.7277306</td><td>-7300</td><td>-200</td></tr>
<tr><td>2015-02-23</td><td>14.66</td><td>25</td><td>1.0459231</td><td>0.6785185</td><td>-6800</td><td>500</td></tr>
<tr><td>2015-02-24</td><td>14.89</td><td>24</td><td>1.1956614</td><td>0.7285719</td><td>-7300</td><td>-500</td></tr>
<tr><td>2015-02-25</td><td>14.66</td><td>23</td><td>1.0208157</td><td>0.6836736</td><td>-6800</td><td>500</td></tr>
<tr><td>2015-02-26</td><td>14.81</td><td>22</td><td>1.1133756</td><td>0.7191333</td><td>-7200</td><td>-400</td></tr>
<tr><td>2015-02-27</td><td>14.75</td><td>21</td><td>1.0577738</td><td>0.7097611</td><td>-7100</td><td>100</td></tr>
<tr><td>2015-03-02</td><td>15.40</td><td>18</td><td>1.5308230</td><td>0.8483386</td><td>-8500</td><td>-1400</td></tr>
<tr><td>2015-03-03</td><td>15.16</td><td>17</td><td>1.3203800</td><td>0.8134503</td><td>-8100</td><td>400</td></tr>
<tr><td>2015-03-04</td><td>15.20</td><td>16</td><td>1.3416118</td><td>0.8272931</td><td>-8300</td><td>-200</td></tr>
<tr><td>2015-03-05</td><td>15.50</td><td>15</td><td>1.5879912</td><td>0.8830361</td><td>-8800</td><td>-500</td></tr>
<tr><td>2015-03-06</td><td>15.10</td><td>14</td><td>1.2352623</td><td>0.8225895</td><td>-8200</td><td>600</td></tr>
<tr><td>2015-03-09</td><td>15.51</td><td>11</td><td>1.5607311</td><td>0.9166819</td><td>-9200</td><td>-1000</td></tr>
<tr><td>2015-03-10</td><td>15.19</td><td>10</td><td>1.2632930</td><td>0.8770427</td><td>-8800</td><td>400</td></tr>
<tr><td>2015-03-11</td><td>15.51</td><td>9</td><td>1.5442340</td><td>0.9358196</td><td>-9400</td><td>-600</td></tr>
<tr><td>2015-03-12</td><td>15.68</td><td>8</td><td>1.6989379</td><td>0.9621082</td><td>-9600</td><td>-200</td></tr>
<tr><td>2015-03-13</td><td>15.95</td><td>7</td><td>1.9579052</td><td>0.9851354</td><td>-9900</td><td>-300</td></tr>
<tr><td>2015-03-16</td><td>15.71</td><td>4</td><td>1.7128848</td><td>0.9942528</td><td>-9900</td><td>0</td></tr>
<tr><td>2015-03-17</td><td>15.54</td><td>3</td><td>1.5419631</td><td>0.9958324</td><td>-10000</td><td>-100</td></tr>
<tr><td>2015-03-18</td><td>15.26</td><td>2</td><td>1.2613654</td><td>0.9961376</td><td>-10000</td><td>0</td></tr>
<tr><td>2015-03-19</td><td>15.42</td><td>1</td><td>1.4203846</td><td>0.9999871</td><td>-10000</td><td>0</td></tr>
<tr><td>2015-03-20</td><td>15.70</td><td>0</td><td>1.7000000</td><td>1.0000000</td><td>-10000</td><td>0</td></tr>
</tbody>
</table>
</div>
