+++
title = "Gamma Scalping Cypress Semiconductor: An Example of Trading a Delta Neutral, Long Gamma Options Position"
date = "2015-01-20T16:07:11-06:00"
tags = ["trading", "greeks"]
+++
In one of today's option mentoring sessions, one of the topics covered was the process of gamma scalping a delta neutral, long gamma options position.  The client was having some difficulty thoroughly understanding the concept.  To better explore the topic, we decided to simulate a very simple long gamma options position in  [Cypress Semiconductor (CY)](http://www.bloomberg.com/quote/CY:US), and then to gamma scalp the underlying security, keeping the net position delta neutral.  
<!--more-->

Since this is purely for educational purposes, we're not as concerned with the profitability of the strategy as we are with exploring the mechanics of gamma scalping.  We will base the paper trading on real, live market prices in CY, and won't go back and adjust trades to make the strategy look better or worse.  If this isn't already abundantly clear, please note that this is entirely for educational purposes and completely fictional. No actual trading will occur in the options or equity markets. Nor will we concern ourselves with many important details such as commissions, availability of stock lending, market liquidity, etc..


#### Option Position

The one and only options position will be a long position of 100 [CY Mar 14 calls](http://www.nasdaq.com/symbol/cy/option-chain/150320C00014000-cy-call), purchased at a price of $1.00.  The total cost is $10,000.  We will hold this option position until expiration in March.

    +100 CY Mar 14 calls @ $1.00


#### Initial Hedge

Each option has a delta of .53, so the net delta will be immediately hedged by selling 5300 shares of CY at $14.00 resulting in a delta neutral position.  Over the life of the option, the option's delta will change as the underlying security moves and as time passes (charm).  We will try to gamma scalp the underlying as vigorously as possible, to offset the time decay (theta) each day.


#### Option Sensitivities (Greeks)
Option sensitivities for call options, from various months, with a strike price of 14, as of January 20th, 2015

<div class="table">
<table class="table table-responsive table-striped">
<thead>
<tr class="header">
<th>Expiration</th>
<th>Price</th>
<th>Delta</th>
<th>Gamma</th>
<th>Theta</th>
<th>Vega</th>
<th>Imp. Vol.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Feb 20, 2015</td>
<td>0.70 - 0.85</td>
<td>0.52</td>
<td>0.19</td>
<td>-0.01</td>
<td>0.02</td>
<td>0.51</td>
</tr>
<tr class="even">
<td>Mar 20, 2015</td>
<td>0.90 - 1.00</td>
<td>0.53</td>
<td>0.16</td>
<td>-0.01</td>
<td>0.02</td>
<td>0.47</td>
</tr>
<tr class="odd">
<td>Jun 19, 2015</td>
<td>1.35 - 1.50</td>
<td>0.53</td>
<td>0.11</td>
<td>-0.00</td>
<td>0.03</td>
<td>0.40</td>
</tr>
<tr class="even">
<td>Jul 17, 2015</td>
<td>1.40 - 1.60</td>
<td>0.53</td>
<td>0.11</td>
<td>-0.00</td>
<td>0.04</td>
<td>0.39</td>
</tr>
</tbody>
</table>
</div>


#### Earnings

Making this example just a bit more interesting, it turns out that Cypress Semiconductor has earnings in two days (Jan. 22th).  It's unclear how this will affect our gamma scalping and ultimately the profitability of this strategy.  Hopefully it will be interesting and provide an additional learning opportunity.

As is fairly typical of a stock heading into earnings, the implied volatility of the options is elevated.  Where the 20 and 50-day historical volatilities are .37 and .43 respectively, the option implied volatilities for the front two months are at least ten points higher.  After earnings are released we would expect implied volatility to decrease so that it's more in line with historical volatility.  Therefore, we might see implied volatility drop .10 to .12 points and the value of the option position may decrease $0.20 to $0.24 given a vega of 0.02.  In other words, the option position may take a quick hit.  Hopefully, the underlying will provide ample opportunity to scalp stock to offset this loss.  We will see.  Normally it wouldn’t be advisable to enter into this kind of a long vega/gamma trade right before earnings, after the implied volatility is already so elevated, but sometimes you learn more when things go wrong than when they go right.


#### Gamma Scalping

Trades in the underlying will be recorded here on a somewhat regular basis. At the end, we will go ahead and tally up the results to determine the net profitability of the strategy. Hopefully though, most of the learning will be done along the way.

<div class="table">
<table class="table table-responsive table-striped">
<caption>Paper Trades in Cypress Semiconductor (CY)</caption>
<thead>
<tr class="header">
<th>Date</th>
<th>Buy / Sell</th>
<th>Quantity</th>
<th>Price</th>
<th>Hedge Position</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jan 20, 2015 2:34 CST</td>
<td>Sell</td>
<td>5300</td>
<td>14.00</td>
<td>-5300</td>
</tr>
<tr class="even">
<td>Jan 21, 2015 8:34 CST</td>
<td>Buy</td>
<td>100</td>
<td>13.82</td>
<td>-5200</td>
</tr>
<tr class="odd">
<td>Jan 21, 2015 11:07 CST</td>
<td>Sell</td>
<td>200</td>
<td>14.22</td>
<td>-5400</td>
</tr>
<tr class="even">
<td>Jan 22, 2015 8:33 CST</td>
<td>Buy</td>
<td>200</td>
<td>13.82</td>
<td>-5200</td>
</tr>
<tr class="odd">
<td>Jan 22, 2015 8:39 CST</td>
<td>Buy</td>
<td>300</td>
<td>13.60</td>
<td>-4900</td>
</tr>
<tr class="even">
<td>Jan 22, 2015 8:41 CST</td>
<td>Buy</td>
<td>300</td>
<td>13.40</td>
<td>-4600</td>
</tr>
<tr class="odd">
<td>Jan 22, 2015 9:14 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.20</td>
<td>-5100</td>
</tr>
<tr class="even">
<td>Jan 22, 2015 9:50 CST</td>
<td>Sell</td>
<td>300</td>
<td>14.40</td>
<td>-5400</td>
</tr>
<tr class="odd">
<td>Jan 22, 2015 10:41 CST</td>
<td>Sell</td>
<td>300</td>
<td>14.65</td>
<td>-5700</td>
</tr>
<tr class="even">
<td>Jan 23, 2015 8:38 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.05</td>
<td>-6200</td>
</tr>
<tr class="odd">
<td>Jan 23, 2015 8:51 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.15</td>
<td>-6700</td>
</tr>
<tr class="even">
<td>Jan 23, 2015 2:19 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.25</td>
<td>-7200</td>
</tr>
<tr class="odd">
<td>Jan 26, 2015 9:05 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.35</td>
<td>-7700</td>
</tr>
<tr class="even">
<td>Jan 27, 2015 9:47 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.80</td>
<td>-7200</td>
</tr>
<tr class="odd">
<td>Jan 27, 2015 1:32 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.25</td>
<td>-7700</td>
</tr>
<tr class="even">
<td>Jan 29, 2015 9:24 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.75</td>
<td>-7200</td>
</tr>
<tr class="odd">
<td>Jan 30, 2015 8:34 CST</td>
<td>Sell</td>
<td>800</td>
<td>15.25</td>
<td>-8000</td>
</tr>
<tr class="even">
<td>Jan 30, 2015 2:20 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.75</td>
<td>-7500</td>
</tr>
<tr class="odd">
<td>Feb 2, 2015 8:45 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.40</td>
<td>-7000</td>
</tr>
<tr class="even">
<td>Feb 2, 2015 9:04 CST</td>
<td>Buy</td>
<td>1000</td>
<td>14.10</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 2, 2015 9:33 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.10</td>
<td>-5500</td>
</tr>
<tr class="even">
<td>Feb 4, 2015 8:33 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.60</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 5, 2015 2:56 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.25</td>
<td>-5500</td>
</tr>
<tr class="even">
<td>Feb 6, 2015 10:28 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.70</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 6, 2015 1:38 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.75</td>
<td>-6500</td>
</tr>
<tr class="even">
<td>Feb 9, 2015 8:47 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.40</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 10, 2015 8:48 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.35</td>
<td>-5500</td>
</tr>
<tr class="even">
<td>Feb 10, 2015 1:40 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.70</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 11, 2015 9:16 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.80</td>
<td>-6500</td>
</tr>
<tr class="even">
<td>Feb 11, 2015 9:59 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.90</td>
<td>-7000</td>
</tr>
<tr class="odd">
<td>Feb 13, 2015 8:35 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.50</td>
<td>-6500</td>
</tr>
<tr class="even">
<td>Feb 13, 2015 8:36 CST</td>
<td>Buy</td>
<td>500</td>
<td>14.40</td>
<td>-6000</td>
</tr>
<tr class="odd">
<td>Feb 13, 2015 12:13 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.80</td>
<td>-6500</td>
</tr>
<tr class="even">
<td>Feb 18, 2015 11:18 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.90</td>
<td>-7000</td>
</tr>
<tr class="odd">
<td>Feb 20, 2015 12:40 CST</td>
<td>Sell</td>
<td>1000</td>
<td>15.00</td>
<td>-8000</td>
</tr>
<tr class="even">
<td>Feb 24, 2015 8:40 CST</td>
<td>Buy</td>
<td>1500</td>
<td>14.40</td>
<td>-6500</td>
</tr>
<tr class="odd">
<td>Feb 24, 2015 9:38 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.75</td>
<td>-7000</td>
</tr>
<tr class="even">
<td>Feb 24, 2015 1:04 CST</td>
<td>Sell</td>
<td>500</td>
<td>14.90</td>
<td>-7500</td>
</tr>
<tr class="odd">
<td>Mar 2, 2015 9:56 CST</td>
<td>Sell</td>
<td>1000</td>
<td>15.22</td>
<td>-8500</td>
</tr>
<tr class="even">
<td>Mar 2, 2015 2:50 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.35</td>
<td>-9000</td>
</tr>
<tr class="odd">
<td>Mar 2, 2015 5:58 CST (afterhours)</td>
<td>Sell</td>
<td>500</td>
<td>15.55</td>
<td>-9500</td>
</tr>
<tr class="even">
<td>Mar 5, 2015 12:45 CST</td>
<td>Sell</td>
<td>500</td>
<td>15.55</td>
<td>-10000</td>
</tr>
</tbody>
</table>
</div>


#### Updates

*   After earnings were released on Thursday morning (Jan. 22nd), the initial price movement was fairly muted, down $0.06. From there the price continued to drop, bottoming at $13.39. Three of our paper trades were "executed" on the way down. The stock then rallied almost 10% from the low, closing at $14.82.  Again, three paper trades were executed as the stock rallied. Culminating in some fairly nice two-way trading.  Volatility came down slightly, but not as much as expected, probably due to the nice movement in the stock.

*   The February expiration cycle was 5 weeks long, leaving 4 more weeks until the expiration of the March calls.  As of February 20th, CY closed at $14.95, and the CY March 14 calls closed at $1.24. Putting together a preliminary tally, thus far the strategy has made a net profit of $1263.00.  That number represents a $2400 profit on the options position, a $4459 profit on CY purchases, and a $5596 loss on CY sales.  Please note two things, the risk would have been far greater, but simply purchasing the call options outright without hedging would have been almost twice as profitable if you liquidated the position right now.  And while there is currently only $0.29 of time value in each option, that essentially represents all of the profit in the options position.  If there aren't further scalping opportunities over the next 4 weeks, and if all of the time value is lost, the position will end up with a net loss of approximately $1650.  At a rate of $0.005 per share, stock commissions thus far would have been $109.

*   On March 2nd, CY was trading up over 1% to $15.59 in after hours trading. Given the options position, and the fact that the 52-week high was $15.48, I was very tempted to sell 1000 shares for the paper account.  With that stock sale, the options would be fully hedged, effectively turning all of the long calls into synthetic long puts.  If the stock were to continue upwards there would be no further opportunities to trade or make money, but if the stock were to fall back towards $14, it would be a great trading opportunity. However, I had some mixed feelings about trading after hours. It felt a bit like cheating. Possibly due to the fact that I know that most "average" investors don't trade outside of normal market hours. The reality though is that if you can get the trade executed, it counts.  Whether that's in pre-market trading, after hours, or during the day. In the end, I decided to split the difference and "sold" 500 shares for the paper account.  In my opinion, that's a fair compromise, in that I'm sure to regret it either way.  If the stock continues up, it was too much, and if it goes back down, it wasn't enough.

*   As of the trade on March 5th, the position has been fully hedged (i.e. all the calls have been turned into synthetic puts).  Given that, it seemed an appropriate time to update the P&L thus far to see where the position stands.  As of the last mark-to-market at Feb. expiration, the position was profitable but vulnerable to time decay.  With the latest scalps and hedging, the position has effectively paid for all the option premium.  That is to say, if the options position is marked to parity versus the stock position, the net P&L for the position would be a small, but positive, profit of $133.  That's an important milestone in that there was still $2900 of time value left in the options as of the last time the position was marked-to-market.  With two weeks still left to expiration, a move back towards the 14 strike is certainly possible.
