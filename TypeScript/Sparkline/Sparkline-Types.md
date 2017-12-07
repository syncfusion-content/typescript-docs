---
layout: post
title: Sparkline types
description: What are the different types of Sparkline available in Essential typescript Chart.
platform: ts
control: Sparkline
documentation: ug
---

# Sparkline Types

## Line Type

To render a Line type Sparkline, set the **type** as **line**. To change the color and width of the line, you can use the **fill** and **width** property.	

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            width: 3,
            fill: "#33ccff", 
            // ...
       });
    });
}

{% endhighlight %}

![](Sparkline-Types_images/Sparkline-Types_img1.png)

## Column Type

To render a Column Sparkline, set the type as **column** To change the color of the column, you can use the **fill** property.

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            type: 'column',
            fill: "#33ccff",
            // ...
       });
    });

{% endhighlight %}

![](Sparkline-Types_images/Sparkline-Types_img2.png)

## Area Type

To render an Area Sparkline, you can specify the type as **area**. To change the Area color, you can use the **fill** property

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            type: 'area',
            fill: '#69D2E7
            // ...
       });
    });

{% endhighlight %}

![](Sparkline-Types_images/Sparkline-Types_img3.png)

## WinLoss Type

WinLoss Sparkline render as a column segment and it show the positive, negative and neutral values. You can customize the positive and negative color of the win-loss type.

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
             type: 'winLoss',
            fill: '#69D2E7'
            // ...
       });
    });

{% endhighlight %}

![](Sparkline-Types_images/Sparkline-Types_img4.png)

## Pie Type

You can create a pie type sparkline by setting the type as **pie**. Colors for the pie can be customize using **palette** property.

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            type: 'pie',
            palette: ['#ff3399', "#33ccff"],
            // ...
       });
    });

{% endhighlight %}

![](Sparkline-Types_images/Sparkline-Types_img5.png)
