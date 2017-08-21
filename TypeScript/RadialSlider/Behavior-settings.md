---
layout: post
title: Behavior-settings
description: behavior settings
platform: typescript
control: RadialSlider
documentation: ug
---

# Behavior settings

The following are some  properties that enables you to an option to enhance the behavior of **RadialSlider** control.

##  Show/hide RadialSlider on initial rendering 

The **RadialSlider** property **autoOpen** allow you to make the control visible on initial rendering. By default, the value of the property is set as **true**. Setting it as **false** will hide the control on initial rendering.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

  /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module RadialSliderComponent {
    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
             innerCircleImageUrl: "chevron-right.png",
             autoOpen:false 
    });
  });
}
    
{% endhighlight %}

## Value accuracy 

The **RadialSlider** property **enableRoundOff** allow  to show  the rounded off value when user changes it. By default, the value of the property is set as **true**. For accurate values, you can set this as false.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

  /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module RadialSliderComponent {
    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                innerCircleImageUrl: "chevron-right.png",
                enableRoundOff:false 
        });
    });
}
{% endhighlight %}

## Display inline

The **RadialSlider** property **inline** is used to show the control values inline of the slider. By default, the value of the property is set as **false**.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}


    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
          innerCircleImageUrl: "chevron-right.png",
          inline:true 
        });
    });


{% endhighlight %}

## Modifying Label Space 

The **RadialSlider** property **labelSpace** allow to define the space of label in it. By default, the **RadialSlider** labelSpace is set as 30. Refer to the following code example.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                 innerCircleImageUrl: "chevron-right.png",
                 labelSpace:40
   });
});

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img1.png)


## Show/Hide inner circle

The **RadialSlider** property **showInnerCircle** allow to show  or hide  the inner circle of  the **RadialSlider**.By default,Value of the property is set as **true** and type of the property is **Boolean**.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

  $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                innerCircleImageUrl: "chevron-right.png",
                showInnerCircle:false
         });
   });

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img2.png)

## Values customization

The **RadialSlider** property **ticks** allow to set an array of a numeric value which will be displayed in it. By Default **RadialSlider** ticks value is a set to an array of length 11 as following,

ticks = { 0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100 }. You can refer the below code for reference.

{% highlight html %}

       <div id="radialSlider"> </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
          var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
                innerCircleImageUrl: "chevron-right.png",
                ticks:[100,200,300,400,500,600,700,800,900,1000],
                value:100 
        });
    });

{% endhighlight %}

The following screenshot shows the output for the above code example.

![](Behavior-settings_images\Behavior-settings_images_img3.png)
