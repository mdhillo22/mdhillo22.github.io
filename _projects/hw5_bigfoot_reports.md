---
name: Bigfoot Reports
tools: [Python, HTML, vega-lite]
image: assets/pngs/pythonanalysisvegaplot.png
description: Two visualizations of Bigfoot reports by state and location.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Bigfoot Reports

The first visualization is comparing 15 U.S. states with the most Bigfoot reportings. I grouped the reports by state, counted them, and kept the top 15 after sorting the
counts from highest to lowest. State is used as a nominal category on the y-axis and the number of reports are used as a quantitative value on the x-axis. I also used the
bar chart style because it helps for easier comparison of the report counts.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_state_reports.json" style="width: 100%"></vegachart>

The second visualization is showing the locations of the reportings by using longitude and latitude, with each point representing a report. Longitude and latitude are 
quantitative position encodings and report classification is a nominal color encoding. The default categorical colors help differentiate the classifications.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_report_locations.json" style="width: 100%"></vegachart>

The second visualization has an interaction where clicking a classification in the legend highlights the reports in that class. The other points in the chart fade, making it easier for comparisons.

{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}

{% include elements/button.html link="https://github.com/mdhillo22/mdhillo22.github.io/blob/main/python_notebooks/hw5.ipynb" text="The Analysis" %}
