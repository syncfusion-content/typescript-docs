---
layout: post
title: Orientation
description: orientation
platform: Typescript
control: Slider
documentation: ug
---

# Orientation

This property is used to set the **Slider** in either horizontal or vertical direction. By default, **Slider** renders in horizontal direction. Data type of this property is “enum”.

Possible **Slider** orientations are as follows,

Property Table for JavaScript

<table>
<tr>
<th>
Property</th><th>
Allowed values</th><th>
Description</th></tr>
<tr>
<td rowspan = "2">
orientation</td><td>
ej.Orientation.Vertical</td><td>
Displays the Slider in vertical direction</td></tr>
<tr>
<td>
ej.Orientation.Horizontal (default value)</td><td>
Displays the Slider in horizontal direction</td></tr>
</table>


The following steps explains you on how to configure the **orientation** property.

In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.



{% highlight html %}


   <div id="ejSlider"></div>

{% endhighlight %}

{% highlight javascript %}

  // When initializing the Slider widget, configure the orientation property as follows.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#ejSlider"), {
            height: "150",
            width: "20",
            orientation:ej.Orientation.Vertical
        });
    });
 }

{% endhighlight %}

Execute the above code example to render the following output.

![](Orientation_images/Orientation_img1.png) 



