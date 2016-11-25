---
layout: post
title: Getting-Started
description: Getting Started
platform: typescript
control: RadialSlider
documentation: ug
---

# Getting Started

This section helps you to understand the getting started of the Radial Slider control with the step-by-step instructions.

## Create a Radial Slider control

The following steps guide you to add a Radial Slider control.

1)	Refer the common Typescript [Getting Started Documentation](https://help.syncfusion.com/js/typescript) to create an application and add necessary scripts and styles for rendering the RadialSlider control.

2)  Create an HTML page and add the scripts and css references in the order mentioned in the following code example.

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
    <!--Add Radial Slider code here-->
</body>
</html>

{% endhighlight %}

3)	Add the following code with in the <body> tag to render the RadialSlider control. 

{% highlight html %}

      <div id="radialSlider">
      </div>

{% endhighlight %}

Initialize the Radial Slider control in ts file by using the ej.RadialSlider method.

{% highlight ts %}

  /// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module RadialSliderComponent {
    $(function () {
        var radialsliderInstance = new ej.RadialSlider($("#radialSlider"), {
           innerCircleImageUrl: " http://js.syncfusion.com/demos/web/content/images/radialslider/chevron-right.png"
        });
    });
}


{% endhighlight %}

To get the following output from the above-mentioned code.

![](getting-started-images/getting-started-img.png)


N> You can find the Radial Slider control properties from the [API reference](https://help.syncfusion.com/api/js/ejradialslider).              
