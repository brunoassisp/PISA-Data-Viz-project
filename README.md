# PISA-Data-Viz-project (In construction :construction_worker:)
Data Visualization Project from Udacity developed over the PISA dataset

| Table of Contents |
| --- |
| [Summary](#summary) :chestnut: :shell: |
| [Design](#design) :triangular_ruler: |
| [Feedback](#feedback) :speech_balloon: |
| [Final View](#final-view) :chart_with_upwards_trend: |
| [Resources](#resources) :link: |

## Summary
PISA is a worldwide study by OECD in member and non-member nations intended to **evaluate educational systems** by measuring 15-year-old students **scholastic performance on _mathematics_, _science_, and _reading_**.

In this **Data Visualization Project**, I'm going to present the **students maths behavior per country** based on PISA-defined variables.

This dataset may not represent the reality, but it can give a sense over students perfomance and behavior.

Besides that, to achieve the final dataset used to build this visualization, an EDA process was realized.

### Findings
From this project I could notice that **Brazil's students behavior over maths** always tend to present a higher count percentage of ***lower** frequencies* (*Never or rarely*, *Sometimes*). 

Besides that, I could also compare Brazil's students behavior tendency with all of the other countries tendencies. Interestingly enough, almost all countries present the same behavior where the *lower frequencies* are a lot higher than the *higher frequencies* (*Often*, *Always or almost always*).

The question that raises is: **How can we change this scenario?**

## Design
The design followed a ["martini glass" visualzation](https://www.benchmarkemail.com/blogs/detail/infographics-structure-the-martini-glass) and by using a [**frequency polygon**](http://onlinestatbook.com/2/graphing_distributions/freq_poly.html) it shows how the students behavior varies per country.

By applying different **colors** and **transparency** in the lines, it becomes possible to analyze and compare a Country behavior with the others and understand which is the tendency for every country.

Besides that, a **table** was used to prompt the values highlighted in the current selection.

Mouse events were also covered so the user could interact with the circles (or bubbles) from the chart.

## Feedback
Many feedbacks were taken into account to build the final view. Let's list some of them:

### Person 1
- Create a link between the table and the circles so the information could be seen as one;
- Adding a gap between the y-axis and the first x point;

**Folow-up**: Added mouse events so when the user hover the mouse over the circles, the correspondent table column gets highlighted. 

For the other suggestion, I've used a different *scale* to the x-axis and defined an "inner-padding":

```javascript
var frequency_scale = d3.scaleBand()
            .rangeRound([0, innerWidth])
            .domain(frequency_list)
            .paddingInner(.8);
```

### Person 2
- Adding more transparency to the non-highlighted lines;

**Follow-up**: Updated the style of the ``.line`` class by decreasing the ``opacity`` parameter.

### Person 3
- Highlighting the highest value in the table;

**Follow-up**: Added style to the *Max-value* found in the list of *count percents* by changing the background color, the font size and weight.

```css
.maxValue {
        font-size: 14px;
        font-weight: bold;
        background: #ececec;
      }
```

### Person 4
- Add a reverse search to find a country from the chart;
- Add a narration to describe the main findings;

**Follow-up**: Added mouse events so when the user hover the mouse over the lines and click them, this line gets selected.

Added a dynamic text box that changes for each displayed variable during the animation.

## Final View
Do you want to see the final result?

Click [here](https://bl.ocks.org/brunoassisp/raw/777155e4bec1f3d883373717208c43a9/)! :point_left:

## Resources
Here a list of references used to build this Data-viz:
- **Popular Blocks** » http://bl.ocks.org
- **Udacity** » https://classroom.udacity.com/
- **Stackoverflow** » stackoverflow.com
- **ColorHexa** » https://www.colorhexa.com
- **W3Schools.com** » https://www.w3schools.com
- **D3: Data-Driven Documents** » https://github.com/d3/d3