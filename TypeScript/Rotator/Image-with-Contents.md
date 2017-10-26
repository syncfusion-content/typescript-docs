---
layout: post
title: Image-with-Contents
description: image with contents 
platform: typescript
control: Rotator
documentation: ug
---

# Image with Contents 

This feature allows you to add text along with the **image** in **Rotator** control. This is achieved by splitting the content into two panels. In the following code example, image is given in the left panel and text is given in the right panel.

  {% highlight html %}
  
<html>
   <body>
      <div class="cols-sample-area">
         <ul id="sliderContent">
            <li>
               <div class="leftPanel">
                  <img src="../images/rotator/tablet.jpg" />
               </div>
               <div class="rightPanel blog">
                  <div class="contentPanel">Tablet </div>
                  <ul>
                     <li>A tablet computer, or simply tablet, is a mobile computer with display, circuitry and battery in a single unit.</li>
                     <li>
                        Tablets are equipped with sensors, including cameras, microphone, accelerometer and touchscreen,
                  </ul>
               </div>
            </li>
            <li>
               <div class="leftPanel">
                  <img src="../images/rotator/nature.jpg" />
               </div>
               <div class="rightPanel">
                  <div class="contentPanel">Nature </div>
                  <ul>
                     <li>The health of the natural environment is critical to the long-term future of the planet</li>
                     <li>Nature, in the broadest sense, is equivalent to the natural, physical, or material world or universe.</li>
                  </ul>
               </div>
            </li>
            <li>
               <div class="leftPanel">
                  <img src="../images/rotator/card.jpg" />
               </div>
               <div class="rightPanel credit">
                  <div class="contentPanel">Credit card </div>
                  <ul>
                     <li>A credit card is a payment card issued to users as a system of payment</li>
                     <li>It allows the card holder to pay for goods and services based on the holder's promise to pay for them</li>
                  </ul>
               </div>
            </li>
            <li>
               <div class="leftPanel">
                  <img src="../images/rotator/rose.jpg" />
               </div>
               <div class="rightPanel">
                  <div class="contentPanel">Rose </div>
                  <ul>
                     <li>A rose is a woody perennial of the genus Rosa, within the family Rosaceae</li>
                     <li>Flowers vary in size and shape and are usually large and showy,
                        There are over 100 species
                     </li>
                  </ul>
               </div>
            </li>
            <li>
               <div class="leftPanel">
                  <img src="../images/rotator/snowfall.jpg" />
               </div>
               <div class="rightPanel rightSide">
                  <div class="contentPanel">Snowfall </div>
                  <ul>
                     <li>Mt. Baker ski area in Washington State has the world record for snowfall at 1,140 inches of snow in the 1998/1999 winter season</li>
                     <li>Mt. Baker ski area is located near but not on the real 10,781 Mount Baker</li>
                  </ul>
               </div>
            </li>
         </ul>
      </div>
   </body>
</html>

  {% endhighlight %}


  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "600px",
            displayItemsCount: "1",
            slideHeight: "300px",
            navigateSteps: "1",
            enableResize: true,
            pagerPosition: ej.Rotator.PagerPosition.Outside,
            orientation: ej.Orientation.Horizontal,
            showPager: true,
            enabled: true,
            showCaption: false,
            allowKeyboardNavigation: true,
            showPlayButton: true,
            animationType: "slide",
            enableRTL: true
        });
    });
}	
  {% endhighlight %}


{% highlight css %}

<style type="text/css" class="cssStyles">
    #sliderContent > li {
        background-color: #9ee8d8;
    }

    #sliderContent > li .leftPanel {
        float: left;
        width: 700px;
        height: 300px;
        padding-right: 0px;
    }

    #sliderContent > li .leftPanel img {
        width: 700px;
        height: 300px;
    }

    #sliderContent .rightPanel {
        background-color: #FFFFFF;
        height: 259px;
        margin-left: 410px;
        margin-top: 21px;
        opacity: 0.5;
        padding-left: 10px;
        position: absolute;
        width: 260px;
    }

    #sliderContent .rightPanel.credit {
        opacity: 0.6;
    }

    #sliderContent .rightPanel.blog {
        background-color: black;
    }

    #sliderContent .rightPanel.blog li {
        color: white;
        list-style: none;
        line-height: 2;
    }

    #sliderContent .rightPanel.blog .contentPanel {
        padding-top: 30px;
        color: white;
    }

    #sliderContent .rightPanel .contentPanel {
        color: #000000;
        font-size: large;
        font-weight: bold;
        left: 16px;
        padding-top: 30px;
        position: relative;
    }

    #sliderContent .rightPanel li {
        color: black;
        list-style: none;
        line-height: 2;
    }

    #sliderContent .rightPanel.rightSide {
        margin-left: 20px;
        background-color: black;
    }

    #sliderContent .rightPanel.rightSide li {
        color: white;
        list-style: none;
        line-height: 2;
    }

    #sliderContent .rightPanel.rightSide .contentPanel {
        padding-top: 30px;
        color: white;
    }

    .rightPanel > ul {
        padding: 6px 17px 17px;
    }
</style>


{% endhighlight %}



![](Image-with-Contents_images/Image-with-Contents_img1.png)


## Display items

### Display Items count 

This property specifies the number of **Rotator** Items to be displayed. The default value is ‘**1’**. The value set to this property is **string** or **number**.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
          slideWidth: "200px", 
          displayItemsCount: 3,
          slideHeight: "165px"
        });
    });
}

{% endhighlight %}


{% highlight css %}

<style type="text/css" class="cssStyles">
    #sliderContent > li .image {
        width:200px;
        height:165px;
    }
</style>

{% endhighlight %}



![](Image-with-Contents_images/Image-with-Contents_img2.png)


### Navigate steps

This property specifies the number of **Rotator** Items to **navigate** on a single click (next/previous/play buttons). The **navigateSteps** property value must be less than or equal to the **displayItemsCount** property value. The default value is ‘**1**’. The value set to this property is **string** or **number**.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: 200,
             slideHeight: 165,
             displayItemsCount: 2,
             navigateSteps: 2 
        });
    });
}

{% endhighlight %}


{% highlight css %}


<style type="text/css" class="cssStyles">
    #sliderContent > li .image {
        width:200px;
        height:165px;
    }
</style>

{% endhighlight %}



![](Image-with-Contents_images/Image-with-Contents_img3.png)

### Start index

This property sets the **index** of the slide that is displayed first. The default value is ‘1’. The value set to this property is **string** or **number**.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: 500, 
            startIndex: 4 
        });
    });
}

{% endhighlight %}



![](Image-with-Contents_images/Image-with-Contents_img4.png) 

### Frame space

This property sets the space between the **Rotator** Items. The value set to this property is **string** or **number**.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: "500px",
             slideHeight: "300px",
             displayItemsCount: 2,
             frameSpace: "30px"
        });
    });
 }
{% endhighlight %}

## Animation 

**animationType** property specifies the **Animation** type for the **Rotator** Item. **animationType** options include slide, fastSlide, slowSlide, and other custom easing animationTypes. The default value is ‘**slide**’. The value set to this property is **string**. 

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: "500px", 
             animationType: "slowSlide" 
        });
    });
}

{% endhighlight %}

### Animation speed

This property sets the **speed** of slide transition. The default value is ‘**600**’. The value set to this property is **string** or **number**.

{% highlight javascript %}



/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "500px",
            animationSpeed: 3000
         });
    });
}


{% endhighlight %}

### Delay

This property sets the **delay** between the **Rotator** Items to move after the slide transition. The default value is **500**. The value set to this property is **string** or **number.**

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: "500px", 
             delay: 5000 
        });
    });
}


{% endhighlight %}

## Theme

**Rotator** control’s style and appearance are controlled based on **CSS** **classes**. In order to apply styles to the **Rotator** control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 17 theme support available for RadialMenu component, namely:

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


### cssClass

This property is used to set **root** **class** for **Rotator** control theme. The value set to this property is **string** type.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: 500,
             slideHeight: 300, 
             cssClass: "flat-lime" 
        });
    });
}


{% endhighlight %}



Add the following code in your **Css**.

{% highlight css %}

<style>
    .flat-lime {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}



![](Image-with-Contents_images/Image-with-Contents_img5.png)
