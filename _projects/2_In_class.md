---
name: Building Inventory Analysis
tools: [Python, HTML, Vega-Lite, Altair]
#image: assets/pngs/building_inventory_viz.png
description: Visualizing building inventory data with Python and Altair.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Building Inventory Analysis

## Visualization 1: Top 10 Years with the Most Total Square Footage

This bar chart highlights the top 10 years with the highest total square footage of buildings. The data is grouped by the year each building was constructed, and the total square footage for each year is calculated and summed. The chart ranks the years in descending order based on total square footage, displaying the results with the x-axis representing total square footage (quantitative) and the y-axis showing the corresponding years (categorical). A blue color scale is applied to visually encode the square footage, with darker shades indicating higher values. This design choice makes it easy to identify and prioritize the years with the most significant building activity.

To create this visualization, the data was transformed by grouping it by "Year Constructed" and summing the square footage for each year. The resulting values were sorted in descending order to highlight the years contributing the most to total square footage. By focusing on the top 10 years, the chart provides a clear and concise overview of how building space has been developed over time, emphasizing the years with the largest contributions to the dataset.

<vegachart schema-url="{{ site.baseurl }}/assets/json/top_year_constructed_bar.json" style="width: 100%"></vegachart>


---

## Visualization 2: Building Sizes Over Time in Champaign-Urbana (Last 50 Years)

This scatter plot visualizes building square footage over time for University of Illinois buildings in Champaign-Urbana, focusing on those constructed in the last 50 years. The x-axis represents the year of construction, while the y-axis shows the square footage of each building. Colors are used to represent different usage descriptions, allowing users to easily distinguish between various building purposes. Tooltips provide detailed information about each building, including its name, year of construction, square footage, and usage description.

The dataset has been filtered to include only University of Illinois buildings in Champaign County constructed from 1974 onward. This ensures the focus remains on recent developments, highlighting trends in infrastructure growth and building functionality over time. By narrowing the scope, the visualization avoids clutter and emphasizes relevant, modern data.

Interactivity is incorporated through tooltips, which offer a dynamic way to explore the data. Hovering over a point reveals detailed building information, enabling users to gain insights without overwhelming the visualization. This scatter plot effectively showcases the diversity and evolution of building sizes and purposes in the Champaign-Urbana area, offering a clear view of the University of Illinois's infrastructure development.

<vegachart schema-url="{{ site.baseurl }}/assets/json/building_scatter_plot.json" style="width: 100%"></vegachart>

---

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/your_username/your_repo/blob/main/building_analysis.ipynb" text="The Analysis" %}
</div>
