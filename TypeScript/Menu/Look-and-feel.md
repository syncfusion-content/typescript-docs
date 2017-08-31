---
layout: post
title: Look-and-feel
description: look and feel
platform: Typescript
control: Menu
documentation: ug
---

# Look and feel

**Essential JavaScript** controls feature 12 built-in themes, six flat and gradient effects, and also supports custom skin options for user-defined themes.

12 themes support available for **Menu** control namely,

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark

##cssClass

**Menu** control also customizes its appearance using user-defined **CSS** and custom skin options (colors and backgrounds). To apply custom themes you can use the “cssClass” property. “cssClass” property sets the root class for **Menu** control theme.

Using this **cssClass** you can override the existing styles under the theme style sheet. The theme stylesheet applies theme-specific styles like colors and backgrounds. In the following sample the value of “cssClass” property is set as “Purple-dark”. Purple-dark is added as root class to **Menu** control at the runtime. From this root class you can customize the **Menu** control theme.

Add the following code in your **HTML** page.

{% highlight html %}


<div>
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
                            <li><a>Location</a></li>
                        </ul>
                    </li>
                </ul>
            </li>

            <li id="Services">
                <a>Services</a>
                <ul>
                    <li><a>Outsourcing</a></li>
                </ul>
            </li>

            <li id="About"><a>About</a></li>

            <li id="Contact">
                <a>Contact us</a>
                <ul>
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
                        </ul>
                    </li>
                    <li><a>Apply online</a></li>
                </ul>
            </li>

        </ul>

    </div>

</div>

{% endhighlight %}

{% highlight javascript %}


    // Add the following code in your script section.
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 500,
            cssClass: "Purple-dark"
        });
    });


{% endhighlight %}

Add the following code in your style section.

{% highlight css %}


<style type="text/css" class="cssStyles">
    .Purple-dark .e-menu,.e-menu.e-horizontal .e-list > ul {     
          
       background: pink;              
     
     }        
    
    .Purple-dark .e-menu.e-horizontal .e-list > a {    
    
      color: blue;      
      
     }
</style>


{% endhighlight %}



Following screenshot displays the output of the above code.

![](Look-and-feel_images/Look-and-feel_img1.png) 

