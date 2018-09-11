---
layout: post
title: Scale-Settings
description: scale settings
platform: Typescript
control: Slider
documentation: ug
---

# Scale Settings

**Slider** widget includes option to display the scale on the **Slider**. Scale in **Slider** supports you to easily identify the current value/values of the **Slider**. Scale contains “small ticks” and “large ticks”. Values of the **Slider** is displayed above each large ticks.

## Show Scale

This property enables the scale in the **Slider**. By default, its value is “false”. Data type of this property is “Boolean”.

The following steps explains you the configuration of **showScale** property.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”.

{% highlight html %}

   <div class="txt">Default Slider</div>
   <div id="defaultSlider"></div>
   <br />
   <br />
   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div> 

{% endhighlight %}

{% highlight javascript %}


        // In JavaScript, configure the showScale property as follows.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            sliderType: ej.SliderType.Default,
            value: 60,
            width: "500",
            minValue: 40,
            maxValue: 80,
            showScale: true
        });

       var slider1 = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [10,90],
            width: "500",
            showScale: true
        });
    });
}
{% endhighlight %}

Execute the above code example to render the following output.

![](Scale-Settings_images/Scale-Settings_img1.png) 

## Enable Small Ticks

**Slider** widget provides you an option to enable/disable the small ticks present in the scale. By default, when you enable “showScale” property, small ticks is displayed in the scale. Use the **showSmallTicks** property to disable the small ticks present in the scale. Data type of this property is “Boolean”. The [renderingTicks](https://help.syncfusion.com/api/js/ejslider#events:renderingticks) event will be triggered while creating each slider scale tick.

The following steps explains you on how to disable the small ticks in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”.

{% highlight html %}


   <div class="txt">Default Slider</div>
   <div id="defaultSlider"></div>
   <br />
   <br />
   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div> 


{% endhighlight %}

{% highlight javascript %}

        // In JavaScript, set the value of showSmallTicks property as “false”.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            sliderType: ej.SliderType.Default,
            value: 60,
            width: "500",
            minValue: 40,
            maxValue: 80,
            showScale: true,
            showSmallTicks: false
        });	
        var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [10,90],
            width: "500",
            showScale: true,
            showSmallTicks:false
        });
    });
}

{% endhighlight %}

Execute the above code example to render the following output.


![](Scale-Settings_images/Scale-Settings_img2.png) 

## Small step

This property specifies the distance between the two small ticks present in the scale and the position of the small ticks in the Slider scale. Data type of this property is “number”.

## Large step

This property specifies the distance between the two small ticks present in the scale and the position of the large ticks in the Slider scale. Data type of this property is “number”.

The following steps explains you on how to configure the smallStep and largeStep property in Slider scale.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”

{% highlight html %}


   <div class="txt">Default Slider</div>
   <div id="defaultSlider"></div>
   <br />
   <br />
   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div> 

{% endhighlight %}

{% highlight javascript %}

        // In JavaScript, specify the value for smallStep and largeStep properties.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            sliderType: ej.SliderType.Default,
            value: 60,
            width: "500",
            minValue: 40,
            maxValue: 80,
            showScale: true,
            smallStep: 5,
            largeStep: 20
        });

        var slider1 = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [25,75],
            width: "500",
            showScale: true,
            smallStep: 5,
            largeStep:25
        });
    });
}

{% endhighlight %}

Execute the above code example to render the following output.


![](Scale-Settings_images/Scale-Settings_img3.png) 

In the above example, for “Default Slider” the “**smallStep**” value is specified as “5”, so for each 5 values from the starting value, small ticks is enabled. Also, “**largeStep**” value is specified as “20”, so for each 20 values from the starting value, large ticks is enabled.

Similarly for “Range Slider”, “**smallStep**” value is specifies as “5”, so for each 5 values from the starting value, small ticks is enabled. Also, “**largeStep**” value is specified as “25” so, for each 25 values large ticks is enabled.

