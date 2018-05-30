---
layout: post
title: the yield curve
date: 2018-05-29
categories: [paragraph]
tags: data understanding_econ
comments: false
---

### the yield curve!

The [yield curve](https://www.investopedia.com/terms/y/yieldcurve.asp) is one of the many named "curves" in economics.  Like any good data visualization, it encapsulates a great deal of information about a complex system in one simple plot.  The yield curve is generated simply by plotting Us Treasury bond yields (y-axis) at different maturity dates (x-axis).  Typically longer dated bonds will have higher yields, reflecting the risk associated with holding an asset for a longer time period.  Shorter bonds are less risky to hold, so investors demand a lower rate of return on their investment as a result.  An upward sloping line is "normal" indicating the situation described above.  

*But in times of stress*, the yield curve can "invert" wherein the yields on longer dated bonds actually come down whilst the yields on shorter dated bonds go up.  This has happened rarely in the last few decades, a good thing, but did notably happen right before the financial crisis in ~2008.  This indicates investors have low expectations for longer term inflation and want to buy long dated bonds now to "lock-in" those higher interest rates.  There's low demand for shorter term bonds so yields go up.  

Despite being one of those curves often talked about, I rarely see the yield curve plotted.  The data is actually available in tabular form from the [Treasury department's website](https://www.treasury.gov/resource-center/data-chart-center/interest-rates/Pages/TextView.aspx?data=yieldYear&year=2018), so I pulled the data for 2018 and plot it below using Bokeh.  Bokeh allows the creation of interactive plots (you can use the slider to adjust the day for which the yield curve is shown) that are embeddable in HTML documents.  *Voila!*  

You can see over the course of this year so far, as inflation picks up and the Fed raises rates, the yield curve shifts higher but maintains its normal shape.  For the time being, outlooks look relatively bright.  

{% include yield_curve_plot.html %}
