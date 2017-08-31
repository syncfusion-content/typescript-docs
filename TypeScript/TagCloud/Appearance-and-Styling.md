---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: Typescript
control: TagCloud
documentation: ug
---

# Appearance and Styling

## Minimum and maximum Font size

The **TagCloud** content are set to different font sizes from minimum to maximum based on its frequency values. By default, **minFontSize** is “10px” and **maxFontSize** is “40px”, using these properties you can customize the minimum and maximum font sizes.

### Customizing font sizes of TagCloud

The following steps explains you on how to configure font sizes for a **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

<div id="website"></div>

{% endhighlight %}

{% highlight javascript %}

    // Assign the values for minFontSize  and maxFontSize properties below.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
 module TagCloudComponent {
    $(function () {  
    var sample = new ej.TagCloud($("#website"), {  
        minFontSize: "20px",
        maxFontSize: "50px",
        titleText: "Tech Sites",
        dataSource: websiteCollection
    });
  });
 }
{% endhighlight %}


The following screenshot illustrates the **TagCloud** control with customized font sizes.

![](Appearance-and-Styling_images/Appearance-and-Styling_img1.png) 


## Tag format

You can set the **TagCloud** content display format using **format** property. By default format is set to cloud, that displays content in **TagCloud**. You can set the format as list to display the content in linear format.

### Defining Cloud and List format

The following steps explains you to configure format for a **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

 
<table>
   <tr>
      <td>
         <span>Tag format cloud</span>
         <div id="techwebcloud"></div>
      </td>
      <td>
         <span>Tag format list</span>
         <div id="website"></div>
      </td>
   </tr>
</table>

{% endhighlight %}

{% highlight javascript %}



     // Assign the values for format property in TagCloud.
    var sample = new ej.TagCloud($("#website"), {  
        format: "list",
        titleText: "Tech Sites List",
        dataSource: websiteCollection
    });
   var sample = new ej.TagCloud($("#techwebcloud"), {  
        format: "cloud",
        titleText: "Tech Sites Cloud",
        dataSource: websiteCollection
    });

{% endhighlight %}

The following screenshot illustrates the **TagCloud** control with customized formats.

![](Appearance-and-Styling_images/Appearance-and-Styling_img2.png) 



## Theme

You can control the style and appearance of **TagCloud** based on CSS classes. To apply styles to the **TagCloud** control, you can refer two files, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 16 theme support available for RadialMenu component, namely:

* flat-azure
* flat-azure-dark
* fat-lime
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

## CssClass

You can use the CSS class to customize the **TagCloud** appearance. Any of the CSS properties can be used to modify look and feel of tag cloud based on the requirement. Define a **CSS** class as per requirement and assign the class name to **cssClass** property.

### Configure TagCloud using CSS class

The following steps allows you to configure **CSS** class for **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.


{% highlight html %}

<div id="website"></div>

{% endhighlight %}

{% highlight javascript %}


     // Add the cssClass property to TagCloud.
    
    var sample = new ej.TagCloud($("#website"), {  
        titleText: "Tech Sites",
        dataSource: websiteCollection,
        cssClass:"CustomCss"
     });
    
{% endhighlight %}

Define CSS class for customizing the **TagCloud** widget.

{% highlight css %}

<style type="text/css" class="cssStyles">
        /* Customize the TagCloud div element */
        .CustomCss
        {
            background-color: #DDC;
            width: 400px;
        }
        /* Customize the TagCloud header element */        
        .CustomCss .e-header.e-title {
            text-align: center;
            font-weight: bold;
        }
</style>


{% endhighlight %}



The following screenshot illustrates the **TagCloud** with customized CSS class,

![](Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 



