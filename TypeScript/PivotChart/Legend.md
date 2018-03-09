---
layout: post
title: Legend
description: legend
platform: Typescript
control: PivotChart
documentation: ug
---

# Legend

## Legend Visibility

You can enable or disable legend using the `visible` property inside the `legend` object.

N> By default, the legend is visible in PivotChart.

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

## Legend Shape
You can customize the legend `shape` in PivotChart control. Default value of legend shape is “Rectangle”. Following legend shapes that are supported:

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

## Legend Position
By using the `position` property, you can place the legend at top, bottom, left or right of the PivotChart. 

N> Default value of legend position is "bottom" in PivotChart.

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

## Legend Title
To add the legend title, you have to specify the title text in `title.text` property.

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

## Legend Alignment
You can align the legend to center, far and near based on its position in the Chart area using the `alignment` option.
 
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

## Legend Items - Size and Border
By using the legend `itemStyle.width`, `itemStyle.height` and `itemStyle.border` properties, you can change the legend items - size and border.

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
 
## Legend Border
By using the `border` option in legend, you can customize border color and width.

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

## Legend Text
By using the `font` option, you can customize the font family, font style, font weight and size of the legend text. 

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