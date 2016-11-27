---
layout: post
title: getting-started
description: getting started
platform: typescript
control: rotator
documentation: ug
---

# Getting Started

This section helps to get started of the Rotator control in a typescript application.

![](Getting-Started_images/getting-started_img1.png) 

## Create a Rotator

The following step by step guidelines will help you to add a Rotator control.

1) Refer the common Typescript [Getting Started Documentation]() to create an application and add necessary scripts and styles for rendering the Rotator control.

2) Create an HTML page and add the scripts and css references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Typescript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>
<body>
    <!--Add Rotator code here-->
</body>
</html>

{% endhighlight %}

3) Add the below mentioned code with in the <body> tag to render the Rotator control in the application. 

{% highlight html %}

    <div class="frame">
        <ul id="sliderContent">
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/nature.jpg" title="Nature" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/bird.jpg" title="Beautiful Bird" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/tablet.jpg" title="Tablet" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/wheat.jpg" title="Wheat" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/snowfall.jpg" title="Snow Fall" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/card.jpg" title="Credit Card" />
            </li>
            <li>
                <img class="image" src="http://js.syncfusion.com/demos/web/content/images/rotator/night.jpg" title="Colorful Night" />
            </li>
        </ul>
    </div>

{% endhighlight %}

## Initialize the control

Initialize the Rotator in ts file by using the ej.Rotator method.

{% highlight ts %}

    /// <reference path="../tsfiles/jquery.d.ts" />
    /// <reference path="../tsfiles/ej.web.all.d.ts" />\

 module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "100%",
            frameSpace: "0px",
            slideHeight: "auto",
            displayItemsCount: "1",
            navigateSteps: "1",
            pagerPosition:"outside",
            orientation: "horizontal",
            showPager: true,
            enabled: true,
            showCaption: true,
            allowKeyboardNavigation: true,
            showPlayButton: true,
            isResponsive:true,
            animationType: "slide",
        });
    });
 }

{% endhighlight %}

Get the following output from the above mentioned code

![](Getting-Started_images/getting-started_img2.png)



> _Note:_ _You can find the Rotator properties from the_ [API reference](https://help.syncfusion.com/api/js/ejrotator) _document_

