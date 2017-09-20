---
layout: post
title: Scroll-Support
description: scroll support
platform: Typescript
control: Tab Control
documentation: ug
---

# Scroll Support

**Tab** control provides you scrolling support on Tab items to display a larger number of tabs with scroll buttons to get rid of the extending page size. The enabled Scroll buttons can be used to traverse through the elements.

By default, **Tab** header is rendered without scroll button. You can add the scroll button by setting the "**enableTabScroll**" property to "**true**". When you move the cursor over the **Tab** header the scroll button is displayed.   



You can use the following code example to render the **Tab** widget with scroll button.

Add the following **HTML** code to create a simple Tab with scroll button.

{% highlight html %}


<div style="width: 500px; padding: 50px;">
    <div id="dish">
        <ul>
            <li><a href="#pizza">Pizza Menu</a></li>
            <li><a href="#pasta">Pasta Menu</a></li>
            <li><a href="#burger">Burger Menu</a></li>
            <li><a href="#sandwich">Sandwich Menu</a></li>
            <li><a href="#spaghetti">Spaghetti Menu</a></li>
            <li><a href="#ramen">Ramen Menu</a></li>
        </ul>
        <div id="pizza" style="background-color: #F5F5F5">
            <!--Food item description-->
            <p>
                Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
        <div id="pasta" style="background-color: #F5F5F5">
            <!--dish description-->
            <p>
                Pasta cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
        <div id="sandwich" style="background-color: #F5F5F5">
            <!--dish description-->
            <p>
                Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
        <div id="burger" style="background-color: #F5F5F5">
            <!--dish description-->
            <p>
                Burger cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
        <div id="spaghetti" style="background-color: #F5F5F5">
            <!--dish description-->
            <p>
                Spaghetti cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
        <div id="ramen" style="background-color: #F5F5F5">
            <!--dish description-->
            <p>
                Ramen cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        </div>
    </div>
</div>


{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                enableTabScroll: true
            });
        });		
}


{% endhighlight %}

The following screenshot illustrates you the **Tab** control with scroll button. 

![](Scroll-Support_images/Scroll-Support_img1.png) 





