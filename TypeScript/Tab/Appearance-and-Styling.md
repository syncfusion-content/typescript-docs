---
layout: post
title: Appearance-and-Styling | Syncfusion
description: appearance and styling
platform: Typescript
control: Tab Control
documentation: ug
---

# Appearance and Styling

## Header Image Customization

To set the **Tab** header image for each **Tab** item you can specify image in &lt;span&gt; tag element during the **Tab** header declaration time.

The following code example is used to add the header image for the root **Tab** header element. 

Add the following **HTML** to render **Tab** with header image.

{% highlight html %}


 <div id="dish" style="width: 650px">
    <ul>
        <li><span class="dish pizzaImg"></span><a href="#pizza">Pizza Menu</a></li>
        <li><span class="dish sandwichImg"></span><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
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
    });
} 


{% endhighlight %}

Add following **CSS** for header image customization.

{% highlight css %}


<style type="text/css" class="cssStyles">
        .dish {
            display: inline-block;
            vertical-align: middle;
            margin: 0px -9px 0px 9px;           
        }
        .pizzaImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_chicken-delite.png") no-repeat;
            height: 25px;
            width: 25px;
        }
        .sandwichImg, .pastaImg {
            height: 25px;
            width: 25px;
        }
        .sandwichImg {
            background: url("http://js.syncfusion.com/UG/Web/Content/rsz_garden-fresh.png") no-repeat;
        }
</style> 


{% endhighlight %}

The following screenshot illustrates the **Tab** with the customized header image. 

![header](Appearance-and-Styling_images/Appearance-and-Styling_img1.png)

Header Image Customization
{:.caption}


## Rounded corner

By enabling ‘**showRoundedCorner’** property, you can customize the shape of the **Tab** widget from regular rectangular shape to rounded rectangle shape that is set to ‘**false**’ by default. 

The following code example is used to render the **Tab** widget with **Rounded Corner**.

Add the following **HTML** to render **Tab** with rounder corner.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
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
                 showRoundedCorner: true 
            });
        });
  }

{% endhighlight %}

The following screenshot illustrates the **Tab** with Rounded corner.

![Rounded](Appearance-and-Styling_images/Appearance-and-Styling_img2.png) 


## Enable/Disable

You can enable or disable the **Tab** widget by ‘**enabled’** property. By default, the property set to ‘**true**’**.**

The following code example is used to render the **Tab** widget with enable/disable.

Add the following **HTML** to render **Tab** with enable/disable.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

  
        // Add the following script to render Tab with disabled format.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                enabled: false
             });
        });
}

{% endhighlight %}

The following screenshot illustrates the **Tab** with disabled format.

![disabled](Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 


 ## Enabling Reload Icon
 
Without refresh/reload the whole page, you can reload a particular **Tab** using **Reload** icon. The **Reload** icon is appeared at right corner of the **Tab** by enabling the property ‘**showReloadIcon**’ to ‘**true**’. When you move cursor over the **Tab** headers, the **Reload** icon is displayed. By default the property value is set to ‘**false**’.   

The following code example is used to render the **Tab** widget with **Reload** icon.

Add the following **HTML** to render **Tab** with **Reload** icon.


{% highlight html %}

        
<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

        // Add the following script to render Tab with Reload icon.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                 showReloadIcon: true
             });
        });
}
{% endhighlight %}

The following screenshot illustrates the **Tab** with **Reload** icon.

![Reload](Appearance-and-Styling_images/Appearance-and-Styling_img4.png) 


## Collapsible Tabs

You can collapse the **Tab** content by enabling the ‘**collapsible’** property to ‘**true**’. When the property is set to ‘**true**’ then click the active **Tab** header, the **Tab** contents are hidden. By default, the property value is set to ‘**false**’.

The following code example is used to render the **Tab** widget with customized collapsible mode.

Add the following **HTML** to render **Tab** with customized collapsible mode.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
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
                 collapsible: true
             });
        });
}

{% endhighlight %}


The following screenshot illustrates the **Tab** with customized collapsible mode.

![collapsible](Appearance-and-Styling_images/Appearance-and-Styling_img5.png) 


## Adjusting Tab Size

### Height Adjust Mode and Height

The height of the **Tab** widget is customized by ‘**height**’ property. The **Tab** widget height depends on ‘**heightAdjustMode**’ property. Using the **heightAdjustMode** property, you can adjust height by “**content**”, “**auto**”, “**fill**”. By default the **heightAdjustMode** is set as **content**.

The following code example is used to render the **Tab** widget with customized height and height adjust mode.

Add the following **HTML** to render **Tab** with customized height and height adjust mode.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>


{% endhighlight %}

{% highlight javascript %}

    
           // Add the following script to render Tab with customized height and height adjust mode.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                    heightAdjustMode:"fill", 
                    height:"300px"
                }); 
           });
}
{% endhighlight %}


The following screenshot illustrates the **Tab** with customized height and height adjust mode.

![height](Appearance-and-Styling_images/Appearance-and-Styling_img6.png) 




### Width

The **width** of the **Tab** widget is customized by using ‘**width**’ property that accepts only the pixel values.

The following code example is used to render the **Tab** widget with customized width.

Add the following **HTML** to render **Tab** with customized width.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
        <p>Sandwich cooked to perfection tossed with bread, milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
</div>


{% endhighlight %}

{% highlight javascript %}

        // Add the following script to render Tab with customized width.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TabComponent {       
    $(function () {
         var sample = new ej.Tab($("#dish"),{
                 width:"450px"
             });
        });   
}

{% endhighlight %}

The following screenshot illustrates the **Tab** with customized width.

![width](Appearance-and-Styling_images/Appearance-and-Styling_img7.png) 


## Theme

**Tab** control’s style and appearance are controlled based on **CSS** classes. In order to apply styles to the **Tab** control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 16 theme support available for RadialMenu component, namely:

* flat-azure
* flat-azure-dark
* fat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap
* high-contrast-01
* high-contrast-02
* material
* office-365

## Custom styles

The style of the **Tab** widget is customized by ‘**cssClass**’ property. 

The following code example is used to render the **Tab** widget with customized style.

Add the following **HTML** to render **Tab** with customized style.

{% highlight html %}


<div id="dish" style="width: 650px">
    <ul>
        <li><a href="#pizza">Pizza Menu</a></li>
        <li><a href="#sandwich">Sandwich Menu</a></li>
    </ul>
    <div id="pizza" style="background-color: #F5F5F5">
        <!--Food item description-->
        <p>Pizza cooked to perfection tossed with milk, vegetables, potatoes, poultry, 100% pure mutton, and cheese - and in creating nutritious and tasty meals to maintain good health.</p>
    </div>
    <div id="sandwich" style="background-color: #F5F5F5">
        <!--dish description-->
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
                 cssClass: "custom"
             });
        });
}

{% endhighlight %}

Add the following styles

{% highlight css %}

<style type="text/css">
    .custom {
        width:650px;
    }
</style>
    

{% endhighlight %}

The following screenshot illustrates the **Tab** with customized style.

![customize](Appearance-and-Styling_images/Appearance-and-Styling_img8.png) 



