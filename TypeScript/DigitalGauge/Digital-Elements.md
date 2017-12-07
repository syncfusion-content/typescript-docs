---
layout: post
title: Digital-Elements
description: digital elements
platform: typescript
control: Digital Gauge
documentation: ug
---

# Digital Elements

**Text Customization**

* The attribute `value` refers the text displayed in the **Digital Gauge**. This text is applicable only for that item instead of all items. Text color is changed by using the property `textColor`

* It is possible to align the text inside the **Digital Gauge** control by using the property `textAlign`. Two possible values for text align are as follows

  * left

  * right


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
            items: [{
                // For setting alignment
                textAlign: "right",
                // For setting text
                value: "STOP",
            }]
        })
    });
}

{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](Digital-Elements_images/Digital-Elements_img1.png)

