---
title: Getting Started for Typescript PivotTreeMap
description: How to create a PivotTreeMap with data source.
platform: Typescript
control: PivotTreeMap
documentation: ug
keywords: ejpivottreemap, pivottreemap, js pivottreemap
---

# Getting Started

This section explains you the steps required to populate the PivotTreeMap with data source. This section covers only the minimal features that you need to know to get started with the PivotTreeMap.

For common steps of typescript , you can refer [here](https://help.syncfusion.com/js/typescript).

The default type definition file ej.web.all.d.ts needs to include the support for type-checking while initializing any of the Syncfusion widgets. 

The important step you need to do is to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (app.ts file), so that you will get the intelliSense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the jquery.d.ts file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

## Script and CSS Reference

Add the scripts and CSS references to the “index.html” page as the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
    <script src="https://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    <script src="app.js"></script>
</head>
<body>
</body>
</html>

{% endhighlight %}

In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/# "") utility to generate a custom script file with the required widgets for deployment purpose.

### Control Initialization

Add a `div` container to render the PivotTreeMap.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotTreeMap1" style="min-height: 275px; min-width: 525px; height: 460px; width: 99%"></div>

         <!--Tooltip labels can be localized here-->
         <script id="tooltipTemplate" type="application/jsrender">
            <div style="background:White; color:black; font-size:12px; font-weight:normal; border: 1px solid #4D4D4D; white-space: nowrap;border-radius: 2px; margin-right: 25px; min-width: 110px;padding-right: 5px; padding-left: 5px; padding-bottom: 2px ;width: auto; height: auto;">
            <div>Measure(s) : {{:~Measures(#data)}}</div><div>Row : {{:~Row(#data)}}</div><div>Column : {{:~Column(#data)}}</div><div>Value : {{:~Value(#data)}}</div>
            </div>
         </script>  
     </body>
</html>

{% endhighlight %}

Initialize the PivotTreeMap in ts file by using the `ej.PivotTreeMap` method.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotTreeMap($("#PivotTreeMap1"), { });
});


{% endhighlight %}

### Populate PivotTreeMap with data

Let us now see how to populate the PivotTreeMap control using a sample JSON data as shown below.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotTreeMap($("#PivotTreeMap1"), {
        dataSource: {
            data: "http://bi.syncfusion.com/olap/msmdpump.dll;Locale Identifier=1033;",
            catalog: "Adventure Works DW 2008 SE",
            cube: "Adventure Works",
            rows: [
                {
                    fieldName: "[Date].[Fiscal]"
                }
            ],
            columns: [
                {
                    fieldName: "[Customer].[Customer Geography]"
                }
            ],
            values: [
                {
                    measures: [
                        {
                            fieldName: "[Measures].[Customer Count]",
                        }
                    ],
                    axis: "columns"
                }
            ],
            filters: []
        }
    });
});


{% endhighlight %}

The above code will generate a simple PivotTreeMap with customer count over a period of fiscal years across different customer geographic locations.

![](getting-started_images/Olap.png)