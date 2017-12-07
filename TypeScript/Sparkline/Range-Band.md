---
layout: post
title: RangeBand
description: Learn how to add Rangeband to Sparkline .
platform: ts
control: Sparkline
documentation: ug
---

## Range Band  

The **range band** feature is used to highlight a particular range along the y-axis using **start** and **end** range property. You can also customize the **color** and **opacity** of the range band. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
           
            rangeBandSettings:{
                startRange:4,
                endRange:30,
                color:"#ff14ae",
                opacity:0.4
            },

            // ...
       });
    });
}

{% endhighlight %}

![](Range-Band_images/Range-Band_img1.png)

