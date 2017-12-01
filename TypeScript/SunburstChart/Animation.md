---
layout: post
title: Animation
description: Learn how to animate the SunburstChart .
platform: ts
control: SunburstChart
documentation: ug
---

# Animation

Sunburst chart allows you to animate the chart segments. You can enable animation using **enableAnimation** property. 

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {
    $(function () {
        var sunburstsample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
           enableAnimation: true

            // ...

        });
    });
}

## Animation Types 
Sunburst chart provide options to animate the chart segments in different ways using **animationType** property.

FadeIn – It gradually changes opacity of the chart segment.
Rotation – During an animation, control rotate from 0 to 360 angle.

### Fade In

The Fade In animation is enabled as follows 

{% highlight ts %}

$(function () {
        var sunburstsample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
          enableAnimation: true,
          animationType:"fadeIn"

            // ...

        });
    });

{% endhighlight %}

![](Animation_images/Animation_img2.gif)

### Rotation

The following example shows how to enable rotation animation in ejSunburstChart

{% highlight ts %}

$(function () {
        var sunburstsample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
          enableAnimation: true,
          animationType:"rotation"

            // ...

        });
    });


{% endhighlight %}

![](Animation_images/Animation_img1.gif)


