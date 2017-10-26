---
layout: post
title: RTL-support
description: rtl support
platform: Typescript
control: Slider
documentation: ug
---

# RTL support

**Slider** includes the Right to Left alignment support. Operations in the **Slider** is performed from Right to Left.

## Enabling RTL

Use the **enableRTL** property to enable the RTL support. By default this property is disabled. Data type of this property is “Boolean”.

The following steps explains you on how to enable RTL support in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Range Slider.**



{% highlight html %}

   <div class="txt">Range Slider</div>
   <div id="rangeSlider"></div>


{% endhighlight %}

{% highlight javascript %}

        // In JavaScript, when initializing the Slider, specify the value for “enableRTL” property as “true” 
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [25,75],
            width: "500",
            enableRTL:true
        });
    });
}


{% endhighlight %}

Execute the above code example to render the following output.


![](RTL-support_images/RTL-support_img1.png)