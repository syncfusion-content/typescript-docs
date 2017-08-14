---
layout: post
title: width
description: width
platform: typescript
control: Radial Slider
documentation: ug
---

# Dimension 

## Stroke Width

**Radial Slider** strokeWidth property specifies the width of the outline . By default, the **Radial slider** strokeWidth is set as 2. Refer to the following code example.

{% highlight html %}

    <div id="radialSlider">
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
          innerCircleImageUrl:"chevron-right.png",
          strokeWidth:4
           });
        });

{% endhighlight %}


The following screenshot illustrates the output of the above code.

![](dimension_images\dimension_img1.png)


## Setting radius

The **RadialSlider** property **radius**  indicates the radius of the RadialSlider's circle ant its allow to change radius value.  By default, the **Radial Slider** radius is set to 200. Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
             innerCircleImageUrl: "chevron-right.png",
             radius:250
             });
    });

{% endhighlight %}

