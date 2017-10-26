---
layout: post
title: Behavior-settings
description: behavior settings
platform: typescript
control: Rotator
documentation: ug
---

# Behavior settings

## Enabling rotator

The **“enabled”** property enables or disables the **Rotator** control. The default value is ‘**true**’. The value set to this property is **Boolean** type. You can refer the following code example to set this property.

  {% highlight html %}

  
<div class="cols-sample-area">
   <ul id="sliderContent" accesskey="e">
      <li>
         <img class="image" src="../images/rotator/nature.jpg" title="Nature" />
      </li>
      <li>
         <img class="image" src="../images/rotator/bird.jpg" title="Beautiful Bird" />
      </li>
      <li>
         <img class="image" src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" />
      </li>
      <li>
         <img class="image" src="../images/rotator/seaview.jpg" title="Sea-View" />
      </li>
      <li>
         <img class="image" src="../images/rotator/snowfall.jpg" title="Snow Fall" />
      </li>
      <li>
         <img class="image" src="../images/rotator/card.jpg" title="Credit Card" />
      </li>
      <li>
         <img class="image" src="../images/rotator/night.jpg" title="Colorful Night" />
      </li>
   </ul>
</div>


  {% endhighlight %}


  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             enabled: true
              });
    });
} 

  {% endhighlight %}
  
## Responsive rotator

The “isResponsive” property resizes the Rotator when the browser window is resized. The default value is ‘false’. The value set to this property is Boolean. 

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             isResponsive : true 
        });
    });
}
{% endhighlight %}

## Auto Play

The **Rotator** Items continuously rotate without user interference by enable the **enableAutoPlay** property. The default value is ‘**false’**. The value set to this property is **Boolean**. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            enableAutoPlay: true 
        });
    });
}
{% endhighlight %}

## Stop on hover

The **stopOnHover** property pauses the **auto play** while hover on the **Rotator** content. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             enableAutoPlay: true,
              stopOnHover: true
         });
    });
}

{% endhighlight %}

## Pager settings

### Pager position

This property specifies the position of the **showPager** in the **Rotator** Item. The default value is ‘**outside**’. The value set to this property is **string** or **enum**. 

* ej.Rotator.PagerPosition.BottomLeft
* ej.Rotator.PagerPosition.BottomRight
* ej.Rotator.PagerPosition.Outside
* ej.Rotator.PagerPosition.TopCenter
* ej.Rotator.PagerPosition.TopLeft
* ej.Rotator.PagerPosition.TopRight



{% highlight javascript %}

    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            pagerPosition: ej.Rotator.PagerPosition.BottomLeft,
            slideWidth: "630px",
            slideHeight: "350px"
        });
    });
}
{% endhighlight %}



![](Behavior-settings_images/Behavior-settings_img1.png)

### Show pager

The **“showPager”** property turns on or off the **pager** support in the **Rotator** control. The **Pager** is used to navigate the **Rotator** Items. The default value is ‘**true**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            showPager: false
         });
    });
}
{% endhighlight %}



![](Behavior-settings_images/Behavior-settings_img2.png)

## Show options

### Show play button

The “**showPlayButton**” property enables play / pause button on **Rotator**. The default value is ‘**false**’. The value set to this property is **Boolean**.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
             slideWidth: "600px", 
             showPlayButton: true 
         });
    });
}
{% endhighlight %}



![](Behavior-settings_images/Behavior-settings_img3.png)

### Show navigate button

The “**showNavigateButton**” property turns on or off the slide buttons (next and previous) in the **Rotator** Items. Slide buttons are used to navigate the **Rotator** Items. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "500px", 
            showNavigateButton: true 
        });
    });
}
{% endhighlight %}



![](Behavior-settings_images/Behavior-settings_img4.png) 

### Show caption

When the **Rotator** Item is an image, you can specify a caption for the **Rotator** Item. The caption text for each **Rotator** Item is set by using the title attribute of the respective **&lt;image&gt;** tag. The caption cannot be displayed when multiple **Rotator** Items are present. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "500px", 
            showCaption: true
         });
    });
}
{% endhighlight %}



![](Behavior-settings_images/Behavior-settings_img5.png) 

