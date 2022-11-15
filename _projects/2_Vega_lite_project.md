---
name: Take 2
tools: [Python, HTML, vega-lite, Jekyll]
image: assets/pngs/ppp2.png
description: This is mutiple ways
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# 1. Including plots
```
<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>
```
Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:



<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:


## Search The Data & Methods

Below is our plot completing process:

```
Plot1 used the dataset of “https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv”.

In order to identify whether the location influenced the square footage of the buildings,
our group used “Square Footage” as the x-axis and “County” as the y-axis to make up a heat map.
For the x-axis, we also use the count function to add up the total square footage varied from each county.
In the heatmap, we used the default color to present the visualization,
because the default color is clear enough to show the relationship.
In addition, we created a histogram based on the “Total Floors” to figure out the frequency of “Total Floors”.
And then we set interactivity between the heat map and histogram.
The interactivity was to what is the frequency of “Total Floors” once selected the location of “Square Footage” and “County”.
```
<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/DDMeer/github.io/blob/main/assets/json/scatter233.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/DDMeer/github.io/blob/main/python_notebooks/group18-assignment10.ipynb" text="The Analysis" %}
</div>

