---
layout: post
title: Axis Customize
description: Learn how to customize axis in Sparkline.
platform: ts
control: Sparkline
documentation: ug
---

## Axis Customize 

The Sparkline axis can be collapsed using visible property in **axisLineSetting** and this not applicable for win-loss. You can customize **color**, **width** and **dash array** of axis line.

 {% highlight javascript %}
 
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            axisLineSettings: {
                visible: true,
                color:"#ff14ae",
            }

            // ...

        });
    });
}

{% endhighlight %}

![](Axis-Customize_images/Axis-Customize_img1.png)