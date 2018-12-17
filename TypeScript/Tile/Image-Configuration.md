---
layout: post
title: Syncfusion Tile Image Configuration
description: image configuration
platform: typescript
control: Tile
documentation: ug
---

# Image Configuration

The **“data-ej-imagePosition”** attribute is used to adjust the position of **Tile** image at the **center** on initialization. The possible values for the “**data-ej-imagePosition”** are as follows

1. Center
2. Top
3. Bottom
4. Right
5. Left
6. TopLeft
7. BottomRight
8. BottomLeft 
9. Fill



The **"data-ej-imageUrl”** attribute is used to set the background image for **Tile**, where the image is given in the path specified by “**data-ej-imageUrl”** attribute.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}
 
Add the following code inside the **script** tag.
 
{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module TileViewComponent {
    $(function () {
        var tile1 = new ej.Tile($("#tile1"), {
        tileSize: "wide", 
        imagePosition: "center",
         imageUrl: "http://js.syncfusion.com/UG/web/Content/tile/Weather_2.png", 
         text: "weather"
  });
 });
}

{% endhighlight %}



![Image Configuration](Image-Configuration_images/Image-Configuration_img1.png)

You can give images for each tile through **css** classes by using **"data-ej-imageClass”** attribute. You can define your desired styles in the specified class.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}

{% highlight css %}
    <style>
        .pictures {
            background: url("http://js.syncfusion.com/UG/web/Content/tile/pictures.png");
            background-size: 30px 30px;
        }
    </style>

{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}

    var tile1 = new ej.Tile($("#tile1"), {
         tileSize: "medium",
         imagePosition: "center", 
         imageClass: "pictures",
         text: "Pictures" 
    });

{% endhighlight %}

![Tile Image Configurations](Image-Configuration_images/Image-Configuration_img2.png)

