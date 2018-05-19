---
layout: post
title: canary in the coal mine
date: 2016-10-31
tags: data financial
---
# quick coal script

I recently read an article about how many mining companies are bringing decommissioned coal mines online as coal prices surge.  The coal price surge is in response to China cutting production (by limiting the number of days per year that coal mines can operate).  I wondered if the fortunes of coal mining companies really track so closely with coal commodity prices.  

I wrote a [quick script](https://github.com/ajtrexler/coal/blob/master/coal.py) to pull data from [Quandl](www.quandl.com) on the stock price of four large mining companies (versus four 'control' companies) relative to a measurement of coal commodity price.

![figure1](https://raw.githubusercontent.com/ajtrexler/coal/master/figure1.png)

Yes, the coal companies stock price correlates really well with coal prices.

The most surprising thing, to me anyway, was how negatively correlated my so-called control companies (GE, MSFT, GOOG, and BOA) were with coal pricing.  I suspect this reflects that the overall state of the economy is largely dependent, to some extent, on commodity pricing.  Google represented a fairly reasonable control, as its valuation was not strongly correlated with coal price.  

Cross-correlation to quantify the relationship:  
    for x in priceframe:
      subdf=pd.concat([priceframe['Coal'],priceframe[x]],1)
      subdf.dropna(0,inplace=True)
      print 'coal to',x,np.corrcoef(subdf,rowvar=False)[0,1]

correlation coefficients:  
coal to Coal 1.0  
coal to BHP 0.793966783557  
coal to CLD 0.807582234861  
coal to GLEN 0.830652996931  
coal to ANGA 0.68839939301  
coal to ctrlGE -0.577720359433  
coal to ctrlMSFT -0.563274986663  
coal to ctrlGOOG 0.183420735782  
coal to ctrlBOA -0.599947074367

The next step would be to dig into the company fundamentals in order to see whether these companies actually generate more profits as coal prices increase or if they choose to expand capacity and plow revenue into investments.

[the code](https://github.com/ajtrexler/coal/blob/master/coal.py)
