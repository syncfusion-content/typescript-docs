---
layout: post
title: RTL-Support
description: rtl support 
platform: Typescript
control: Uploadbox
documentation: ug
---

# RTL Support 

This feature supports the change of left-to-right alignment of the **Uploadbox** widget to right-to-left (**RTL**). That is, it sets the **Uploadbox** to right-to-left actions.

The following steps explain the configuration of **enableRTL** property in **Uploadbox**. 

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}

<div class="control">
    <div id="Uploadbox"></div>
</div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module UploadboxComponent {
    $(function () {
        var sample = new ej.Uploadbox($("#Uploadbox"),{
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            enableRTL: true
        });
    });
}
{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



![](RTL-Support_images/RTL-Support_img1.png) 



