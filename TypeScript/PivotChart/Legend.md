---
layout: post
title: Legend
description: legend
platform: Typescript
control: PivotChart
documentation: ug
---

# Legend

## Legend visibility

You can enable or disable the legend by using the `visible` property in the `legend` object.

N> By default, the legend is visible in the pivot chart.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		legend: { 
			visible: true 
		},
	});
});

{% endhighlight %}

![](Legend_images/Legend_img1.png) 

## Legend shape
You can customize the legend `shape` in the pivot chart control. The default value of legend shape is rectangle. Following are the legend shapes that are supported:

* Rectangle
* Circle
* Cross
* Diamond
* Pentagon
* Hexagon
* Star
* Ellipse
* Triangle etc.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		legend: {
            visible: true,
            shape: "star"
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img2.png) 

## Legend position
By using the `position` property, you can place the legend at top, bottom, left, or right of the pivot chart.

N> The default value of legend position is bottom in the pivot chart.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            position: "top"
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img3.png) 

## Legend title
To add the legend title, you should specify the title text in the `title.text` property.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            title: {
                text : "Countries"
            }
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img4.png) 

## Legend alignment
You can align the legend to center, far, and near based on its position in the chart area by using the `alignment` option.
 
{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            alignment: "near"
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img5.png)

## Legend items - size and border
By using the legend `itemStyle.width`, `itemStyle.height`, and `itemStyle.border` properties, you can change the size and border of legend items.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            itemStyle: {
                border: {
                    width: 1.5,
                    color: "magenta"
                },
                width: 12,
                height: 12
            }
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img6.png)
 
## Legend border
By using the `border` option in the legend, you can customize the border color and width.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            border: {
                color: "orange",
                width: 5
            }
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img7.png)

## Legend text
By using the `font` option, you can customize the font family, font style, font weight, and size of the legend text. 

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        legend: {
            visible: true,
            font: {
                size: "20px",
                color: "blue",
                fontWeight: "bold",
                fontFamily: "Segoe UI"
            }
        },
	});
});

{% endhighlight %}

![](Legend_images/Legend_img8.png)