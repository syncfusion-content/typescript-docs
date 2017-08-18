---
layout: post
title: Splitter-Orientation
description: splitter orientation
platform: Typescript
control: Splitter
documentation: ug
---

# Splitter Orientation

The **Splitter** supports both vertical and horizontal orientation of the pane. You can declare the orientation by using **enum**, **ej.Orientation.Vertical** or **ej.Orientation.Horizontal**, that have the corresponding value of vertical and horizontal as a string.

## Configure Splitter Orientation

The following steps explain the implementation of **Splitter** orientation option.

In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** widget. 

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
            ASP.NET MVC applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential MVC Grid offers full featured a Grid control with extensive support for
            Grouping and the display of hierarchical data.
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

module SplitterComponent {
    $(function () {
        var splitterInstance = new ej.Splitter($("#spliter"), {
            height: 280, width: 600,
            orientation: ej.Orientation.Vertical,
        });  
    });
}  

{% endhighlight %}


The output for **Splitter** with **ej.Orientation.Vertical**.

![](Splitter-Orientation_images/Splitter-Orientation_img1.png) 

The output for **Splitter** with **ej.Orientation.Horizontal**.

![](Splitter-Orientation_images/Splitter-Orientation_img2.png) 

