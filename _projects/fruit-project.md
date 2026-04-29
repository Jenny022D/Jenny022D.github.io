---
layout: project
title: "Which Fruits Give You the Best Value?"
description: "A data visualization project comparing fruit prices by form and cup equivalent."
image: "/assets/images/fruit.png"
category: python
---

# Which Fruits Give You the Best Value
By [Jenny Dong, Huiwon An]

Fruit Prices can be confusing because the sticker price does not always tell us how much fruit we actually get to eat. A fruit may look cheap by the pound, but once we account for preparation yield, waste, and cup equivalent size, the real cost can look very different. This project uses USDA fruit price data to compare average retail price with average price per cup equivalent.

## 🍎 Main Visualization: Comparing Fruit Prices by Form

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>


<div id="vis"></div>

<script type="text/javascript">
  var spec = "/assets/json/fruit_db.json";
  vegaEmbed('#vis', spec);
</script>


This interactive dashboard lets readers explore how fruit form affects price. The top chart shows the average price per cup equivalent by fruit form, such as fresh, frozen, canned, dried, or juice. When readers click a form, the lower charts filter to show only fruits in that category. The scatterplot compares retail price with price per cup equivalent, while the bar chart shows preparation yield for selected fruits.

## 📊 What the Data Shows

One important pattern is that the retail price alone does not always show the real cost of eating fruit. Some fruits may have a low price per pound but a higher price per cup equivalent because parts of the fruit are discarded during preparation. This makes the cup equivalent measure more useful for consumers who want to compare actual edible servings.

Another pattern is that fruit form matters. Fresh fruit is not always the cheapest option, and processed forms such as frozen, canned, or juice can sometimes be more cost effective depending on the fruit. However, price is only one part of the story. Consumers may also consider convenience, nutrition, shelf life, and taste.

One of the most noticeable trends is that canned and frozen fruits tend to have the highest price per cup equivalent. This suggests that while these forms offer convenience and longer shelf life, consumers are paying a premium for processing and preservation. On the other hand, juice appears to have the lowest cost per cup equivalent, making it the most affordable option in terms of volume, though it may lack the nutritional benefits of whole fruit.

## 💡 How to understand the Dashboard

When using this dashboard, start by looking at the top bar chart, where you can see which fruit forms, like juice, fresh or canned, generally cost more per cup. Clicking on one of the bars will filter the two charts below to show only the fruits in that specific category. In the bottom left scatter plot, each point represents a fruit, you can click and drag your mouse over a group of points to brush a slection, which then updates the bar chart on the right to list only those specific fruits. This allows you to compare each fruit yields and prices, for example you can select the least expensive juices in the scatter plot to see their names and preparation yield factors in the right list.

The scatter plot reveals the relationship between retail price and price per cup equivalent. While there is a general upward trend meaning higher retail prices often lead to higher per cup costs the relationship is not perfectly linear. Some fruits have high retail prices but relatively efficient yields, making them more cost effective than expected. Others appear cheap at first but have low edible yield, increasing their true cost.


## 💡 Plot Summary 

This data visualization represents the relationship between the average retail price of fruits and vegetables and the average price per cup equivalent. The points on the scatter plot represent a specific food item, allowing the users to be able to compare how the cost at the purchase goes into the cost of actual consumption. Looking at the plot, it is clear that some items with lower retail value still have a high price per cup, suggesting inefficiencies due to preparation, waste, or serving size differences. The interactive feature allows users to click on individual points to view detailed information and helps identify patterns across different food forms like fresh, frozen, or canned. This plot helps highlight how pricing differences are not always straightforward.

## Sources

Data source: USDA Economic Research Service, Fruit and Vegetable Prices  
https://www.ers.usda.gov/data-products/fruit-and-vegetable-prices
