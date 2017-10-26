---
layout: post
title: Appearance-and-Styling
description: appearance and styling	
platform: Typescript
control: Slider
documentation: ug
---

# Appearance and Styling

**Slider** widget looks sleek and enriched with good UI appearance. It is included with both metro (flat) theme and gradient theme support. Totally twelve built-in themes are provided including six flat themes and six gradient themes. The themes include three color variations such as “Azure”, “Lime” and “Saffron”. The themes supported by the **Slider** widgets are as follows,

By default, there are 16 theme support available for RadialMenu component, namely:

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap
* high-contrast-01
* high-contrast-02
* material
* office-365



In order to apply different themes, you can refer the “**ej.widgets.all.min.css**” file from the corresponding theme folders. This file is a combination of two style sheets “**ej.widgets.core.min.css**” and “**ej.theme.min.css**”. Instead of including “ej.widgets.all.min.css” file you can also refer the “ej.widgets.core.min.css” and “ej.theme.min.css” files separately. 

The following steps explains you on how to apply “**flat-lime-dark**” theme to the **Slider** widget

In an **HTML** page, specify the desired “**ej.widgets.all.min.css”** file to load the corresponding theme.



{% highlight html %}

<!--In _Layout page, specify the desired “ej.widgets.all.min.css” file to load the corresponding theme.-->
<head>
   <title>Slider</title>
   <!--Flat-Lime theme-->
   <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css"rel="stylesheet"/>
   <!--scripts-->
   <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
   <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>

{% endhighlight %}


{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            sliderType: ej.SliderType.Default,
            value: 60,
            width: "500",
            minValue: 40,
            maxValue: 80,
            showScale: true,
            smallStep: 5,
            largeStep: 20
        });
      var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [25,75],
            width: "500",
            showScale: true,
            smallStep: 5,
            largeStep:25
        });
    });
 }

{% endhighlight %}


Execute the above code example to render the following output.

![](Appearance-and-Styling_images/Appearance-and-Styling_img1.png) 

## CSS Class

When you want to display the **Slider** widget in a different style based on the appearance of your application, you can use this **cssClass** property to apply custom theme for the **Slider**. Specify a class name as the value for **cssClass** property. The specified class is added to the wrapper of the **Slider** widget. Now, you can easily override the styles of the **Slider** widget by accessing the styles from the root level (using the cssClass specified).

The following steps explains you on how to configure the **Slider** with custom theme using the **cssClass** property. Here, a class name “purple” is specified for the **cssClass**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider” and “Range Slider”.



{% highlight html %}


<div class="txt">Range Slider</div>
<div id="rangeSlider"></div>


{% endhighlight %}

{% highlight javascript %}


        // In JavaScript, specify a class as the value for “cssClass” property.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#rangeSlider"), {
            sliderType: ej.SliderType.Range,
            values: [25,75],
            width: "500",
            cssClass: "purple"
        });
    });
}  

{% endhighlight %}

Include the **cssClass** value before each style of the **Slider** widget and customize the styles as follows.


{% highlight css %}



<style>
   .purple.e-slider.e-widget {
       background-color: gray;
       border-color: #bbbcbb;
   }
   .purple.e-tooltip {
       background: none repeat scroll 0 0 violet;
       /* Old browsers */
       border-color: #1b95cf;
       color: white;
   }
   .purple.e-slider .e-handle.e-select {
       background-color: purple;
       border-color: purple;
   }
   .purple.e-slider .e-handle.e-hover {
       background-color: purple;
       border-color: purple;
   }
   .purple.e-slider .e-handle.e-focus {
       box-shadow: 0 0 2px rgba(0, 0, 0, 0.2);
   }
   .purple.e-slider .e-range {
       background: none repeat scroll 0 0 violet;
   /* Old browsers */
   }
   .purple.e-scale .e-tick {
       background-image: url(images/dot.png);
   }
</style>



{% endhighlight %}


Execute the above code example to render the following output.

![](Appearance-and-Styling_images/Appearance-and-Styling_img2.png) 

## Show Tooltip

**Slider** displays the tooltip to indicate the current value when you click on the **Slider** handle. By default, **Slider** displays the tooltip. Using the **showTooltip** option you can enable or disable the Tooltip. Data type of this property is “boolean”.

The following steps explains you on how to disable the tooltip in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the **Default Slider**.

{% highlight html %}

<div class="txt">Default Slider</div>
<div id="defaultSlider"></div>

{% endhighlight %}

{% highlight javascript %}


        // In JavaScript, during initialization disable the showTooltip property.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
            value: 60,
            width: "500",
            showTooltip:false
        });
    });
} 
{% endhighlight %}

## Show Rounded Corner

This property is used to display the **Slider** and its handle with rounded corners. By default **showRoundedCorner** is in disabled state. Data type of this property is “Boolean”.

The following steps explains you on how to disable the tooltip in **Slider**.

In an **HTML** page, specify the **&lt;div&gt;** elements to render the “Default Slider”.


{% highlight html %}

<div class="txt">Default Slider</div>
<div id="defaultSlider"></div>

{% endhighlight %}

{% highlight javascript %}


    // In JavaScript, during initialization enable the showRoundedCorner property.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SliderComponent {
    $(function () {
        var slider = new ej.Slider($("#defaultSlider"), {
        value: 60,
        width: "500",
        showRoundedCorner:true
    });

{% endhighlight %}

Execute the above code example to render the following output.


![](Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 

