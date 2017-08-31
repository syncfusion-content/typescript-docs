---
layout: post
title: Customizing-the-Submenu-direction
description: customizing the submenu direction
platform: Typescript
control: Menu
documentation: ug
---

# Customizing the Submenu direction

You can customize the direction to open the sub menu items using **subMenuDirection** property. **subMenuDirection** accepts the type as string or enum and value as “Left” and “Right”. 

In the following example, the Sub menus opens in the Left side of the menu.

Add the following code in your **HTML** page.


{% highlight html %}

 
<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <ul id="coProducts">
                <li id="Products">
                    <a href="#">Products</a>
                    <ul>
                        <li><a>ASP.NET</a></li>
                        <li><a>ASP.NET MVC</a></li>
                        <ul>
                            <li><a>WinRT (XMAL)</a></li>
                            <li><a>Silverlight</a></li>
                        </ul>
                       </ul>
                </li>            

            <li id="Support">
                <a>Support</a>
                <ul>
                    <li><a>Direct-Trac Support</a></li>
                    <li>
                        <a>Services</a>
                        <ul>
                            <li><a>Consulting</a></li>
                            <li><a>Training</a></li>
                        </ul>
                    </li>
                </ul>
            </li>

            <li id="Purchase"><a>Purchase</a></li>

            <li id="Downloads">
                <a>Downloads</a>
                <ul>
                    <li><a>Evaluation</a></li>
                </ul>
            </li>

            <li id="Resources">
                <a>Resources</a>
                <ul>
                    <li>
                        <a>Technology Resource Portal </a>
                        <ul>
                            <li><a>White Papers</a></li>
                        </ul>
                    </li>
                    <li><a>FAQ</a></li>
                </ul>
            </li>

            <li id="Company">
                <a>Company</a>
                <ul>
                    <li>
                        <a>About Us</a>
                        <ul>
                            <li><a>Media Kit</a></li>
                        </ul>
                    </li>
                    <li><a>Company Blog</a></li>
                    <li><a>Technical Blog</a></li>
                    <li><a>Newsletter</a></li>
                    <li>
                        <a>Partners</a>
                        <ul>
                            <li><a>Technology Partners</a></li>
                            <li><a>Training Partners</a></li>
                            <li><a>Consulting Partners</a></li>
                        </ul>
                    </li>
                    <li>
                        <a>Locations</a>
                        <ul>
                            <li><a>RDU</a></li>
                        </ul>
                    </li>
                    <li><a>Contact Us</a></li>
                    <li><a>Careers</a></li>
                </ul>
            </li>
          </ul>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#coProducts"),{
            subMenuDirection: "left"
        });
    });
}

{% endhighlight %}



The output for the above code example is as follows.          

![](Customizing-the-Submenu-direction_images/Customizing-the-Submenu-direction_img1.png) 

You can even achieve auto positioning for Context Menu. Use the following code sample for context menu in order to open the submenu items of context menu in left side.

Add the following code in your **HTML** page.

{% highlight html %}


 <div>
    <div id="target" class="textarea">
        HTML is written in the form of HTML elements consisting of tags enclosed in angle
        brackets (like
        &lt;html&gt;
        ),within the web page content. HTML tags most commonly come in pairs like and ,although
        some tags, known as empty elements, are unpaired, for example
        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into
        visible or audible web pages. The browser does not display the HTML tags, but uses
        the tags to interpret the content of the page.
    </div>
    <ul id="contextMenu">
        <li>
            <a>Cut</a>
            <ul>
                <li>
                    <a>Cut Particular</a>
                </li>
                <li><a>Cut Fully</a></li>
            </ul>
        </li>
        <li><a>Copy</a></li>
        <li><a>Paste</a></li>
        <li class="separator"></li>
        <li><a>Comments</a></li>
        <li><a>Links</a></li>
        <li><a>Clear Formatting</a></li>
    </ul>
</div>

{% endhighlight %}

{% highlight javascript %}

    // Add the following code in your script section.
    $(function () {
        var sample = new ej.Menu($("#contextMenu"),{          
             menuType: ej.MenuType.ContextMenu,
             openOnClick: false,
             contextMenuTarget: "#target",
             subMenuDirection: ej.Direction.Left
         });
    });


{% endhighlight %}

Add the following code in your style section.

{% highlight css %}


<style type="text/css">
    .textarea {
        border: 1px solid;
        padding: 10px;
        position: relative;
        text-align: justify;
        width: 463px;
        color: gray;
        margin: 0 auto;
    }
</style>


{% endhighlight %}


The output for the above code example is as follows.

![](Customizing-the-Submenu-direction_images/Customizing-the-Submenu-direction_img2.png) 



