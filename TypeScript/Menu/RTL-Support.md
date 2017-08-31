---
layout: post
title: RTL-Support
description: rtl support
platform: Typescript
control: Menu
documentation: ug
---

# RTL Support

The **enableRTL** option allows the **Menu** control to display it in the right to left direction. By default, this option is set to “false” in the **Menu** control.

The following code depicts you on how to enable the **rtl** property of the **Menu** control.


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

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
         var sample = new ej.Menu($("#menu"),{
            enableRTL: true 
        });
    });
}

{% endhighlight %}

Following screenshot displays the output for the above code.

![](/js/Menu/RTL-Support_images/RTL-Support_img1.png)

RTL Support
{:.caption}


