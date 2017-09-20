---
layout: post
title: Integration-with-other-widgets
description: integration with other widgets
platform: Typescript
control: Tab Control
documentation: ug
---

# Integration with other widgets

You can provide more customization to the **Tab** with **rating** control as content in it for describing the item rating value.

The **Essential JavaScript Rating** control provide you an intuitive rating experience that allows you to select the number of stars that represents the rating. For more information about the rating, you can refer the following link:

<https://help.syncfusion.com/js/rating/getting-started>

The following code example explains you the **rating** control creation. The input element is used to create the **rating** control. Render the input element as **rating** control using the input element **id**. The code example is placed within the content description &lt;div&gt; element to declare the **rating** control and description in the **Tab** section and it is appended with the header initialization code section &lt;div&gt; element.

Add the following **HTML** to render **Tab** with other widget.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <p>Rating:</p>
        <div class="dish">
            <input id="pizza" type="text" class="rating" /><br />
        </div>
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <p>Rating:</p>
        <div class="dishRating">
            <input id="sandwich" type="text" class="rating" />
        </div>
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
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
           var sample = new ej.Tab($("#pizza"),{
               precision: ej.Rating.Precision.Exact,
               value: 4.8 
         });
          var sample = new ej.Tab($("#sandwich"),{
              precision: ej.Rating.Precision.Exact, 
              value: 4.8 
         });
    });
</script>

{% endhighlight %}

To render the **rating** controls in the first **Tab** element refer the styles mentioned in the following code example. 

Add the following styles to render **Tab**.

{% highlight css %}

    
<style type="text/css" class="cssStyles">
    .dishRating {
        position: absolute;
        margin: -31px 0px 0px 80px;
    }       
</style>


{% endhighlight %}



The following screenshot illustrates the **Tab** content with rating control. 

![](Integration-with-other-widgets_images/Integration-with-other-widgets_img1.png) 



