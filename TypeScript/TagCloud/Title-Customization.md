---
layout: post
title: Title-Customization
description: title customization
platform: Typescript
control: TagCloud
documentation: ug
---

# Title Customization

## Show title

The **TagCloud** items are displayed with a Title element by default. To hide the title, you can use **showTitle** property that is true by default.

### How to disable title in TagCloud

The following steps explains you on how to configure **title** for a **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}


 <div id="website"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TagCloudComponent {
    // Disable the Title element of TagCloud control as follows.
$(function () {  
     var sample = new ej.TagCloud($("#website"), {
        showTitle:false, 
        dataSource: websiteCollection
    });
  });
}

{% endhighlight %}

The following screenshot illustrates a **TagCloud** control when you disable title,

![](Title-Customization_images/Title-Customization_img1.png) 



## Title text

**TagCloud** widget allows you to set a custom title text by using the **titleText** property. By default titleText property is set to string value “Title”.

### Defining title text for TagCloud

The following steps explains you on how to configure **titleText** for a **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}


 <div id="website"></div>

{% endhighlight %}

{% highlight javascript %}



    // Disable the Title element of TagCloud control as follows.
    
    var sample = new ej.TagCloud($("#website"), {
        showTitle:true, 
        titleText: "Tech Sites",
        dataSource: websiteCollection
    });

{% endhighlight %}


The following screenshot illustrates the **TagCloud** control with customized title text.

![](Title-Customization_images/Title-Customization_img2.png)



## Title image

**TagCloud** widget provides **titleImage** to set an image for the title. You can set the desired image **URL** to **titleImage** property.

### Defining title text for TagCloud

The following steps explains you to configure **titleImage** for a **TagCloud**.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

 <div id="website"></div>

{% endhighlight %}

{% highlight javascript %}


    // Disable the Title element of TagCloud control as follows.
    
     var sample = new ej.TagCloud($("#website"), {
        titleImage: "http://js.syncfusion.com/demos/web/images/waitingpopup/js_logo.png",
        titleText: "Tech Sites",
        dataSource: websiteCollection
    });


{% endhighlight %}


Using CSS class you can resize the image content as follows.



{% highlight css %}

<style type="text/css">
.e-title-img {
            height::35px;
            width:35px;
        }
    </style>


{% endhighlight %}



The following screenshot illustrates the **TagCloud** control with customized title image.

![](Title-Customization_images/Title-Customization_img3.png)



