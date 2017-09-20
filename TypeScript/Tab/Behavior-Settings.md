---
layout: post
title: Behavior-Settings
description: behavior settings
platform: Typescript
control: Tab Control
documentation: ug
---

# Behavior Settings

## Close Button

By default, **Tab** contents are rendered without **Close Button**. You can add the **Close** **Button** by setting the ‘**showCloseButton**’ property to ‘**true**’. When you move cursor over the **Tab** headers, the **Close** **Button** is displayed.   

The following code example is used to render the **Tab** widget with **Close** **Button**.

Add the following **HTML** for simple **Tab** creation with **Close** **Button**.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>


{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                showCloseButton: true
             });
        });
}

{% endhighlight %}

The following screenshot illustrates the **Tab** with **Close** **Button**. 

![](Behavior-Settings_images/Behavior-Settings_img1.png) 

## Orientation

By default, **Tab** control renders in horizontal orientation. You can change the **Orientation** to vertical using the ‘**headerPosition**’ property. Using  this property, you can customize the header by ” **top**”,” **bottom**”, “**left**”, and  “**right**”.

The following code example is used to render the sub **Tab** widget in the vertical orientation. 

Add the following **HTML** for **Tab** orientation.

{% highlight html %}

 
<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>


{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{ 
                 headerPosition: "left", 
                 height: "220px" 
            });                                          
        });   
}

{% endhighlight %}


The following screenshot illustrates the sub **Tab** with vertical orientation. 

![](Behavior-Settings_images/Behavior-Settings_img2.png) 

## State Maintenance

When the page gets refreshed or reloaded, the **Tab** state is changed (i.e.) the focus is moved to start **Tab**. You can maintain the state of the **Tab** by using ‘**enablePersistence**’ property. When this property is set to **‘true’,** it retains the state. 

The following code example is used to render the **Tab** widget with state maintenance. 

Add the following **HTML** for **Tab** **state** **maintenance**.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                  enablePersistence: true
            });     
        });
}

{% endhighlight %}


The following screenshot illustrates the **Tab** with **State** **maintenance**.

![](Behavior-Settings_images/Behavior-Settings_img3.png)

State before page refresh
{:.caption}





![](Behavior-Settings_images/Behavior-Settings_img4.png)

State after page refresh
{:.caption}

