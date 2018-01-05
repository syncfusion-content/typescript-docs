---
layout: post
title: Right-to-Left
description: right-to-left
platform: TypeScript
control: DateTimePicker
documentation: ug 
---

# Right-to-Left

RTL control supports right-to-left functionality and features for languages that work right-to-left for selecting and editing date and time. You can change your popup and textbox display to read right-to-left. Arabic and Hebrew are written from right to left. The customer who has a right to left writing style can use this feature. You can achieve this in your **DateTimePicker** by using **enableRTL** property. Setting this property to “**true**”allows you to write in the right to left format. Position of the toolbars are also changed to right to left.

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
    // Add the code in your script section to render DateTimePicker with right to left appearance
     var datetimeSample = new ej.DateTimePicker($("#datetime"), {
       width: 200,
       enableRTL: true
    });
    });
}

{% endhighlight %}
  
![](Right-to-Left_images/Right-to-Left_img1.png)

