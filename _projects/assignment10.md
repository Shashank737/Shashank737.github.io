---
name: Assignment 10
tools: [Python, HTML, vega-lite]
image: assets/pngs/visualization.png
description: My Homework 10 visualizations
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Shashank Kambhatla
# IS 445 Assignment 10

Note: Links to the data used and the Python notebook used can be found in "the data" and "the analysis" buttons at the bottom of the page respectively.

Code sources:
- https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek12%2FinClass_week12.ipynb
- https://vega.github.io/vega-lite/docs/bind.html
- https://vega.github.io/vega-lite-v3/docs/filter.html
- https://vega.github.io/vega-lite-v4/docs/init.html
- https://starboard.gg/nb/nFpfz3I


# Viz 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart1.json" style="width: 100%"></vegachart>

Code sources:
- https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek12%2FinClass_week12.ipynb
- https://vega.github.io/vega-lite/docs/bind.html
- https://vega.github.io/vega-lite-v4/docs/init.html
- https://starboard.gg/nb/nFpfz3I

For this assignment, I chose to stick with the same dataset that I used for assignment 9, as I felt there was plenty of scope for more interesting graphs. Furthermore, I wanted to work on creating an interactive graph for this dataset. I decided to make an interactive version of a graph of floors above grade over time. The graph depicts the mean floors above grade for each year in which a building was constructed. I made an interactive graph by providing the ability for the user to filter the chart to the Congressional district of their choosing. I felt that this interactivity makes for an interesting way to observe how different counties took up taller buildings over time, and how many they were building.

I had done a graph of floors above grade over years constructed as a line graph for my previous assignment, so I referenced this as a starting point. This was plot 1 from assigmment 9. I removed the quotation marks around the numbers to make the previous vega lite plot on Starboard work with Altair. I also made other changes to the code. I chose to implement a bar chart, rather than a line graph that I had previously executed, as I noticed that upon filtering, data values for some years were not present for some congressional district. This affected the line graph because it introduced inacurate lines in some places where there was no data. The bar graph showcased a much better representation of which years had no data, and which years did. 

The transformation I added to this graph was to filter the data to the "selection s". Selection s is the parameter I created that takes an input Congressional district from the user in a dropdown menu. The transform command sees this and filters to the desired Congressional district. For the encoding, I made sure to specify that the year constructed was temporal data. I also specified the timeunit as years, so we get yearly intervals. I also implemented mean aggration for the floors above grade to get the average number for each year a building was constructed. I also I chose not to add any additional coloring or colorscheme as I deemed the standard vega lite bar graph colors sufficient in conveying the meaning of the graph. The bars themselves differentiate years from one another, so further coloring was not necessary.

# Viz 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/mychart2.json" style="width: 100%"></vegachart>

Code sources:
- https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek12%2FinClass_week12.ipynb
- https://vega.github.io/vega-lite-v3/docs/filter.html
- https://starboard.gg/nb/nFpfz3I

Once again, this visualization uses the same dataset as that used in Homework 9. This visualization is based upon the seccond plot form Assignment 9, but uses a different field on the y axis, a different and a different transformation. This graph is a bar graph that depicts the number of buildings with 5 floors or more in all counties with at least one building in this range. I chose to make this graph because I wanted to explore the transformation features that Vega lite has. 

I performed a filter transformation on the dataset. Specifically, I filtered the Total Floors field to all values equal to and above 5 using the "gte" parameter. I then counted these values using the aggregate count function in the encoding for the Total Floors axis. I set the encoding of the counties field to "nominal" given that it is vategorical data. I again chose a bar graph as I felt it was the best at depicting the aggrgated counts of the various counties. I did not implement a colormap as, like before, I found the standard colors to be sufficient for the purposes of a bar graph. 

## Search The Data & Methods

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

