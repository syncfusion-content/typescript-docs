---
layout: post
title: Thumbnail
description: thumbnail 
platform: typescript
control: Rotator
documentation: ug
---

# Thumbnail 

This feature implements **Thumbnail** in **Rotator** control. You can view or access any of the Rotator items instantly. All the images are given as **Thumb Element** to use this feature. 

The property **showThumbnail** turns on or off thumbnail support in the **Rotator** control. Thumbnail is used to navigate between slides. Thumbnail supports only single slide transition. You must specify the source for thumbnail elements through the **thumbnailSourceID** property. The default value is ‘**false**’. The value set to this property is **boolean**. 

The property **thumbnailSourceID** specifies the source for thumbnail elements. The default value is **null**. The value set to this property is **object**. 

You can refer the following code example of Thumbnail in Rotator.

  {% highlight html %}
  
<div class="cols-sample-area">
   <ul id="sliderContent">
      <li>
         <img class="image" src="../images/rotator/green.jpg" title="green" />
      </li>
      <li>
         <img class="image" src="../images/rotator/snow.jpg" title="snow" />
      </li>
      <li>
         <img class="image" src="../images/rotator/wheat.jpg" title="wheat" />
      </li>
      <li>
         <img class="image" src="../images/rotator/tablet.jpg" title="tablet" />
      </li>
      <li>
         <img class="image" src="../images/rotator/sea.jpg" title="sea" />
      </li>
      <li>
         <img class="image" src="../images/rotator/bread.jpg" title="bread" />
      </li>
      <li>
         <img class="image" src="../images/rotator/snowfall.jpg" title="snowfall" />
      </li>
   </ul>
   <ul id="thumbElement" style="display: none">
      <li>
         <img src="../images/rotator/green.jpg" title="green" />
      </li>
      <li>
         <img src="../images/rotator/snow.jpg" title="snow" />
      </li>
      <li>
         <img src="../images/rotator/wheat.jpg" title="wheat" />
      </li>
      <li>
         <img src="../images/rotator/tablet.jpg" title="tablet" />
      </li>
      <li>
         <img src="../images/rotator/sea.jpg" title="sea" />
      </li>
      <li>
         <img src="../images/rotator/bread.jpg" title="bread" />
      </li>
      <li>
         <img src="../images/rotator/snowfall.jpg" title="snowfall" />
      </li>
   </ul>
</div>


  {% endhighlight %}


  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "600px",
            frameSpace: "0px",
            displayItemsCount: "1",
            slideHeight: "350px",
            navigateSteps: "1",
            enableResize: true,
            pagerPosition: ej.Rotator.PagerPosition.Outside,
            showThumbnail: true,
            thumbnailSourceID: "thumbElement",
            orientation: ej.Orientation.Horizontal,
            showPager: false,
            enabled: true,
            showCaption: false,
            allowKeyboardNavigation: true,
            showPlayButton: true,
            enableAutoPlay: false,
            animationType: "slide"
        });    
    });
}


  {% endhighlight %}


![](Thumbnail_images/Thumbnail_img1.png)

