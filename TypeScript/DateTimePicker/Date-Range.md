---
layout: post
title: Date-Range
description: date range
platform: TypeScript
control: DateTimePicker
documentation: ug
---

# Date Range

**Date Range** between two dates is achieved by **minDateTime**, **maxDateTime** property of **DateTimePicker**.

In **DateTimePicker**, a property called **enableStrictMode** is available. When this property is set to false, it does not allow wrong values and corrects the entered value automatically. If it is true, then **DateTimePicker** allows values with error class to indicate the selected date is wrong.

**minDateTime** - Sets the minimum value to the **DateTimePicker**. Based on the **enableStrictMode** value behind the minimum value an error class is added to the wrapper element or it is corrected automatically to the nearest correct date value.

**maxDateTime** - Sets the maximum value to the **DateTimePicker**. Based on the **enableStrictMode** value beyond the maximum value an error class is added to the wrapper element or it is corrected automatically to the nearest correct date value.

Sometimes, you can give restrictions on selecting the date before or after the particular date. Consider you are going to make a project for hotel reservation system. The “**In DateTime**” has to be lesser than the “**Out DateTime**” and vice versa. So you have to set “**In DateTime**” as minimum **DateTime** and “**Out DateTime**” as maximum **DateTime** for selection in **DateTimePicker** control. 

The dates before min date and after the max date are considered as invalid dates and it is disabled for selection. 

In the following example September 10, 2014 2.00 PM is set as **minDateTime** and September 21, 2014 2.00 PM set as **maxDateTime.**

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
    // Add the code in your script section to render the DateTimePicker with fixed minimum and maximum date and time
    var datetimeSample = new ej.DateTimePicker($("#datetimepick"), {
       width: 200,
       minDateTime: "9/10/2014 2:00 PM",
       maxDateTime: "9/21/2014 2:00 PM",
    });
 });
}

{% endhighlight %}


![](Date-Range_images/Date-Range_img1.png)

