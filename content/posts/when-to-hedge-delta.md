+++
title = "When To Hedge Delta: Why There's No Good Answer"
date = "2015-03-03T15:38:03-06:00"
tags = ["trading", "greeks"]
+++
In the course of explaining delta-neutral trading strategies, the question that inevitably arises is when to hedge the net position delta.  It's a great question, but a question with no good (i.e. definite) answer.

<!--more-->
For long gamma strategies, gamma scalping is a means of paying for theta and generating profit.  In this context, the trader is metaphorically trying to harvest volatility from the market.  The convex curvature of a long gamma position allows the trader to buy low and sell high. The question is how to best maximize that process, thereby buying as low and selling as high as possible, while not also missing any smaller intra-day scalps.

Short gamma strategies are the opposite side of the same coin, whereby hedging is the cost of maintaining risk parameters.  The trader is effectively forced to trade counter to the market (i.e. buy high, sell low) in order to keep position risk in check. In this context, the trader would ideally trade as little as possible, thereby minimizing any potential negative scalping.

Digging into the academic literature associated with option pricing models reveals the expectation that an option position is continuously hedged.  So the answer to the initial question, to the extent that there is one, is that an option position should be hedging continuously.  Whether continuous hedging is even possible is highly debatable. Regardless of the theoretical underpinnings, the reality is that traders hedge their positions far less regularly.

Researchers have investigated the impact of non-continuous hedging and have found that less frequent hedging results in a range of possible profit and loss scenarios. The standard deviation of these scenarios tends to decrease by half as the frequency of hedging is increased four-fold. In other words, the less frequent the hedging, the wider the range of possible profit and loss scenarios.

Research into non-continuous hedging has tended to focus on hedging at reduced, but regular time intervals with a constant, known volatility.  Traders have employed hedging strategies ranging from simple ad hoc approaches to various regimented strategies that hedge at regular time intervals (e.g. daily, hourly), are triggered based upon net position delta, or are based upon the expected daily range based upon implied volatility and the [Rule of 16](/post/rule-of-16/).

Perhaps a more interesting question that might help define a hedging strategy is whether there exists any additional underlying volatility not fully represented in historical volatility calculations.  The most typical representation of historical volatility is as the annualized standard deviation of log-normal daily price returns.  The problem is that this model only utilizes daily closing prices, ignoring the intra-day range as represented by the daily high and low prices.  Various models, such as the Garman-Klass volatility estimator, have been constructed that attempt to better estimate historical volatility, yet the close-close model remains ubiquitous.

<a href="/images/2015/03/ohlc.png"><img src="/images/2015/03/ohlc.png" alt="Daily Range vs Historical Volatility" title="Daily Range vs Historical Volatility" height="100%" width="100%"></a>

Taking a look at the price chart for one security sheds some light on the type of movement that might not be fully reflected in the standard close to close historical volatility calculation.  This chart shows a typical daily representation of open, high, low, and closing prices.  The blue bar overlaying each days price range has been added to reflect the daily change in price that would ordinarily be represented by historical volatility.  The areas lying outside of the blue bar represent movement that's not being reflected in the calculation.  For a few of the days, the difference is insignificant, but for many of the days, there's quite a bit of difference.

One of the most obvious instances of this difference is on January 22nd.  The underlying security opens slightly down at $14.10, continues down, hitting an intraday low of $13.39, turns around and rallies to an intraday high of $14.90, before eventually closing the day at $14.82. The close to close change of $0.66 represents only 43.7% of the high-low range.  While the magnitude of the volatility on this particular day was fairly exceptional, there are other days that exhibit a similar back and forth trading range that's simply not adequately captured by the historical volatility calculation.

Identifying securities where historical volatility is not adequately capturing the true intraday trading range can help define both the option trading strategy and the hedging strategy.  In the end, there are many possible hedging strategies, but ideally the hedging strategy will be tailored to the option position and the trading characteristics of the underlying security.
