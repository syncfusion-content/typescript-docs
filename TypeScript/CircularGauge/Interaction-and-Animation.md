---
layout: post
title: Interaction-and-Animation
description: interaction and animation
platform: typescript
control: Circular Gauge
documentation: ug
---

# Interaction and Animation

**Interaction**

**Circular Gauge** control contains **Interaction** feature. You can use this interaction feature to change the pointer values manually. You can achieve this by clicking and dragging the pointer over the **Gauge** and you can see the value of pointer changes dynamically while dragging. To Enable/Disable the user interaction you can use the Boolean property called `readOnly`. The user interaction option is enabled when you set the value as false for the property **readOnly**.By default it holds the true value.That is by default it does not support interaction. 

{% highlight html %}


  <div id="CircularGauge1">  </div>  


{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {

$(function () {
        // For Circular Gauge rendering
        var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // For User interaction
            readOnly: false,
        })
    });

}
   
{% endhighlight %}

Execute the above code to render the following output.

![](Interaction-and-Animation_images/Interaction-and-Animation_img1.png)

**Animations**

**Circular Gauge** contains an attractive concept called **Animation**. The animation option enables the pointer to rotate from the minimum value to the current value with animation effects. By using this animation you can change the pointer value dynamically.You can apply the animation on  pointer either by clockwise or counterclockwise based on the scale direction. You can enable / disable it using the property `enableAnimation`. Animation is enabled when you set **enableAnimation** as ‘true’. By default it holds the true value. You can control the speed of the pointer during animating by using the property `animationSpeed`. It is a numerical value that holds the time in milliseconds. That is when the value is given as 1000, it is considered as 1 second.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
        // For Circular Gauge rendering
      var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // For enabling animation
        enableAnimation: true,
            // For setting animation speed
        animationSpeed:1000
        })
    });

{% endhighlight %}


Execute the above code to render the following output.

![](Interaction-and-Animation_images/Interaction-and-Animation_img2.png)

**Gradient**

You can change the interior gradient of circular gauge by using `interiorGradient` property. The `isRadialGradient` property is used to check whether the gradient is circular or not.  

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
       var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{       
        interiorGradient: { colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] },
        isRadialGradient : true,
        })
    });

{% endhighlight %}

**Distance From Corner**

You can display the circular gauge from distance apart from the corner by specifying value for `distanceFromCorner` property. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
      var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{        
        distanceFromCorner :25
        })
    });

{% endhighlight %}

**Resize**

Circular gauge can be responsive while resizing by specifying `enableResize` property as true. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
     var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{        
            enableResize: true
        })
    });

{% endhighlight %}

**Localization**

The circular gauge can be localized based on name of culture specified in `locale` property.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

$(function () {
       var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{        
           locale : "en-US"
        })
    });

{% endhighlight %}

**Themes**

**CircularGauge** theme is a set of pre-defined options that are applied to the control before **CircularGauge** is instantiated. Following predefined themes are available in JavaScript **CircularGauge**.

1. flat light
2. flat dark
3. gradient light 
4. gradient dark 
5. azure                      
6. azure dark               
7. lime 
8. lime dark
9. saffron
10. saffron dark
11. gradient azure
12. gradient azure dark
13. gradient lime
14. gradient lime dark
15. gradient saffron
16. gradient saffron dark

The theme for circular gauge can be specified using `theme` property.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
       var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{     
            theme : "flatlight"
        })
    });

{% endhighlight %}

**Circular Gauge Values**

The `minimum`, `maximum`, `radius` and `value` attributes of circular gauge are used to render the circular gauge with specified location. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
       var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{          
            maximum: 120,
            minimum: 10,
            value: 30,
            radius: 100
        })
    });

{% endhighlight %}
