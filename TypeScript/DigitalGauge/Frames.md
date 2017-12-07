---
layout: post
title: Frames
description: frames
platform: typescript
control: Digital Gauge
documentation: ug
---

# Frames

## Inner and Outer Width Customization

`Frames` are space that enclose the **Digital Gauge**. The inner width of the `Frame` is the distance between the canvas element and the frame. The outer width is the distance from the frame. The code example to set frame’s `innerWidth` and `outerWidth` is as follow.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module DigitalGaugeComponent {

 $(function () {
        // For Digital Gauge rendering
       var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
            // For setting text
            value: "WELCOME",
            frame: {
                // For setting inner width
                innerWidth: 6,
                // For setting outer width
                outerWidth: 10,
            },
        })
    });
}

{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

![](Frames_images/Frames_img1.png)



## Setting Background Image

For a better appearance, you can set the `background image` for the **Digital Gauge** using the property **backgroundImageUrl.** 

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function() {
     // For Digital Gauge rendering
   var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
         // For setting text
         value: "RADAR",
         height: 300,
         frame: {
             // For setting background image
             backgroundImageUrl: "board3.jpg",
         },
         items: [{
             position: {
                 x: 95,
                 y: 10
             }
         }]
     })
 });

{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.

![](Frames_images/Frames_img2.png)

