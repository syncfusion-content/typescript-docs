---
layout: post
title: Point Customization
description: Learn how to customize points in Sparkline.
platform: ts
control: Sparkline
documentation: ug
---

## Point Customization

You can customize points by initializing the point colors. The customization options allow you to differentiate the **first**, **last**, **highest**, **lowest**, and **negative** points. This customization only applicable for line, column and area type Sparkline.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            // ...
            negativePointColor: "red",
            highPointColor: "blue",
            lowPointColor: "orange",
            startPointColor: "green",
            endPointColor: "green",
            // ...
        });
    });
}

{% endhighlight %}

![](Point-Customization_images/Point-Customization_img1.png)