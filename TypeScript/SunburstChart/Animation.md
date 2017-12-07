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

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {
    $(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
           enableAnimation: true

            // ...

        });
    });
}

{% endhighlight %}

## Animation Types 
Sunburst chart provide options to animate the chart segments in different ways using **animationType** property.

FadeIn – It gradually changes opacity of the chart segment.
Rotation – During an animation, control rotate from 0 to 360 angle.

### Fade In

The Fade In animation is enabled as follows 

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
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

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
          enableAnimation: true,
          animationType:"rotation"

            // ...

        });
    });


{% endhighlight %}

![](Animation_images/Animation_img1.gif)


