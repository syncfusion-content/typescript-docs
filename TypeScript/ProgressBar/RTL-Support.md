---
layout: post
title: RTL-Support
description: rtl support
platform: TypeScript
control: ProgressBar
documentation: ug
---

# RTL Support

Right-to-left starts from the right of the page and continues to the left. By default, this option is set to ‘**false**’ in the ProgressBar control. The **enableRTL** option allows the ProgressBar control to display it in the right to left direction.

The following steps explain how to **enable** the **RTL** property of the ProgressBar control.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}

<div class="control">
   <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}

        
        // Add the following code example to enable the RTL property of the ProgressBar control.        
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ProgressBarComponent {
    $(function () {
        var sample = new ej.ProgressBar($("#progressbar"),{
            enableRTL: true,
            value: 80,
            text: 80,
            height: 20,
            width: 500
        });
        sample.setModel({ text: progress.getValue() + " % Completed" });
        });
}

{% endhighlight %}


The following screenshot displays the output.

![](RTL-Support_images/RTL-Support_img1.png) 























