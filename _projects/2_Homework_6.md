---
name: Homework 6
tools: [Python, HTML, vega-lite]
image: assets/pngs/hw6-pic.png
description: This is my homework 6 page, License Types and Disciplinary Actions - Interactive Visualizations
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# License Types and Disciplinary Actions: Interactive Visualizations

We explore the licenses dataset using two interactive visualizations created with Altair. The dataset provides information about various types of licenses, including their statuses and any disciplinary actions taken. Our goal is to help users understand the distribution of licenses by type and status and to explore the timeline of disciplinary actions. Both visualizations are interactive, with one offering a unique selection feature to highlight specific licenses.

## The Data

<div class="left" style="display: block;">
{% include elements/button.html link="/assets/hw6/licenses_fall2022.csv" text="Download Data CSV" %}
</div>
<br/>

## Visualization 1: Number of Licenses by Type and Status

<vegachart schema-url="/assets/hw6/number_of_licenses_by_type_and_status.json" style="width: 100%"></vegachart>

#### Description
The first visualization displays the number of licenses by type and their respective statuses. The dataset contains a variety of licenses, including those related to cosmetology, medical boards, and many others. Each bar represents a license type, with the colors indicating the license status.

#### Design Choices
We used a stacked bar chart to visualize the count of licenses across different types. The color scheme helps differentiate between the various license statuses, making it easier for viewers to quickly identify trends or outliers in the data. We chose to use a selection filter bound to the legend, allowing users to highlight and focus on specific license types. This improves clarity by dynamically adjusting the opacity of non-selected licenses, emphasizing user-selected data.

#### Data Transformation
The data was grouped by 'License Type' and 'License Status' to calculate the count of each combination, making the bar chart intuitive for comparison. No further transformations were needed.

---

## Visualization 2: Timeline of Licenses with Disciplinary Actions

<vegachart schema-url="/assets/hw6/timeline_of_licenses_with_disciplinary_actions.json" style="width: 100%"></vegachart>

#### Description

The second visualization is a timeline that shows the disciplinary actions associated with various licenses. Each line represents a period in which a license had disciplinary action, with the x-axis indicating the start and end dates of the disciplinary period.

#### Design Choices

We used a line chart to display the periods of disciplinary action for different licenses, with each line representing a different license type. To add interactivity, we added a zoom feature to allow users to focus on specific periods. This makes it easier to examine the details of disciplinary actions over time without overwhelming the viewer with too much data at once.

#### Data Transformation

The disciplinary data was filtered to remove records without valid start or end dates. We also converted these dates to a temporal format, allowing them to be used effectively in the timeline.

---

## Conclusion
These visualizations help provide insight into the types of licenses issued and their statuses, as well as into any disciplinary actions that occurred. The interactive features enable users to explore the data more deeply, providing a clearer understanding of trends and specific cases.