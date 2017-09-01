---
layout: post
title: Center-Menu
description: center menu
platform: Typescript
control: Menu
documentation: ug
---

# Center Menu

You can align the **Menu** items to center by setting “enableCenterAlign” property as true. “**enableCenterAlign**” property accepts Boolean value. By default, its value is **false**. When set to **true**, then the root menu items is aligned in center.

Add the following code in your **&lt;script&gt;** section.

{% highlight html %}

    
<div>
    <ul id="menu">
        <li id="home">
            <a href="#">Home</a>
            <ul>
                <li><a>Foundation</a></li>
                <li><a>Launch</a></li>
                <li>
                    <a>About</a>
                    <ul>
                        <li><a>Company</a></li>
                        <li><a>Location</a></li>
                    </ul>
                </li>
            </ul>
        </li>
        <li id="Services">
            <a>Services</a>
            <ul>
                <li><a>Consulting</a></li>
                <li><a>Outsourcing</a></li>
            </ul>
        </li>
        <li id="About"><a>About</a></li>
        <li id="Contact">
            <a>Contact us</a>
            <ul>
                <li><a>Contact number</a></li>
                <li><a>E-mail</a></li>
            </ul>
        </li>
        <li id="Careers">
            <a>Careers</a>
            <ul>
                <li>
                    <a>Position</a>
                    <ul>
                        <li><a>Developer</a></li>
                        <li><a>Manager</a></li>
                    </ul>
                </li>
                <li><a>Apply online</a></li>
            </ul>
        </li>
    </ul>
</div>

{% endhighlight %}

{% highlight javascript %}

   
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#menu"),{
                width: 500,
                enableCenterAlign: true
            });
        });
  }

{% endhighlight %}


The following screenshot displays the output of the above code.

![](Center-Menu_images/Center-Menu_img1.png) 