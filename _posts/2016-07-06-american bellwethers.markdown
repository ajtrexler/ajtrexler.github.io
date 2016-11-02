---
layout: post
title: american bellwethers
date: 2016-07-06
---
A 'bellwether', defined by Wikipedia, is one that indicates or leads trends.  

What region of the country (counties or cities) might be best representative of the rest of the country?  The answer to this question might be of interest for a variety of applications like market research or polling.  I wanted to address this question using the [American Community Survey](https://www.kaggle.com/census/2013-american-community-survey) dataset from Kaggle.  The ACS data is census data grouped into defined population-size areas called [PUMAs](https://en.wikipedia.org/wiki/Public_Use_Microdata_Area) (public use microdata areas).  As a test case I attempted to predict the peoples' occupations based on a model I built for each PUMA in the dataset using machine learning algorithms (support vector machines and principle component analysis).

![figure1](https://raw.githubusercontent.com/ajtrexler/abw/master/readme_figure1.png)
[results](https://github.com/ajtrexler/abw/blob/master/puma_result.md)  
**TL;DR: More data is better, in this case.**

[full analysis pipeline](https://github.com/ajtrexler/abw/blob/master/README.md)
