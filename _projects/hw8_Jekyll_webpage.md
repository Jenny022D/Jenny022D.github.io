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

For my first visualization, I created a bar chart showing the number of Bigfoot reports by season. This visualization helps compare how sightings vary across different times of the year. I encoded season as a nominal variable on the x-axis and the count of reports as a quantitative variable on the y-axis. I used color to represent season because it is a categorical variable, making it easier to visually distinguish between different groups.

In my data preparation, I created a subset of the dataset that included only the relevant variables (season, state, and classification) and removed rows with missing values. This ensured the visualization was accurate and clean.

---

## Visualization 2: Reports by State (Interactive)

<div id="vis2"></div>

For my second visualization, I created an interactive bar chart showing the number of Bigfoot reports by state, filtered by classification. In this chart, state is encoded as a nominal variable on the y-axis, while the count of reports is represented quantitatively on the x-axis. I used color to represent classification to help distinguish between categories.

The interactivity is implemented using a dropdown menu that allows the user to select a classification. This improves clarity by allowing users to focus on one group of reports at a time and better compare patterns across states.

---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
vegaEmbed("#vis1", "/assets/json/bigfoot_season.json");
vegaEmbed("#vis2", "/assets/json/bigfoot_state_interactive.json");
</script>
