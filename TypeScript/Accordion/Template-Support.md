---
layout: post
title: Template-Support
description: template support
platform: Typescript
control: Accordion 
documentation: ug
---

# Template Support

In **JavaScript**, you can load the contents or **HTML** elements directly inside the **&lt;div&gt;** element that you are going to convert as **Accordion** control.

{% highlight html %}

   
<div id="pizzaMenu" style="width: 500px">
    <h3>
        <a href="#">GARDEN FRESH (Veg)</a>
    </h3>
    <div>
        <img src="~/Content/accordion/garden-veggie.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $50
            <br />
            Ingredients : cheese, onions, green capsicums & tomatoes.
        </div>
    </div>
    <h3>
        <a href="#">CORN & SPINACH (Veg)</a>
    </h3>
    <div>
        <img src="~/Content/accordion/corn-and-spinach-05.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $70
            <br />
            Ingredients : cheese, sweet corn & green capsicums.
        </div>
    </div>
    <h3>
        <a href="#">CHICKEN DELITE (Non-veg)</a>
    </h3>
    <div>
        <img src="~/Content/accordion/chicken-delite.png" alt="garden-fresh" />
        <div class="ingredients">
            Rate    : $100
            <br />
            Ingredients : cheese, chicken chunks, onions & pineapple chunks.
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}
/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />\

module AccordionComponent {
    $(function () {
        var sample = new ej.Accordion($("#pizzaMenu"), {
         enableMultipleOpen: true
     });
  });
}  

{% endhighlight %}



![](Template-Support_images/Template-Support_img1.png)

