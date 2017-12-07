---
layout: post
title: Sunburst Zooming
description: Learn how to Zoom the SunburstChart for better data visualization
platform: ts
control: SunburstChart
documentation: ug
---

# Zooming

Sunburst chart provides zooming (drill down) experience with animation for both mouse and touch enabled devices. It allows you to virtualizing the large sets of data into minimum data view.The zooming is achieved by using the property of **zoomSettings**

The following code shows how to initialize the zooming.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          
          //..
          zoomSettings: { enable: true },	           
         //..

        });
    });
}

{% endhighlight %}

![](Zooming_images/Zooming_img1.gif)

## Zooming toolbar
By default, zooming toolbar will be enabled while zooming the segment.It contains both back and reset option.
You can align the zooming toolbar position by using **toolbarHorizontalAlignment** and **toolbarVerticalAlignment**property.


{% highlight javascript %}

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          
          //..
          zoomSettings: {enable: true,toolbarHorizontalAlignment: "left"},	           
         //..

        });
    });

{% endhighlight %}

![](Zooming_images/Zooming_img2.png)


