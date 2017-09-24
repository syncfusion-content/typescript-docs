---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: Typescript
control: Tab Control
documentation: ug
---

# Keyboard Navigation

**Tab** control provides supports **keyboard** interaction. Using this functionality you can interact with control using keyboard. This is achieved by enabling ‘**allowKeyboardNavigation**’ to **‘true**’**.** By default this property value is set to ‘**true**’.

Following table illustrates the accessible key and their usage

<table>
<tr>
<th>
Keys</th><th>
Behavior</th></tr>
<tr>
<td>
Up</td><td>
Selected previous item.</td></tr>
<tr>
<td>
Right</td><td>
Selected previous item.</td></tr>
<tr>
<td>
Down</td><td>
Selected next item.</td></tr>
<tr>
<td>
Left</td><td>
Selected next item.</td></tr>
<tr>
<td>
Home</td><td>
Selected first item.</td></tr>
<tr>
<td>
End</td><td>
Selected last item.</td></tr>
</table>
The following code example is used to render the **Tab** element in **RTL** format. 

Add the following **HTML** to render **Tab** with **keyboard** navigation.

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
                 allowKeyboardNavigation: true 
         });

            //Control focus key
            $(document).on("keydown", function (e) {
                if (e.altKey && e.keyCode === 74) {
                    // j- key code.
                    $("#dish ul a").focus();
                }
            });
        });

}
{% endhighlight %}


The following screenshot illustrates the **Tab** with **keyboard** navigation.

![](Keyboard-Navigation_images/Keyboard-Navigation_img1.png) 

