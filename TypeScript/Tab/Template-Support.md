---
layout: post
title: Template-Support
description: template support
platform: Typescript
control: Tab Control
documentation: ug
---

# Template Support

We can use this option to load any HTML elements and showcase it in the Tab panels as per our requirement.

We can load the contents or HTML elements directly inside the &lt;div&gt; element which we are going to convert as Tab control.



{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#corn">Corn & Spinach </a></li>
        <li><a href="#chicken">Chicken Delite</a></li>
    </ul>
    <div id="corn" style="background-color: #F5F5F5">
        <div class="e-content">
            <img src="http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"/>
            <div class="ingredients">
                Rate    : $70<br /> Ingredients : cheese, sweet corn &amp; green capsicums.
                <br />
                Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.
            </div>
        </div>
    </div>
    <div id="chicken" style="background-color: #F5F5F5">
        <!--Content for Chicken Delite-->
    </div>
</div>


{% endhighlight %}





{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
        });
    });
} 
{% endhighlight %}





**Output:**

![](Template-Support_images/Template-Support_img1.png) 

