---
layout: post
title: Export
description: export
platform: Typescript
control: PivotChart
documentation: ug
keywords: ejpivotchart, pivotchart, js pivotchart
---

# Exporting

The PivotChart control can be exported to the following file formats.

* Excel
* Word
* PDF
* Image

The PivotChart control can be exported by invoking **“exportPivotChart”** method, with an appropriate export option as parameter.

{% tabs %}

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }       
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport", "fileName");
        }
    });
});

{% endhighlight %}

{% endtabs %}

## Excel Export

User can export contents of the PivotChart to Excel document for future archival, references and analysis purposes.

To achieve Excel export, service URL and file name is sent as the parameter.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }       
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport", "fileName");
        }
    });
});

{% endhighlight %}

## Word Export

User can export contents of the PivotChart to Word document for future archival, references and analysis purposes.

To achieve Word export, service URL and file name is sent as the parameter.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }       
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport", "fileName");
        }
    });
});

{% endhighlight %}

## PDF Export

User can export contents of the PivotChart to PDF document for future archival, references and analysis purposes.

To achieve PDF export, service URL and file name is sent as the parameter.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        }       
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport", "fileName");
        }
    });
});

{% endhighlight %}

## Image Export

User can export contents of the PivotChart to image format for future archival, references and analysis purposes. We can export PivotChart to the following image formats.

* PNG
* EMF
* JPG
* GIF
* BMP

To export PivotChart in PNG format, service URL, file name and **“ej.PivotChart.ExportOptions.PNG”** enumeration value is sent as the parameter. This is similar to other image formats.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        },
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport", "fileName", "png");
        }
    });
});

{% endhighlight %}

## Exporting Customization

You can add title and description to the exporting document by using title and description property obtained in the "beforeExport" event.

N> Title and description cannot be added to image formats.

{% tabs %}

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 100%"></div>
         <button id="button"></button>
         <div>
     </body>
</html>

{% endhighlight %}

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), {
        commonSeriesOptions: {
            type: ej.PivotChart.ChartTypes.Column
        },
        beforeExport: function(args) {
            args.title = "PivotChart";
            args.description = "Visualizes both OLAP and Relational datasource in graphical format";
        }        
     });
    var basicButton = new ej.Button($("#button"), {
        size: "large",
        showRoundedCorner: true,
        text: "Export",
        click: function (args) {
            let chartObj = $('.e-pivotchart').data("ejPivotChart");
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport", "fileName");
        }
    });
});

{% endhighlight %}

{% endtabs %}

The below screenshot shows the PivotChart control exported to Excel document.

![](Export_images/Export_ExcelClient.png)

The below screenshot shows the PivotChart control exported to Word document.

![](Export_images/Export_WordClient.png)

The below screenshot shows the PivotChart control exported to PDF document.

![](Export_images/Export_PDFClient.png)

The below screenshot shows the PivotChart control exported to PNG format.

![](Export_images/Export_PNGClient.png)