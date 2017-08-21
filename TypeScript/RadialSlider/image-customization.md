---
layout: post
title: image-customization
description: image customization
platform: typescript
control: Radial Slider
documentation: ug
---

# Image customization

## Customizing inner circle 

### Using Class

The **RadialSlider** property **innerCircleImageClass** allow to set image for the inner circle of the  **RadialSlider**.  By default, the **Radial Slider** innerCircleImageClass is set as "null". Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
            innerCircleImageClass:"Radial-Slider"
         });
    });

{% endhighlight %}

The following screenshot illustrates the output of above code.

![](image-customization_images\image-customization_img1.png)


### Using image URL 

The **RadialSlider** property **innerCircleImageUrl** allow to set URL image to the inner circle of the **RadialSlider**.  By default, the **Radial Slider** innerCircleImageUrl  is set as "null". Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                innerCircleImageUrl:"chevron-right.png"
                 });
        });

{% endhighlight %}

The following screenshot illustrates the output of above code.

![](image-customization_images\image-customization_img2.png)




