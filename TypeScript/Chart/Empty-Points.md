---
layout: post
title: Empty Points 
description: How to show or hide an empty point in Essential Typescript Chart.
platform: typescript
control: Chart
documentation: ug
---

# Empty Points 

The Data points that uses the **null** or **undefined** as value are considered as empty points. Empty data points are ignored and not plotted in the Chart. When the data is provided by using the [`points`](../api/ejchart.html#members:series-points) property, you can set the **isEmpty** to true to specify that the particular point is an empty point.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
               series:[ {
                     //Using empty points 
                     points: [
                              { x: 0, y: 210 }, 
                              { x: 1, y: null }, { x: 2, y: 150 },
                              { x: 3, y: 180,isEmpty: true }, 
                              { x: 4, y: 170},
                              { x: 5, y: 200 }, 
                              { x: 6, y: 140, isEmpty: true },
                              { x: 7, y: 120 }, { x: 8, y: 140 } 
                          ],
             }],

            // ...
       });

{% endhighlight %}

![](Empty-Points_images/Empty-Points_img1.png)

## EmptyPointSettings

You can customize the empty points visibility and change its [`displayMode`](../api/ejchart.html#members:series-emptyPointSettings-displayMode) *(gap, zero and average)* using [`emptyPointSettings`](../api/ejchart.html#members:series-emptyPointSettings) option.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                
            series:[ {
                   //...
                   emptyPointSettings: {
                       // visible the empty point settings with displayMode as average
                       visible: true,
                       displayMode : "average"
                     }, 
                }],

            // ...
       });

{% endhighlight %}

![](Empty-Points_images/Empty-Points_img2.png)


If the [`visible`](../api/ejchart.html#members:series-emptyPointSettings-visible) property of [`emptyPointSettings`](../api/ejchart.html#members:series-emptyPointSettings) is *false*, then the empty points has been dropped and chart will be rendered without empty points.

![](Empty-Points_images/Empty-Points_img3.png)

## Customizing Styles

Empty points color and border can be customized using [`style`](../api/ejchart.html#members:series-emptyPointSettings-style) property of [`emptyPointSettings`](../api/ejchart.html#members:series-emptyPointSettings).

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                   //...
                   emptyPointSettings: {
                       visible: true,
                       //Customizing empty points styles
                       style: {
                           color: "#ffa000",
                           border:{
                               color: "gray",
                               width:2
                            }
                        }
                     }, 
                }],

            // ...
       });

{% endhighlight %}

![](Empty-Points_images/Empty-Points_img4.png)