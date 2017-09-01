---
layout: post
title: Orientation
description: orientation
platform: Typescript
control: Menu
documentation: ug
---

# Orientation

It gets or sets the direction in which the **Menu** control renders and specifies the orientation of the normal menu.  According to the orientation property the **Menu** control renders in horizontal or vertical.

##Horizontal Menu

Horizontal orientation displays the menu items horizontally and it is the default orientation behavior of **Menu** control. 

The following steps explains you the details on rendering the **Menu** control. 

In an **HTML** page, add the **&lt;UL&gt;** and **&lt;LI&gt;** to configure **Menu** control.

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

     
    // Initialize the control in JavaScript.
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 500 
       });
    });


{% endhighlight %}


The following screenshot displays the output of the above code.        

![](Orientation_images/Orientation_img1.png) 


##Vertical Menu

You can also render **Menu** control in vertical direction using **orientation.** To set the vertical orientation of **Menu** control, replace the following script in the above sample code example.

Add the following code in your **&lt;script&gt;** section.



{% highlight javascript %}


    $(function () {
        var sample = new ej.Menu($("#menu"),{
            orientation: ej.Orientation.Vertical
        });
    });



{% endhighlight %}



The following screen shot displays the output of the above code.                       

![](Orientation_images/Orientation_img2.png) 


