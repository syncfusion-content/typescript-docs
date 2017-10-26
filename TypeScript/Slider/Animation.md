---
layout: post
title: Animation
description: animation
platform: Typescript
control: Slider
documentation: ug
---

# Animation

This feature includes the animation effect for the **Slider** when moving the **Slider** handle.

## Enabling Animation

By default, animation is enabled in the **Slider**. Using the **enableAnimation** property you can enable/disable the animation effects. Data type of this property is “Boolean”.

The following steps explains you on how to disable the animation effect in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider”.



{% highlight html %}


<div class="txt">Default Slider</div>
<div id="defaultSlider"></div>

{% endhighlight %}

{% highlight javascript %}

 // In JavaScript, during initialization disable the enableAnimation property.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            value: 60,
            width: "500",
            enableAnimation:false
        });
    });
}

{% endhighlight %}

## Customizing Animation speed

Animation speed of the **Slider** indicates the speed at which the slider handle can be moved. Higher the value specified for this property decreases the rate of speed at which the **Slider** handle can be moved. You can customize the animation speed of the **Slider** using the **animationSpeed** property. Default value of this property is “500”. 

The following steps explains you on how to customize the animation speed.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider”.


{% highlight html %}

   <div class="txt">Default Slider</div>
   <div id="defaultSlider"></div>

{% endhighlight %}

{% highlight javascript %}

        // In JavaScript, during initialization specify the value for animationSpeed property.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            value: 60,
            width: "500",
            animationSpeed: 600
        });
    });
}


{% endhighlight %}
