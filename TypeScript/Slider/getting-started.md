---
layout: post
title: getting-started
description: getting started
platform: js
control: Slider
documentation: ug
---

# Getting Started



Using the following steps, you can create a **TypeScript** Slider component.

## Creating an Slider in TypeScript



You can create a **TypeScript** application with the help of the given [TypeScript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

 Within an index.html file and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>TypeScript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>

</head>
<body>
    <!--Add Slider sample  here-->
</body>
</html>


{% endhighlight %}



The Slider can be created from a HTML `div` element with the HTML `id` attribute and pre-defined options set to it.



{% highlight html %}

<div id="minSlider"></div>
<script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module SliderComponent {
$(function () {
    var slider = new ej.Slider($("#minSlider"), {
        sliderType: "MinRange",
        height: "16px",
        width: "300px",
        value: 60
    });
});
}

{% endhighlight %}



* Now build your application, so that the **app.ts** file will compiled and automatically generated the **app.js** file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file by compiling     build the application.



Execution of above code will render the following output.

![](getting-started_images/getting-started_img1.png)


## set min and max values

* To set the maximum/ending value of the Slider, you can use the maxValue property. By default its value is 100. Data type of this property is “number”.


{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module SliderComponent {
$(function () {
    var slider = new ej.Slider($("#minSlider"), {
        sliderType: "MinRange",
        height: "16px",
        width: "300px",
        value: 60,
        maxValue: 50,
    });
});
}

{% endhighlight %}


* To set the minimum/starting value of the Slider, you can use the minValue property. By default its value is 0. Data type of this property is “number”.


{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module SliderComponent {
$(function () {
    var slider = new ej.Slider($("#minSlider"), {
        sliderType: "MinRange",
        height: "16px",
        width: "300px",
        value: 60,
        minValue: 50,
    });
});
}

{% endhighlight %}








