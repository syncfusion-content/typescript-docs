---
layout: post
title: Frame Type
description: frame type 
platform: Typescript
control: PivotGauge
documentation: ug
---

# Frame type

## Full circle

The full circle frame is used to display the pivot gauge in circular shape. The frame type can be set by using the `frameType` property. By default, the frame type is "FullCircle".

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), { 
        frame: {
            frameType: "fullcircle"
        },
    });
});	

{% endhighlight %}

![](Frame-Type_images/FullCircle.png)

## Half circle
The half circle frame is used to display the pivot gauge in semi-circular shape. For this, set the frame type to "HalfCircle" within the `frameType` property, and then set the `startAngle` and `sweepAngle` for the pivot gauge in the `scales` property.


{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), { 
        frame: {
            frameType: "halfcircle",
            halfCircleFrameStartAngle: 180,
            halfCircleFrameEndAngle: 360
        },
        scales: [{
            startAngle: 180,
            sweepAngle:180
        }]
    });
});	

{% endhighlight %}

![](Frame-Type_images/HalfCircle.png)
