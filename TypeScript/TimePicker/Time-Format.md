---
layout: post
title: Time-Format
description: time format
platform: TypeScript
control: TimePicker
documentation: ug
---

# Time Format

**TimePicker** widget provides you an option to change the time format.

## Steps to change Time Format of TimePicker widget

The following steps explains you to change the time format for the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
    // Change time format for TimePicker controls as follows.
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
            timeFormat: "h:mm:ss tt"
        });
    });
}
    
{% endhighlight %}


Execute the above code to render the following output.



![](/js/TimePicker/Time-Format_images/Time-Format_img1.png) 

