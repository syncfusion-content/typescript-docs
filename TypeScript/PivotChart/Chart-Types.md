---
layout: post
title: Chart Types
description: chart types
platform: Typescript
control: PivotChart
documentation: ug
---

# Chart Types

Essential **PivotChart Typescript** supports 17 different types of chart as follows:


* Column
* Stacking Column
* Bar
* Stacking Bar
* Pie
* Pyramid
* Funnel
* Line
* Step Line
* Spline
* Area
* Step Area
* Spline Area
* Stacking Area
* Doughnut
* Scatter
* Bubble


## Column Chart


**Column Chart** is the most commonly used chart type. It uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars next to each other. It is used to compare the frequency, count, total or average of data in different categories. It is ideal to show the variations in the value of an item over a period of time.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        },
	});
});

{% endhighlight %}

The following screenshot displays a **Column Chart**.



![](Chart-Types_images/Chart-Types_img1.png)



## Stacking Column Chart

**Stacking Column** Chart is similar to column charts except the Y-values. These Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to whole across categories.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingColumn
        },
	});
});

{% endhighlight %}



The following screenshot displays the **stacking Column Chart**.

![](Chart-Types_images/Chart-Types_img2.png)


## Bar Chart

The **Bar Chart** displays horizontal bars for each point in the series and points from adjacent series. Bar charts are used to compare values across categories, for displaying the variations in the value of an item over time or for comparing the values of several items at a single point in time.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Bar
        },
	});
});

{% endhighlight %}


The following screenshot displays a **Bar Chart**.


![](Chart-Types_images/Chart-Types_img3.png)



## Stacking Bar Chart

**Stacking Bar Chart** is a regular **bar** chart with the X-values stacked on top of each other in the specified series order.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingBar
        },
	});
});

{% endhighlight %}



The following screenshot displays the **Stacking Bar Chart**.

![](Chart-Types_images/Chart-Types_img4.png)



## Pie Chart

A **Pie chart** is used to summarize a set of categorical data or displaying different values of a given variable (e.g., percentage distribution). This type of chart is a circle divided into a series of segments. Each segment represents a particular category.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Pie
        },
	});
});

{% endhighlight %}


The following screenshot displays a **Pie Chart**.



![](Chart-Types_images/Chart-Types_img5.png)



## Pyramid Chart

The **Pyramid Chart** type displays the data in the form of a triangle. It helps you to visualize data in a hierarchical structure without any axes.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Pyramid
        },
	});
});

{% endhighlight %}

The following screen shot displays the **Pyramid Chart**.


![](Chart-Types_images/Chart-Types_img6.png)


## Funnel Chart

The **Funnel Chart**  type displays the data in the form of an inverted triangle. It helps you to visualize data in a hierarchical structure without any axes.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Funnel
        },
	});
});

{% endhighlight %}


The following screen shot displays the **Funnel Chart**.


![](Chart-Types_images/Chart-Types_img14.png)



## Line Chart

The **Line Chart** joins the data points on a plot using straight lines that show trends in data at equal intervals.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Line
        },
	});
});

{% endhighlight %}


The following screenshot displays the **Line Chart**.

![](Chart-Types_images/Chart-Types_img7.png)



## Step Line Chart

**Step Line Chart** uses horizontal and vertical lines to connect the data points resulting in a step like progression. 

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepLine
        },
	});
});

{% endhighlight %}


The following screenshot displays the **Step Line Chart**.

![](Chart-Types_images/Chart-Types_img8.png)



## Spline Chart

The **Spline Chart** is similar to line charts except it connects different data points using curve lines instead of straight lines.


{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Spline
        },
	});
});

{% endhighlight %}


The following screenshot displays the **Spline Chart**.

![](Chart-Types_images/Chart-Types_img9.png)



## Area Chart

**Area Chart** emphasizes the degree of change of values over a period of time. Instead of rendering data as discrete bars or columns, an area chart renders it in a continuous ebb-and-flow pattern as defined against the y-axis.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Area
        },
	});
});

{% endhighlight %}

The following screenshot displays the **Area Chart**.

![](Chart-Types_images/Chart-Types_img10.png)



## Step Area Chart

**Step Area** chart is similar to the regular area chart except for a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines forming a step like progression.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StepArea
        },
	});
});

{% endhighlight %}


The following screenshot displays a **Step Area Chart**.

![](Chart-Types_images/Chart-Types_img11.png)



## Spline Area Chart

**Spline Area** chart is similar to Area Chart with the difference in which the data points of a series are connected. It connects each series of points by a smooth **spline curve**.


{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.SplineArea
        },
	});
});

{% endhighlight %}

The following Screenshot displays a **Spline Area Chart**.

![](Chart-Types_images/Chart-Types_img12.png)



## Stacking Area Chart

**Stacking Area** chart is similar to regular area chart except the “Y-values”. These “Y-values” stack on top of each other in the specified series order. This helps to visualize the relationship of parts to whole across categories.


{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.StackingArea
        },
	});
});

{% endhighlight %}


The following screenshot displays a **Stacking Area Chart**.

![](Chart-Types_images/Chart-Types_img13.png)

## Doughnut Chart

A **Doughnut chart** is also used to summarize a set of categorical data which possesses a doughnut like structure divided into a series of segments. Each segment represents a particular category.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Doughnut
        },
	});
});

{% endhighlight %}

The following screenshot displays a **Doughnut Chart**.

![](Chart-Types_images/DoughnutChart.png)

## Scatter Chart

The **Scatter Chart**  type displays the data as a collection of points corresponding to the associated values.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Scatter
        },
	});
});

{% endhighlight %}

The following screen shot displays the **Scatter Chart.**

![](Chart-Types_images/ScatterChart.png) 

## Bubble Chart

The **Bubble Chart**  type displays the data as a collection of bubbles.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Bubble
        },
	});
});

{% endhighlight %}

The following screen shot displays the **Bubble Chart.**

![](Chart-Types_images/BubbleChart.png)

## Combination Chart 

A **combination Chart** combines two or more series types in a single Chart. But there are some limitations in the combination Chart. They are:

1. Can’t combine Column and Bar series.
2. Pie Chart can’t be used with other series types.


{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        },
        load: function (args) {
            this.model.seriesRendering = function (event) {
                this.model.series[5].type = ej.PivotChart.ChartTypes.Line;
                this.model.series[5].marker.visible = true;
            };
        }
	});
});

{% endhighlight %}


The following screenshot displays a **combination Chart**.

![](Chart-Types_images/combinationalchart.png)


