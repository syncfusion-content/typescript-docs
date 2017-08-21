---
layout: post
title: AngleSupport
description: AngleSupport
platform: typescript
control: Radial Slider
documentation: ug
---

# Display Angle Support

## Start Angle

The **RadialSlider** property **startAngle** allows you to change the startAngle level of the  **RadialSlider**. By default, the **Radial Slider** startAngle is set as 0. Refer to the following code example.


{% highlight html %}

        <div id="radialSlider">
        </div>

{% endhighlight %}
    
{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
             innerCircleImageUrl:"chevron-right.png",
             startAngle: 20 
        });
    });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](display-angle-settings_images\display-angle-settings_images_img1.png)


## End Angle

The **RadialSlider** property **endAngle** allows you  to change the endAngle level of the  **RadialSlider**. By default, the **Radial Slider** endAngle is set as 360. Refer to the following code example.

{% highlight html %}

        <div id="radialSlider"></div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                 innerCircleImageUrl:"chevron-right.png",
                 endAngle: 300 
    });
});

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](display-angle-settings_images\display-angle-settings_images_img2.png)