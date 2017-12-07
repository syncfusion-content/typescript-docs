---
layout: post
title: Sub-Gauges
description: sub gauges
platform: typescript
control: Circular Gauge
documentation: ug
---

# Sub Gauges

A **Circular Gauge** containing another circular gauge is said to be `subGauges`. In order to make a sample like watch that has second gauge, minute gauge and hour gauge, sub gauges are used.

## Adding SubGauges

Sub gauge collection is directly added to the scale object. Refer the following code example to add custom sub gauge collection in a **Gauge** control.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {

 $(function () {
        //For circular gauge rendering
            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            scales: [{ showSubGauges: true,
                subGauges:[{
                    gaugeID: "Gauge1"
                }]
    }]
    })
    });
}

{% endhighlight %}

**Basic Customization**

Basic attributes such as `height` and `width` property are used to set height and width of the sub gauge. You can easily position the gauge in another gauge using the `position` object and by giving the `x` and `y` Coordinates value. **controlID** attribute is used to specify the sub gauge ID.



{% highlight html %}

<div id=" SubGauge1"></div>
<div id="CircularGauge1"> </div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
           var circularGauge = new ej.datavisualization.CircularGauge($("#SubGauge1"),{
            backgroundColor: "Blue",value:50, radius: 110,
            scales: [{
                radius: 110,
            }]
        });
           var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            height: 500,value:50, width: 500,
            scales: [{radius:190,
                subGauges:[{
                    //For setting sub gauge control ID
                    controlID: "SubGauge1",
                    //For setting sub gauge height
                    height:250,
                    //For setting sub gauge width
                    width: 250,
                    //For setting sub gauge position
                    position: { x: 150, y: 100 }
                }]
            }]
        });    });


{% endhighlight %}



Execute the above code to render the following output.

![](Sub-Gauges_images/Sub-Gauges_img1.png)

## Multiple SubGauges

You can set multiple sub gauges in a single **Circular Gauge** by adding an array of sub gauge objects. Refer the following code example for multiple sub gauges functionality.


{% highlight html %}

<div id="CircularGauge1"></div>
<div id=" SubGauge1"> </div>
<div id=" SubGauge2"> </div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
         var circular = new ej.datavisualization.CircularGauge($("#SubGauge1"),{
            backgroundColor: "#f5b43f",
            scales: [{
                radius: 150
            }]
        });
         var circularGauge = new ej.datavisualization.CircularGauge($("#SubGauge2"),{
            backgroundColor: "#f5b43f",
            scales: [{
                radius: 150
            }]
        });
          var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            height: 500,
            width: 500,
            scales: [{
                radius:250,
                subGauges:[
                //Sub gauge1
                {
                    controlID: "SubGauge1",
                    height:200,
                    width: 200,
                    position: { x: 200, y: 150 }
                },
                //Sub gauge2
                {
                    controlID: "SubGauge2",
                    height: 200,
                    width: 200,
                    position: { x: 50, y: 200 }
                }]
            }]
        });    });


{% endhighlight %}



Execute the above code to render the following output.

![](Sub-Gauges_images/Sub-Gauges_img2.png)

