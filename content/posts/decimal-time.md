+++
title = "Decimal Time"
date = "2013-01-25T15:40:27-06:00"
tags = ["javascript"]
+++
My son wondered why we don't have a more rational, [decimal](http://en.wikipedia.org/wiki/Decimal_time) system for time. To explore the idea, we made a simple javascript clock implementing decimal time.<!--more--> We chose a 20 hour day, rather than 10, because it makes the duration of an hour more similar to our current system, and therefore a bit more intuitive as a unit of time.

<h1 id="decTime"></h1>
Decimal Time

<h1 id="stdTime"></h1>
Standard Time

### Time subdivisions
* 20 hours per day; each hour equals 72 standard minutes.
* 100 minutes per hour; each minute equals 43.2 standard seconds.
* 100 seconds per minute; each second equals 0.432 standard seconds.  
*Midnight, 6am, noon, and 6pm align with the hours 0, 5, 10, and 15.*

<script type="text/javascript" src="/js/clock.js"></script>
