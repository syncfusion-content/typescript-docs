---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: TypeScript
control: ProgressBar
documentation: ug
---

# Appearance and Styling

## Adjusting ProgressBar size

**ProgressBar** widget provides the ability to change or adjust the ProgressBar size. The ‘**height’** and ‘**width’** properties in the ProgressBar widget allows you to set the maximum height and maximum width for the ProgressBar. The value set to this property is **string or Number** type.

The following steps explain you on how to adjust the ProgressBar size.

In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget

{% highlight html %}

<div class="control">
   <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ProgressBarComponent {
    $(function () {
        var sample = new ej.ProgressBar($("#progressbar"),{
            value: 50,
            width: "400px",
            height: "40px"
        });
        sample.setModel({ text: progress.getValue() + " %" });
    });
}
{% endhighlight %}

The following screenshot displays the output.

![](Appearance-and-Styling_images/Appearance-and-Styling_img1.png) 

## Custom text

**Custom text** is displayed when the **ProgressBar** shows different levels of progress in the ProgressBar. Support for **Custom text** to mention the percentage or any other message inside the **ProgressBar** is possible by using “**text**” property.

The following steps explain the configuration of the **Custom text** for the ProgressBar widget.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}


<div class="control">
   <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}

      // Add Custom Text for the ProgressBar widget.
    
    $(function () {
        var sample = new ej.ProgressBar($("#progressbar"),{
              text: "loading",
              value: 35,
              height: 20,
              width: 500
          });
      });

{% endhighlight %}

The following screenshot displays the output.      

 ![](Appearance-and-Styling_images/Appearance-and-Styling_img2.png) 

## Theme

The ProgressBar widget style and appearance are controlled based on **CSS** classes. In order to apply **Theme** to the ProgressBar widget, you can refer two files, namely, ej.widgets.core.min.css and ej.theme.min.css. When the file ej.widgets.all.min.css is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project, as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes’ support available for the **ProgressBar** widget namely,

* Default-theme
* Flat-azure-dark
* Fat-lime
* Flat-lime-dark
* Flat-saffron
* Flat-saffron-dark
* Gradient-azure
* Gradient-azure-dark
* Gradient-lime
* Gradient-lime-dark
* Gradient-saffron
* Gradient-saffron-dark

## CSS class

To apply custom styles to the ProgressBar widget, you can specify the **cssClass** property. The specified **CSS** name is added in the root of the **ProgressBar** widget.

The following code example is used to render the ProgressBar widget with customized style.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.



{% highlight html %}

<div class="control">
    <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}


        // Add the class for the ProgressBar Widget.
    
    $(function () {
        var sample = new ej.ProgressBar($("#progressbar"),{
                cssClass: 'custom',
                value: 70,
                height: 20,
                width: 500
            });
            progress.sample({ text: progress.getValue() + "%" });
        });	

{% endhighlight %}

Add the following styles to render the ProgressBar with customized style.

{% highlight css %}


<style type="text/css">
   .custom .e-progress {
       background-color:gray;
   }
</style>


{% endhighlight %}



The following screenshot displays the output.

![](Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 

