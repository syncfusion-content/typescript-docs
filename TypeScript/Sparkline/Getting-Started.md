---
layout: post
title: Getting-Started
description: getting started
platform: typescript
control: Sparkline
documentation: ug
---
# Getting Started

This section explains you the steps required to populate the Sparkline with data, tooltips and type for Sparkline. This section covers only the minimal features that you need to know to get started with the Sparkline.


## Create your sparkline

You can easily create the Sparkline widget by using the following steps.

1.First create an TypeScript Project and add the following script reference in the app.ts page 
For common getting started of TypeScript , you can refer [here](https://help.syncfusion.com/js/typescript).

The default type definition file **ej.web.all.d.ts** needs to include the support for type-checking while initializing any of the Syncfusion widgets. 

The important step you need to do is to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (app.ts file), so that you will get the intelliSense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the **jquery.d.ts** file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

2.Add the following script reference in the HTML page  

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
</head>
<body>
</body>
</html>
{% endhighlight %}
In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/# "") utility to generate a custom script file with the required widgets for deployment purpose.

3.Create a <div> tag.
	
   {% highlight html %}

<html> <body> <div id="Sparkline"></div> </body> </html>

{% endhighlight %}
   


4.Initialize the Sparkline in ts file by using the `ej.Sparkline` method. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"));
    });
}

{% endhighlight %}

Now, the Sparkline is rendered with some auto-generated random values and with default Line type Sparkline.

![](Getting-Started_images/Getting-Started_img1.jpg)

Simple Sparkline
{:.caption}

 The Sparkline is rendered to it's default size. You can also customize the Sparkline dimension either by setting the width and height of the container element as in the above code example or by using the **size** of the Sparkline.


## Populate Sparkline with data

Now, this section explains how to plot JSON data to the Sparkline. First, let us prepare a sample JSON data with each object containing following fields – employeeId and sales.

var sparklineData = [
{ employeeId: 1, sales: 25 },
{ employeeId: 2, sales: 28 },
{ employeeId: 3, sales: 34 },
{ employeeId: 4, sales: 32 },
{ employeeId: 5, sales: 40 },
{ employeeId: 6, sales: 32 },
{ employeeId: 7, sales: 35 },
{ employeeId: 8, sales: 55 },
{ employeeId: 9, sales: 38 },
{ employeeId: 10, sales: 30 }];

Now, add the dataSource to the Sparkline and provide the field name to get the values from the dataSource in xName and yName options.

{% highlight javascript %}
$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
           dataSource: sparklineData,
            xName: "employeeId",
            yName: "sales",
            
           });
});


{% endhighlight %}


## Sparkline Type 

 To change the sparkline types, following example code illustrates this.
{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            type:"column"
           });
});

{% endhighlight %}


## Enable Tooltip

To enable the Sparkline tooltip we can see the current point values.

The following code example illustrates enable tooltip in sparkline,

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            tooltip: {
                visible: true,
                   },
           });
});
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img2.png)
