---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: Typescript
control: Menu
documentation: ug
---

# Keyboard Navigation

The **Menu** control also provides support for keyboard navigation. In the **Menu** control, it is possible to control the entire menu control items by using the provided shortcut keys. 

The various keyboard shortcuts available within the **Menu** control are discussed in the following table, 

List of keyboard shortcut keys

<table>
<tr>
<th>Keys</th><th>Usage</th></tr>
<tr>
<td>
Esc</td><td>
Closes the opened Menu control.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item.</td></tr>
<tr>
<td>
Up/left/down/right arrow keys</td><td>
Navigates up or previous item.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down or next item.</td></tr>
<tr>
<td>
Left</td><td>
Navigates to previous group.</td></tr>
<tr>
<td>
Right</td><td>
Navigates to next group.</td></tr>
</table>


Add the following code for Keyboard navigation in your **Menu** control.

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

</div>

{% endhighlight %}

{% highlight javascript %}


        // Add the following code in your script section.
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            //Control focus key
            $(document).on("keydown", function(e) {
                if (e.altKey && e.keyCode === 74) { // j- key code.
                    $("#menu").focus();
                }
            });
        });


{% endhighlight %}

Add the following code in your style section.

{% highlight css %}


<style type="text/css">
    #keyboard {
        margin-left: 50px;
    }
</style>


{% endhighlight %}

Following screenshot displays the output of the above code. 

![](Keyboard-Navigation_images/Keyboard-Navigation_img1.png)


When you press **alt+j,** the first item of the **Menu** control only gets focused as displayed in the following screenshot.

![](Keyboard-Navigation_images/Keyboard-Navigation_img2.png)


Similarly you can access the **Menu** control using keyboard itself.

