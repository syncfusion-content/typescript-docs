---
layout: post
title: Dimensions
description: dimensions
platform: Typescript
control: ListView
documentation: ug
---

# Dimensions

To customize the **ListView** dimensions, **Width** and **Height** properties are used.

Refer to the following code examples.



{% highlight html %}


    <div id="defaultlistview">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#defaultlistview"), {
                 width: 300, 
                 height: 600
            });
        });
}

{% endhighlight %}



Run the code to get the following output

![](Dimensions_images/Dimensions_img1.png) 

