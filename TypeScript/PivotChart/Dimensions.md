---
layout: post
title: Dimensions
description: dimensions
platform: Typescript
control: PivotChart
documentation: ug
---

# Dimensions

## Set size in percentage

You can customize the pivot chart dimension by setting the width and height of the control in percentage.

{% highlight ts %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		size: {
            height: "80%",
            width: "80%"
        },
	});
});
{% endhighlight %}

{% highlight html %}
    <style>
        #PivotChart1 {
            width:100%;
            height:450px;
        }
    </style>

{% endhighlight %}

## Set size in pixels

You can customize the pivot chart dimension by setting the width and height of the control in pixels.

{% highlight ts %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		size: {
            height: "460px",
            width: "950px"
        },
	});
});
{% endhighlight %}

{% highlight html %}
    <style>
        #PivotChart1 {
            width:950px;
            height:460px;
        }
    </style>

{% endhighlight %}

![](Dimensions_images/Dimensions.png) 

## Responsive

The pivot chart control supports responsive rendering based on the target device (desktop and tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in the pivot chart by setting the `IsResponsive` property to true.

{% highlight ts %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
        isResponsive: true,
		size: {
            height: "460px",
            width: "950px"
        },
	});
});
{% endhighlight %}

{% highlight html %}
    <style>
        #PivotChart1 {
            min-height: 275px; 
            min-width: 525px; 
            height: 460px; 
            width: 100%;
        }
    </style>

{% endhighlight %}

![](Dimensions_images/NormalView.png)

_Normal View_

![](Dimensions_images/ResponsiveView.png)

_ResponsiveView_