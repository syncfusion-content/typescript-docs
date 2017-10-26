---
layout: post
title: getting-started
description: getting started
platform: Typescript
control: NumericTextbox
documentation: ug
---

# Getting Started



Using the following steps, you can create a **Typescript** NumericTextbox component.

## Creating an NumericTextbox in TypeScript

You can create a **Typescript** application with the help of the given [Typescript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

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
<!--Add Textbox sample  here-->
</body>
</html>


{% endhighlight %}

The NumericTextbox can be created from a `input` element with the HTML `id` attribute and pre-defined options set to it.

{% highlight html %}

<input id="numeric" type="text" />
<script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
   var number = new ej.NumericTextbox($("#numeric"), {
            value: 30,
            minValue: 1,
            maxValue: 100,
            name: "numeric",
            width: "100%"
        });
}

{% endhighlight %}



* Now build your application, so that the **app.ts** file will compiled and automatically generated the **app.js** file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file by compiling     build the application.



Execution of above code will render the following output.

![](getting-started_images/getting-started_img1.png)


## set min and max values

* To set the maximum/ending value of the Textbox, you can use the maxValue property. Data type of this property is “number”.


{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
   var number = new ej.NumericTextbox($("#numeric"), {
            value: 30,
            maxValue: 100,
            name: "numeric",
            width: "100%"
        });
}
{% endhighlight %}


* To set the minimum/starting value of the Textbox, you can use the minValue property. Data type of this property is “number”.


{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module SliderComponent {
 $(function () {
        var number = new ej.NumericTextbox($("#numeric"), {
            value: 30,
            minValue: 1,
            maxValue: 100,
            name: "numeric",
            width: "100%"
        });
});
}

{% endhighlight %}
