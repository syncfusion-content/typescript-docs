---
layout: post
title: Scales
description: scales
platform: Typescript
control: PivotGauge
documentation: ug
---

# Scale

## Adding scale

The scale can be added to the pivot gauge control.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            radius: 150, 
            showScaleBar: true
        }]
    });
});	

{% endhighlight %}

![](Scales_images/AddingScale.png) 

## Scale customization

### Pointer cap
The pointer cap is a circular shape element located at the center of the pivot gauge. It can be customized with the `pointerCap` property in the scales option. Following are the properties used to customize its appearance.

* **radius**: Sets the radius of the pointer cap.
* **borderColor**: Sets the color of the pointer cap border.
* **borderWidth**: Sets the width of the pointer cap border.
* **backgroundColor**: Sets the background color of the pointer cap.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            radius: 150, 
            showScaleBar: true,
            pointerCap: {
                radius: 5,
                borderWidth: 2,
                borderColor: "green",
                backgroundColor: "yellow"
            }
        }]
    });
});	

{% endhighlight %}

![](Scales_images/PointerCap.png) 

### Appearance
The appearance of the scale can be customized through the following properties:

* **radius**: Sets the radius of the scale.
* **backgroundColor**: Sets the background color of the scale.
* **border**: Sets the border of the scale with color and width properties.
* **size**: Sets the size of the scale.
* **minimum**: Sets the least value of the scale.
* **maximum**: Sets the highest value of the scale.
* **majorIntervalValue**: Sets the interval between minor ticks in the scale.
* **minorIntervalValue**: Sets the interval between major ticks in the scale.
* **direction**: Sets the direction of the scale. By default, it takes clockwise direction.

The `showIndicators`, `showTicks`, `showRanges`, `showPointers`, and `showScaleBar` properties are used to enable/disable the indicators, ticks, ranges, pointers, and scale bar respectively. By default, the `showTicks` and `showPointers` are set to true, and other properties are set to false.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
                radius: 120, showScaleBar: true,
                size: 10,
                backgroundColor: "yellow",
                border: {
                    width: 3,
                    color: "blue"
                },
                minimum: 20,
                maximum: 120,
                majorIntervalValue: 20,
                minorIntervalValue: 5,
                direction: "counterClockwise"
        }]
    });
});	

{% endhighlight %}

![](Scales_images/Appearance.png) 