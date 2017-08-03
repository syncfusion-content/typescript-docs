---
layout: post
title: Time-Interval
description: time interval
platform: TypeScript
control: DateTimePicker
documentation: ug 
---

# Time Interval

You can set time interval between two adjacent time values in the time popup manually using the **interval** property. By default the value of the **interval** property is 30 minutes. Setting this value as 60 is considered as 1 hour. Sometimes you need to update for every hour work log reports. In that case to select time from time popup window with 1 hour interval to update the every 1 hour report you can use **interval** option by setting time interval value as “60 minutes”.

Add the following code in your **HTML** page.



{% highlight html %}
  
<div class="control">
   <input type="text" id="dateTime" />
</div>

{% endhighlight %}


{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateTimePickerComponent {
    $(function () {
    // Add the code in your script section to render DateTimePicker with 1 hour interval between two adjacent times in time picker popup
     var datetimeSample = new ej.DateTimePicker($("#datetimepick"), {
       interval: 60,
       width: '200px',
    });
    });
}

{% endhighlight %}

![](Time-Interval_images/Time-Interval_img1.png)

