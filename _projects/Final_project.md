---
name: Greenhouse gasses over the years (IS 445 Final Project)
tools: [Python, HTML, vega-lite]
image: assets/pngs/final project viz.png
description: We analyze the emissions of greenhouse gasses over the years up to 2012 to see how our emmissions are trending. We investigate what are indicators of a high emission country.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Greenhouse gasses over the years (IS 445 Final Project)
## By Shashank Kambhatla

Over the years, greenhouse gas emissions have become increasingly problematic. Gasses like CO2, CH4, and N20 are greenhouse gasses (1) and are often emmiteed by power, industry, and transporttion sectors. These gasses are big contributors towards global climate change, and as such, their emmissions should be monitored closely. 

This article aims to visualize the trends in greenhouse gas emissions over the years up until 2012. We will be using a dataset from the Emissions Database for Global Atmospheric Research (EDGAR) (3, 6), which includes data on emissions for the three gasses for a variety of countires. Data for the years 1970-2012 is present. We will be visualizing trends in emissions over this time period, as well as focussing on our latest data, from 2012, and visualizing what may contribute towards a country being a "high emmisions" country.

# Investigating greenhouse gas emissions
Click on dropdown to select a country

Zoom in and zoom out to see more detail

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart10.json" style="width: 100%"></vegachart>


CO2, NH4, and N20 are some of the largest contributors to phenomenon like climate change. The best way to see whether emissions have increased over the years is to simply plot a line graph like above. We have visualized the emissions of the three gasses over the years for all countries in the dataset. This paints a picture of the trends in each countries emissions. In general we can see that emisisons have drastically gone up over the past few years, particularly that of CO2. However, we can also see some flatter lines around the year 2012, which suggests countries are becoming more aware of the issues posed by these greenhouse gas emissions, and are taking steps to combat them.

# Which sectors emit the most greenhouse gasses
Click on dropdown to select a country

Zoom in and zoom out to see more detail

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart11.json" style="width: 100%"></vegachart>


Just fuguring out who emited how much does not tell us the whole story. It is important for countries to know which sectors of their industries produce the most greenhosue gasses so that they can react with appropriate measures. Our dataset has a convenient set of columns that tells us the emissions from various sectors. This is a graph of overall greenhouse gas emissions per sector over the years. We can see that the contribution of different sectors towards emissions is highly dependant on the country. We can see that in general power emissions seem to be a predominant factor in contributing towards emissions. Furthermore, we do see declining emissions from some sectors in some countries, particularly in the transport sector. 

# What about country size?
Hover over a point to see which country it is

Zoom in and zoom out to see more detail

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart12.json" style="width: 100%"></vegachart>


Not all countries are the same size. This can be in terms of population, area or various other metrics. The size of a country can heavily dictate the ammount of greenhouse gasses emited. It follows that in general a small county will not emit nearly as much as a large one. We have located a dataset by the United Nations (5) that maintains population details on various countries. We are going to use this in conjunction with our emissions dataset to investigate how much population plays a role in determining emissions. We have focused on the year 2012, as this is the latest year of which the emissions dataset includes data. We have also focused on CO2 emissions, as this was seen to be one of the predonminant gasses emitted. We have used a scatter plot to represent various countries. This also allows us to identify which countries have disproportionately high or low emissions for their population.

# How big is an economy?

Hover over a point to see which country it is

Zoom in and zoom out to see more detail

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart13.json" style="width: 100%"></vegachart>


Another metric that can be used to identify "high emission" countries is GDP. GDP stands for Gross Domestic Product and consits of the values of various goods and services made in a given country. It is often used as a measure of the size of a country's economy, which indicates how active their industry is (2). As we have seen. General industry is a large contributor of emissions, so this can be a good metric of how more active economies may emit more greenhouse gasses. We found a dataset by the World Bank (4) that maintains GDP measures for various countries. We will use this to compare GDP data against CO2 emissions. As before, we have focused on the year 2012 and consturcted a scatterplot of country's GDP against their CO2 emissions.. We can also identify disproportionately high or low emissions for a given GDP range.

Thank you for reading my article. I hope this article was informative, and instructive in showcasing some of the trends in greenhouse gas emissions. Please scroll down to see my references, my data sources, and a link to the Python notebook I used to contruct the visualizations seen here.

# References

- (1) Environmental Protection Agency. (n.d.). Overview of Greenhouse Gasses. EPA. Retrieved April 13, 2023, from https://www.epa.gov/ghgemissions/overview-greenhouse-gases
- (2) Beginners:GDP - what is gross domestic product (GDP)? Beginners:GDP - What is gross domestic product (GDP)? - Statistics Explained. (n.d.). Retrieved April 28, 2023, from https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Beginners%3AGDP_-_What_is_gross_domestic_product_%28GDP%29%3F 

# Data Sources

- (3) Janssens-Maenhout, G., Crippa, M., Guizzardi, D., Muntean, M., &amp; Schaaf, E. (2014, September 26). Emissions database for Global Atmospheric Research, version V4.2 FT2012 (time-series). Joint Research Centre Data Catalogue - Emissions Database for Global Atmospheric Research... - European Commission. Retrieved April 28, 2023, from https://data.jrc.ec.europa.eu/dataset/jrc-edgar-jrc-edgar_v4-2_ft2010_timeseries 
- (4) GDP (current US$). World Bank Open Data. (n.d.). Retrieved April 28, 2023, from https://data.worldbank.org/indicator/NY.GDP.MKTP.CD 
- (5) United Nations. (2022). World population prospects - population division. United Nations. Retrieved April 28, 2023, from https://population.un.org/wpp/Download/Standard/CSV/ 
- (6) Emissions CSV file. CORGIS Datasets Project. (n.d.). Retrieved April 28, 2023, from https://think.cs.vt.edu/corgis/csv/emissions/ 

# Code Sources

- https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek12%2FinClass_week12.ipynb
- https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek14%2FinClass_week14.ipynb
- https://vega.github.io/vega-lite/docs/bind.html
- https://vega.github.io/vega-lite-v3/docs/filter.html
- https://vega.github.io/vega-lite-v4/docs/init.html
- https://starboard.gg/nb/nFpfz3I
- https://altair-viz.github.io/user_guide/generated/channels/altair.Tooltip.html

## Search The Data & Methods

<!-- these are written in a combo of html and liquid --> 

<div class="right">
{% include elements/button.html link="https://github.com/Shashank737/Shashank737.github.io/blob/main/python_notebooks/kambhatla-shashank-final_project_part3.ipynb" text="The Analysis" %}
</div>

