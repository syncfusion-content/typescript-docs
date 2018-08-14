---
layout: post
title: Updating-slider-value
description: updating slider value
platform: Typescript
control: Slider
documentation: ug
---

# Updating slider value

**Slider** widget includes an option to specify/update its value. And also you can specify the starting and ending value for the **Slider** using the **minValue** and **maxValue** properties.

## Value

This property is used to set the value in the “**Default**” and “**Min-Range**” Sliders. By default its value is null when no value is specified. Data type of this property is “**number**”.
You can get/set the value in the slider handle by using [getValue](https://help.syncfusion.com/api/js/ejslider#methods:getvalue) and [setValue](https://help.syncfusion.com/api/js/ejslider#methods:setValue) methods.
Also [change](https://help.syncfusion.com/api/js/ejslider#events:change) event will be triggered whenever **Slider** value is changed.

## Values

This property is used to set the value in “**Range Slider**”. By default range values is from 0 to 100. This property is of “**Array**” data type.

The following steps explains you the configuration of “**value**” and “**values**” property.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “**Range Slider**” and “**Default Slider**”.



{% highlight html %}

<div class="txt">Default Slider</div>
<div id="defaultSlider"></div>
<br />
<br />
<div class="txt">Range Slider</div>
<div id="rangeSlider"></div>


{% endhighlight %}

{% highlight javascript %}

        // When initializing Slider widget, configure the “value” and “values” property as follows.	    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#minSlider"), {
            sliderType: ej.SliderType.Default,
            value: 50,
            width: "500"
        });

        $("#rangeSlider").ejSlider({
            sliderType: ej.SliderType.Range,
            values: [20,80],
            width: "500"
        });
    });
}

{% endhighlight %}

Execute the above code example to render the following output.


![](Updating-slider-value_images/Updating-slider-value_img1.png) 

## MinValue

To set the minimum/starting value of the Slider, you can use the minValue property. By default its value is 0. Data type of this property is “**number**”.

## MaxValue

To set the maximum/ending value of the Slider, you can use the maxValue property. By default its value is 100. Data type of this property is “**number**”.

The following steps explains you on how to configure minValue and maxValue property.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Default Slider** and **Range Slider**.

{% highlight html %}

   <div class="txt">Default Slider</div>
   <div id="defaultSlider"></div>
   <br />
   <br />
   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div> 

{% endhighlight %}

{% highlight javascript %}


        // When initializing Slider widget, configure the minValue and maxValue properties as follows.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            sliderType: ej.SliderType.Default,
            value: 60,
            width: "500",
            minValue: 40,
            maxValue:80
        });
        
    var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [10,90],
            width: "500",
            minValue: 10,
            maxValue:90
        });
    });
 }

{% endhighlight %}

Execute the above code example to render the following output.

![](Updating-slider-value_images/Updating-slider-value_img2.png)

In the above example, for **Default Slider** the slider value starts from “40” (min value) and ends in “80” (max value), so the slider handle is placed at the center of the Slider while specifying the value as “60”.

For **Range Slider**, the value starts from “10” (min value) and ends in “90” (max value). The range shadow occupies the entire **Slider**, since the range (values) is specified as “[10, 90]”.

## Buttons

**Slider** includes the button support for increment or decrement the values of the slider.

### Enabling Buttons

Use the **showButtons** property to enable the button support. By default this property is disabled. Data type of this property is “Boolean”.

The following steps explains you on how to enable button support in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Range Slider.**



{% highlight html %}

   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div>


{% endhighlight %}

{% highlight javascript %}

        // In JavaScript, when initializing the Slider, specify the value for “showButtons” property as “true” 
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [30,60],
            width: "500",
            showButtons:true
        });
    });
}


{% endhighlight %}

Execute the above code example to render the following output.

![](Button-Support_images/Button-Support_img1.png)
