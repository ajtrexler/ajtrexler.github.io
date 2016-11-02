---
layout: post
title: exoplanet data exploration
date: 2016-10-21
---
# Where should we go?

This is a simple exploratory analysis of the Open Exoplanet Catalogue.  I map out all the systems in the database, look for a bit of structure in the data using principle component analysis (after adding in missing values using a kernel density estimation function), and finally apply some simple rules to five features in the dataset to assess which exoplanets might be habitable.  Below are plotted what my analysis shows are the closest exoplanets, most likely to be habitable and with surface temperatures conducive to liquid water!

![figure1](https://raw.githubusercontent.com/ajtrexler/exoplanet/master/exo_figure2.png)

Here's my [kernel](https://www.kaggle.com/atrexler/d/mrisdal/open-exoplanet-catalogue/where-should-we-go-v2) on Kaggle with more description of each step of the code.

[Repo with code and figures](https://github.com/ajtrexler/exoplanet)
