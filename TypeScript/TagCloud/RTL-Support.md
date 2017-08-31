---
layout: post
title: RTL-Support
description: rtl support
platform: Typescript
control: TagCloud
documentation: ug
---

# RTL Support

This feature supports you to change the left-to-right alignment of the **TagCloud** widget to right-to-left (RTL). This displays the content from right-to-left in the widget. You can achieve this using **enableRTL** property that is set false by default.

## Enabling RTL Support

The following steps explains you the enabling of right-to-left property in **TagCloud**.

 In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

 <div id="website"></div>

{% endhighlight %}

{% highlight javascript %}


    // Enable RTL property for TagCloud.  
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TagCloudComponent {
$(function () {
    var sample = new ej.TagCloud($("#website"), {
       enableRTL:true,
        titleText: "Tech Sites",
        dataSource: websiteCollection
    });
 });
}

{% endhighlight %}

The following screenshot illustrates the **TagCloud** control with RTL support.



![](RTL-Support_images/RTL-Support_img1.png) 



