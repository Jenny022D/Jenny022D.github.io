---
layout: project
title: "Which Fruits Give You the Best Value?"
---
# Which Fruits Give You the Best Value
By [Jenny Dong, Huiwon An

Fruit Prices can be confusing because the sticker price does not always tell us how much fruit we actually get to eat. A fruit may look cheap by the pound, but once we account for preparation yield, waste, and cup equivalent size, the real cost can look very different. This project uses USDA fruit price data to compare average retail price with average price per cup equivalent.

## Main Visualization: Comparing Fruit Prices by Form

<div id="vis"></div>

<script type="text/javascript">
  var spec = "/assets/json/fruit_db.json";
  vegaEmbed('#vis', spec);
</script>
<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
