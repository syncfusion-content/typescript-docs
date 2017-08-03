---
layout: post
title: Range
description: range
platform: TypeScript
control: TimePicker
documentation: ug
---

# Range

**TimePicker** widget provide options to set the Range (minTime & maxTime) for the time.

## Steps to change minTime & maxTime of the TimePicker

The following steps explains you to change the Range of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
    // Use minTime and maxTime property to change the Range of the TimePicker.
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
            minTime: "10:00 AM",
            maxTime: "9:00 PM"
        });
    });
}
    
{% endhighlight %}


Execute the above code to render the following output.



![](Range_images/Range_img1.png) 

