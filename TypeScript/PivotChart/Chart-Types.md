---
layout: post
title: Chart Types
description: chart types
platform: Typescript
control: PivotChart
documentation: ug
---

# Chart types

The Essential **PivotChart Typescript** supports 17 types of charts:


* Column
* Stacking column
* Bar
* Stacking bar
* Pie
* Pyramid
* Funnel
* Line
* Step line
* Spline
* Area
* Step area
* Spline area
* Stacking area
* Doughnut
* Scatter
* Bubble


## Column chart


The **column chart** is the most commonly used chart type. This uses vertical bars (called columns) to display different values of one or more items. Points from adjacent series are drawn as bars to compare frequency, count, total, or average of the data in different categories. Column chart is ideal to show the variations in the value of an item over a period of time.

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

The following screenshot displays **column chart**:



![](Chart-Types_images/Chart-Types_img1.png)



## Stacking column chart

The **stacking column** chart is similar to column charts except for the Y-values. The Y-values stack on top of each other in a specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.

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



The following screenshot displays **stacking column chart**:

![](Chart-Types_images/Chart-Types_img2.png)


## Bar chart

The **bar chart** displays horizontal bars for each point in the adjacent series. Bar charts are used to compare values across various categories for displaying the variations in the value of an item over a period of time or comparing the values of several items at a single point of time.

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


The following screenshot displays **bar chart**:


![](Chart-Types_images/Chart-Types_img3.png)



## Stacking bar chart

The **stacking bar chart** is a regular **bar** chart with the X-values stacked on top of each other in the specified series order.

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



The following screenshot displays **stacking bar chart**:

![](Chart-Types_images/Chart-Types_img4.png)



## Pie chart

The **pie chart** is used to summarize a set of categorical data or display different values of a given variable (e.g., percentage distribution). This type of chart is in a circular form that is divided into several segments. Each segment represents a particular category.

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


The following screenshot displays **pie chart**:



![](Chart-Types_images/Chart-Types_img5.png)



## Pyramid chart

The **pyramid chart** displays data in the form of a triangle. You can visualize data in a hierarchical structure without any axes.

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

The following screenshot displays **pyramid chart**:


![](Chart-Types_images/Chart-Types_img6.png)


## Funnel chart

The **funnel chart** displays data in the form of an inverted triangle. You can visualize data in a hierarchical structure without any axes.

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


The following screenshot displays **funnel chart**:


![](Chart-Types_images/Chart-Types_img14.png)



## Line chart

The **line chart** joins the data points on a plot using straight lines that show the trends in data at equal intervals.

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


The following screenshot displays the **line chart**:

![](Chart-Types_images/Chart-Types_img7.png)



## Step line chart

The **step line chart** uses horizontal and vertical lines to connect data points resulting in a step like progression.

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


The following screenshot displays **step line chart**:

![](Chart-Types_images/Chart-Types_img8.png)



## Spline chart

The **spline chart** is similar to the line chart except that it connects different data points with curve lines instead of straight lines.


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


The following screenshot displays the **spline chart**:

![](Chart-Types_images/Chart-Types_img9.png)



## Area chart

The **area chart** emphasizes the degree of change of values over a period of time. Instead of rendering data as discrete bars or columns, the area chart renders the continuous ebb-and-flow pattern as defined against the Y-axis.

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

The following screenshot displays **area chart**:

![](Chart-Types_images/Chart-Types_img10.png)



## Step area chart

The **step area** chart is similar to the regular area chart except for a straight line tracing the shortest path between the data points. The values are connected by continuous vertical and horizontal lines to form a step like progression.

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


The following screenshot displays **step area chart**:

![](Chart-Types_images/Chart-Types_img11.png)



## Spline area chart

The **spline area** chart is similar to the area chart, but differs by connecting data points in a series. This connects each series of points by a smooth **spline curve**.


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

The following screenshot displays **spline area chart**:

![](Chart-Types_images/Chart-Types_img12.png)



## Stacking area chart

The **stacking area** chart is similar to the regular area chart except for the Y-values. These Y-values stack on top of each other in the specified series order. This helps to visualize the relationship of parts to the whole chart across various categories.


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


The following screenshot displays **stacking area chart**:

![](Chart-Types_images/Chart-Types_img13.png)

## Doughnut chart

The **doughnut chart** is a doughnut like structure used to summarize a set of categorical data that is divided into several segments. Each segment represents a particular category.

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

The following screenshot displays **doughnut chart**:

![](Chart-Types_images/DoughnutChart.png)

## Scatter chart

The **scatter chart** displays data as a collection of points corresponding to associated values.

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

The following screenshot displays **scatter chart:**

![](Chart-Types_images/ScatterChart.png) 

## Bubble chart

The **bubble chart** displays data as a collection of bubbles.

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

The following screenshot displays **bubble chart:**

![](Chart-Types_images/BubbleChart.png)

## Combination chart

The **combination chart** combines two or more series types in a single chart, but there are some limitations in the combination chart. They are:

1. The combination chart cannot combine column and bar series.
2. The pie chart cannot be used with other series types.


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


The following screenshot displays **combination chart:**

![](Chart-Types_images/combinationalchart.png)


