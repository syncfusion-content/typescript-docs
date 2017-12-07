---
layout: post
title: Gauge-Position
description: gauge position
platform: typescript
control: Circular Gauge
documentation: ug
---

# Gauge Position

**Semi-circular Gauge** can be positioned within the canvas element which provides better appearance for the gauge in the canvas.

**Positioning**

Semi-circular Gauge can be positioned with the help of the attribute called `gaugePosition`. It is an enumerable value. You can position the gauge away from the corner with the help of the distanceFromCorner attribute. 

The possible enum values for the gaugePosition are as follows:

* Top left

* Top center

* Top right

* Middle left

* Center

* Middle right

* Bottom left

* Bottom center

* Bottom right

{% highlight html %}

<div style="float: left" id="gauge1"></div>
<div id=" CoreCircularGauge "></div>

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {

 $(function() {
     var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
         backgroundColor: "transparent",
         // To set dimension of the canvas.
         width: 800,
         height: 500,
         // To set the value and radius of the canvas frame.
         radius: 120,
         value: 60,
         // To set the gauge position.
         gaugePosition: "center",
         // To set the distance from the corner.
         distanceFromCorner: 30,
         // To set the semicircle frame specifications.
         frame: {
             frameType: 'halfcircle',
             halfCircleFrameStartAngle: 270,
             halfCircleFrameEndAngle: 90
         },
         // To set the scale specification.
         scales: [{
             startAngle: 270,
             sweepAngle: 180,
             radius: 160,
             showScaleBar: true,
             size: 1,
             maximum: 120,
             majorIntervalValue: 20,
             minorIntervalValue: 10,
             border: {
                 width: 0.5,
             }
         }]
     });
 });

}

{% endhighlight %}



Execute the above code to render the following output.

![](Gauge-Position_images/Gauge-Position_img1.png)

