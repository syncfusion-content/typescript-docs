---
layout: post
title: Dropdown-Button
description: dropdown button
platform: TypeScript
control: Split Button
documentation: ug
---

# Dropdown Button

You can change the **Split Button** as **Dropdown Button** that consists of a single button that when clicked displays a drop-down list of mutually exclusive items. You can achieve this by using default functionality of **Split Button** with **buttonMode** as **ej.ButtonMode.Dropdown**. Initially the **targetID** is a mandatory one.

The following steps explain how to change the **Split Button** as **Dropdown Button.**

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

<button id="dropdownButton">login</button>
<ul id="menu">
    <li><span>User</span></li>
    <li><span>Guest</span></li>
    <li><span>Admin</span></li>
</ul>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SplitButtonComponent {
    $(function () {
       var button = new ej.SplitButton($("#dropdownButton"), {
            size: "medium",
            showRoundedCorner: true,
            buttonMode: ej.ButtonMode.Dropdown,
            targetID: "menu"
        });
    });
}


{% endhighlight %}



Execute the above code to render the following output.

![](Dropdown-Button_images/Dropdown-Button_img1.png) 

