---
layout: page
title: Bigfoot Reports Visualization
description: Altair and Vega-Lite visualizations of Bigfoot sightings
---

# Bigfoot Reports Visualization

[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv){: .btn .btn-primary}
[The Analysis](https://github.com/Jenny022D/Jenny022D.github.io/blob/main/Workbook.ipynb){: .btn .btn-primary}

---

## Visualization 1: Reports by Season

<div id="vis1"></div>

For my non interactive first visualization, I created a bar chart that shows the number of Bigfoot reports by season. The visualization helps compare how sightings vary across different times of the year. I showed seasons as a nominal variable for the x axis and the count of reports as a quantitative variable on the y axis. I used colors to represent seasons sand it makes it easier to distinguish between the different groups of seasons. I also created a subset of data that included only the relevant variables like seasons, state, and classification, and removed rows and missing values. This makes sure the visualizations were accurate and clean.

---

## Visualization 2: Reports by State (Interactive)

<div id="vis2"></div>

For my second visualization, I created an interactive bar chart showing the number of Bigfoot reports by state, filtered by classification. In this chart, the states are placed as a variable on the y axis, and the count of reports is placed on the x axis as numbers. I used color to represent the classification to help distinguish between categories. The interaction is made to use a dropdown menu that allows the user to select a classification. The improves clarity by allolwing the users to be able to focus on one group of reports at a time to better compare patterns across states. 

---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed("#vis1", "/assets/json/bigfoot_season.json");
vegaEmbed("#vis2", "/assets/json/bigfoot_state_interactive.json");
</script>
