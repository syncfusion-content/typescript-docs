---
layout: post
title: Markers Customization
description: Learn how to add markers to Sparkline.
platform: ts
control: Sparkline
documentation: ug
---

## Marker Customization

You can customize markers by initializing the **markerSettings** property. The customization options allow you to change the **visibility** **fill**, **width**, **opacity**and **border** options **color**, **width**, **opacity** for marker. This customization only applicable for line, column and area type Sparkline.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            markerSettings: {
                visible: true,
                width: 4,
                fill: "#ff14ae",
                border: {
                    width: 1
                }
            }
            // ...
     });
    });
}



{% endhighlight %}

![](Marker-Customization_images/Marker-Customization_img1.png)
