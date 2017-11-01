---
layout: post
title: Keyboard-interaction
description: keyboard interaction
platform: typescript
control: Rotator
documentation: ug
---

# Keyboard interaction

The **Rotator** property **allowKeyboardNavigation** turns on keyboard interaction with the Rotator items. You must set this property to ‘**true**’ to access the keyboard shortcuts. The default value is ‘**true**’. The value set to this property is **Boolean**.

The entire Rotator commands are accessed through the keyboard by specifying the **Keyboard Shortcut** in the following table.

Keyboard shortcuts

<table>
<tr>
<th>
KeyboardShortcut	</th><th>
Function</th></tr>
<tr>
<td>
Alt + j</td><td>
Focuses the control</td></tr>
<tr>
<td>
UP</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Left</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Right</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item.</td></tr>
<tr>
<td>
End</td><td>
Navigates to the ending item.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
</table>


You can refer the following code example for **keyboard** navigation.


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
   <ul id="slide" style="display: none">
      <li>
         <img src="../images/rotator/nature.jpg" title="Nature" />
      </li>
      <li>
         <img src="../images/rotator/bird.jpg" title="Beautiful Bird" />
      </li>
      <li>
         <img src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" />
      </li>
      <li>
         <img src="../images/rotator/seaview.jpg" title="Sea-View" />
      </li>
      <li>
         <img src="../images/rotator/snowfall.jpg" title="Snow Fall" />
      </li>
      <li>
         <img src="../images/rotator/card.jpg" title="Credit Card" />
      </li>
      <li>
         <img src="../images/rotator/night.jpg" title="Colorful Night" />
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
            slideWidth: "550px",
            frameSpace: "0px",
            displayItemsCount: "1",
            slideHeight: "350px",
            navigateSteps: "1",
            enableResize: true,
            pagerPosition: ej.Rotator.PagerPosition.Outside,
            showThumbnail: true,
            thumbnailSourceID: "slide",
            orientation: ej.Orientation.Horizontal,
            enableRTL: true,
            showPager: false,
            enabled: true,
            showCaption: false,
            allowKeyboardNavigation: true,
            showPlayButton: true,
            animationType: "slide",
        });	      
    });
}


  {% endhighlight %}


Add the following code in your **JavaScript** to focus the control.

  {% highlight javascript %}

  
    //Control focus key
    $(document).on("keydown", function (e) {
        if (e.altKey && e.keyCode === 74) { // j- key code.
            $("#sliderContent")[0].focus();
        }
    });

  {% endhighlight %}
  
  
{% highlight css %}

<style type="text/css" class="cssStyles">
    .e-rotator-wrap .e-thumb .e-thumb-items li img {
        width: 130px;
        height: 82px;
    }
</style>


{% endhighlight %}



![](Keyboard-interaction_images/Keyboard-interaction_img1.png) 



