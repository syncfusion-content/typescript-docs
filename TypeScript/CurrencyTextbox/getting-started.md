---
layout: post
title: getting-started
description: getting started
platform: Typescript
control: CurrencyTextbox
documentation: ug
---

# Getting Started



Using the following steps, you can create a **Typescript** CurrencyTextbox component.

## Creating an CurrencyTextbox in TypeScript

You can create a **TypeScript** application with the help of the given [Typescript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

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


The CurrencyTextbox can be created from a `input` element with the HTML `id` attribute and pre-defined options set to it.

{% highlight html %}

<input id="currency" type="text" />
<script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
   var cur = new ej.CurrencyTextbox($("#currency"), {
            value: 100,
            name: "currency",
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
   var cur = new ej.CurrencyTextbox($("#currency"), {
            value: 100,
            maxValue: 1000,
            name: "currency",
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
