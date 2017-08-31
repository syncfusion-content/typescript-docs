---
layout: post
title: Separators
description: separators
platform: Typescript
control: Menu
documentation: ug
---

# Separators

Menu can also contain separators that are horizontal bars between menu items. You cannot select a separator. Separators are somewhat similar to [borders](http://docs.oracle.com/javase/tutorial/uiswing/components/border.html), except that they are genuine components and, as such, are drawn inside a control, rather than around the edges of the **Menu** control. **enableSeparator** is the property that is used to display the separators in the **Menu** control. It accepts the Boolean type value. Its default value is true. 

 


Add the following **&lt;script&gt;** in the above code sample to display the **Menu** control without separator by setting **enableSeparator** as **false**.

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
            enableSeparator: false
        });
    });
}


{% endhighlight %}



The following screenshot displays the output for the above code. 

![](Separators_images/Separators_img2.png) 


# Separators for Context Menu

We can add the separators for particular ContextMenu items by including **e-separator** class in the required **LI** elements. Add the following code to display ContextMenu with separator lines.


{% highlight html %}

<div id="target" class="textarea">
	HTML is written in the form of HTML elements consisting of tags enclosed in angle brackets (like &lt;html&gt;),within the web page content. HTML tags most commonly come in pairs like and ,although some tags, known as empty elements, are unpaired, for example &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into visible or audible web pages. The browser does not display the HTML tags, but uses the tags to interpret the content of the page.
</div>

<ul id="contextMenu">
	<li><a>Cut</a></li>
	<li><a>Copy</a></li>
	<li class="e-separator"><a>Paste</a></li>
	<li><a>Comments</a></li>
	<li><a>Links</a></li>
	<li><a>Clear Formatting</a></li>
</ul>

{% endhighlight %}


{% highlight javascript %}

 <script type="text/javascript">

    $(function () {
         var sample = new ej.Menu($("#contextMenu"),{
				menuType: ej.MenuType.ContextMenu,
				openOnClick: false,
				contextMenuTarget: "#target",
			});
        });
		
 </script>
	
{% endhighlight %}


{% highlight css %}

    <style type="text/css">'
	
        .textarea {
            border: 1px solid;
            padding: 10px;
            position: relative;
            text-align: justify;
            width: 463px;
            color: gray;
        }
		
    </style>

{% endhighlight %}

The following screenshot displays the output for the above code. 

![](Separators_images/Separators_img3.png) 


