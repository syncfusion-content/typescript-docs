---
layout: post
title: Ajax-Content-Load-Load-on-Demand
description: ajax content load (load on demand)
platform: Typescript
control: Tab Control
documentation: ug
---

# AJAX Content Load (Load on Demand)

You can change the contents in sub **Tab** element periodically and you are provided with a support to change the contents without any problems. To achieve the content load, use the **Load on Demand** concept.

In **Load On-Demand**, the external **HTML** file with the necessary details is referred in &lt;href&gt; section during **Tab** header declaration section. Also include “**dataType**”, “**contentType**”, and “**async**” in the script like the following example when rendering the control. When you click the **Tab** header, the AJAX automatically calls the content from the external files and displays in a **Tab** content section. 

## Sub Tab with AJAX Content

Each item has a variety of options and these options are also specified in the limited space. So you can choose the **Tab** control that is used within the root **Tab** to specify more details.

The following code example illustrates to create the **Tab** control within the root **Tab** element. This **HTML** code is appended within the previous **HTML** code section. To render the child **Tab** with its header, add this code example within the first **Tab** &lt;div&gt; element. 

Add the following **HTML** to render sub **Tab** with **AJAX** content.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        <div id="pizza">
            <ul>
                <li>
                    <a href="content/cornSpinach.html">Corn & Spinach </a></li>
                <li>
                    <a href="Content/chickenDelite.html">Chicken Delite </a></li>
            </ul>
        </div>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
        <div id="sandwich">
            <ul>
                <li>
                    <a href="Content/gardenVeggie.html">Garden Veggie </a></li>
                <li>
                    <a href="Content/chickenTikka.html">Chicken Tikka </a></li>
                <li>
                    <a href="Content/paneerTikka.html">Paneer Tikka </a></li>
            </ul>
        </div>
    </div>
</div>


{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {
    $(function () {
        var sample = new ej.Tab($("#dish"),{
        });
        var sample1 = new ej.Tab($("#pizza"),{
              dataType: "html", 
              contentType: "html", 
              async: true
        });
        var sample2 = new ej.Tab($("#sandwich"),{
              dataType: "html",
              contentType: "html", 
              async: true
              });
        });
    }

{% endhighlight %}

The file ‘**cornSpinach.html**’ content is as follows.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
        <img src="http://js.syncfusion.com/demos/web/images/accordion/corn-and-spinach-05.png" alt="corn-spinach"/>
        <div class="ingredients">
            Rate    : $70<br />
            Ingredients : cheese, sweet corn &amp; green capsicums.
                <br />
            Description: Small pizza bases are topped with spinach and paneer and fresh cream, a nice layer of mozzarella cheese. This is baked until the cheese is all hot and gooey.                   
        </div>
    </div>
</body>
</html>


{% endhighlight %}



The file ‘**chickenDelite.html’** content is as follows.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<body>
    <div class="e-content">
        <img src="http://js.syncfusion.com/demos/web/images/accordion/chicken-delite.png" alt="chicken-delite"/>
        <div class="ingredients">
            Rate    : $100<br />
            Ingredients : cheese, chicken chunks, onions &amp; pineapple chunks.  
            <br />
            Description: This is a tasty, elegant chicken dish that is easy to prepare.
        </div>
    </div>
</body>
</html>

{% endhighlight %}


At the time of **Ajax** call, the content fetched from external file referenced location is illustrated in the following screenshot. 


![](Ajax-Content-Load-Load-on-Demand_images/Ajax-Content-Load-Load-on-Demand_img1.png) 


The following screenshot illustrates the First **Tab** with the sub **Tab** control using **Load on Demand**. 

![](Ajax-Content-Load-Load-on-Demand_images/Ajax-Content-Load-Load-on-Demand_img2.png) 



