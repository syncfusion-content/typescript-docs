---
layout: post
title: Date-in-other-months
description: date in other months
platform: TypeScript
control: DateTimePicker
documentation: ug
---

# Date in other months

**DateTimePicker** calendar can display the dates in other months at the start or end of the current month. To enable or disable the display of other month dates in the current month, you can use the property called **showOtherMonths**. By setting this property value as **“true”** you can display the dates in other months at the start or end of the current month. By default the value of this property is **“true”**. 

Consider you are going to calculate the monthly report of your company’s employee attendance. To avoid the mistake of selecting other month dates while calculating current month report, you can disable showing other month dates in the current month. You can achieve this requirement by setting **showOtherMonths** value as **“false”.**

Add the following code in your **HTML** page.


{% highlight html %}
  
<div class="control">
   <input type="text" id="datetime" />
</div>

{% endhighlight %}


{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateTimePickerComponent {
    $(function () {
    //  Add the code in your script section to render DateTimePicker without displaying other month dates in current month
    var datetimeSample = new ej.DateTimePicker($("#datetime"), {
       showOtherMonths: false,
       width: '200px',
    });
    });
}

{% endhighlight %}
  
![](Date-in-other-months_images/Date-in-other-months_img1.png)

