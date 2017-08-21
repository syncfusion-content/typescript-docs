---
layout: post
title: RTL-Support
description: rtl support
platform: Typescript
control: Splitter
documentation: ug
---

# RTL Support

The **Splitter** provides you with **RTL** (**Right-To-Left**) support. The alignment of **Splitter** can be changed from **Left-To-Right** to **Right-To-Left**.

## Enable RTL

The following steps explain enabling the right-to-left property for **Splitter** widget.

In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control.

{% highlight html %}

<div id="outersplitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3"> JavaScript </h3>
        </div>
    </div>
    <div id="innersplitter">
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Tools </h3>
                Essential Tools is an collection of user interface components used to create interactive
                            JavaScript applications.
            </div>
        </div>
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Chart </h3>
                Essential Chart is a business-oriented charting component.
            </div>
        </div>
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Grid </h3>
                Essential JavaScript Grid offers full featured a Grid control with extensive support for
                            Grouping and the display of hierarchical data.
            </div>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module SplitterComponent {
    $(function () {
        var splitterInstance = new ej.Splitter($("#outterSpliter"), {
        height: 250, width: 600,
        orientation: ej.Orientation.Vertical,
        enableRTL: true,
        properties: [{ paneSize: 60 }]
    });
    
  var splitterInstance1 = new ej.Splitter($("#innerSpliter"), {
        width: 600,
        properties: [{ paneSize: 200 }, { paneSize: 170 }]
    });
 }); 
} 

{% endhighlight %}

The output for **Splitter** when **enableRTL** is “**true**”.

![](RTL-Support_images/RTL-Support_img1.png) 









