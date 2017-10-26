---
layout: post
title: Persistence-Support
description: persistence support
platform: Typescript
control: Slider
documentation: ug
---

# Persistence Support

This feature supports you to save current model value to browser cookies for state maintenance. When you refresh the web page, the **Slider** control retains the model value apply from browser cookies. The data type of **enablePersistence** is Boolean type. 

The following steps explain you on how to enable the **enablePersistence** property.

In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.

{% highlight html %}


   <div id="ejSlider"> </div>

{% endhighlight %}


{% highlight javascript %}


        // When initializing the Slider widget, enable the enablePersistence property as follows.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#ejSlider"), {
            height: "15",
            width: "500",
            enablePersistence:true
        });
    });
}

{% endhighlight %}

