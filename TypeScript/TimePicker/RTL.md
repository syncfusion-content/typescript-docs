---
layout: post
title: RTL
description: rtl
platform: TypeScript
control: TimePicker
documentation: ug
---

# RTL

This feature supports to change the left-to-right alignment of the **TimePicker** widget to right-to-left(**RTL**). The custom template **TimePicker** also supports **RTL**.

## Enabling Right-To-Left Support

The following steps explains you in enabling the right-to-left property for the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.   

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
    // Enable RTL for TimePicker controls as follows.
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
            enableRTL: true
        });
    });
}
    
{% endhighlight %}


The following screenshot illustrates a **TimePicker** control when **enableRTL** is set to **“true”**

![](RTL_images/RTL_img1.png) 

