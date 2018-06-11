---
title: Getting Started for Typescript Spreadsheet
description: How to create a Spreadsheet with data source, apply format and export it as excel file.
platform: Typescript
control: Spreadsheet
documentation: Ug
keywords: 
---

# Getting started

This section explains you the steps required to populate the Spreadsheet with data, format, and export it as excel file. This section covers only the minimal features that you need to know to get started with the Spreadsheet.

## Adding Script Reference

You can create a TypeScript application with the help of the given [Typescript Getting Started Documentation.](https://help.syncfusion.com/js/typescript)

In your TypeScript app folder, create “app.ts” file.

To get intellisense support and compile time type-checking, we need to follow the below steps,

1. Copy the `ej.web.all.d.ts` file from the below location into your project,

   (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript
2. Refer the file in your typescript application(app.ts file).

It is also necessary to refer `jquery.d.ts` in typescript application(app.ts file), which can be downloaded [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

Add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
        <script src="https://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
        <script src="http://js.syncfusion.com/demos/web/scripts/xljsondata.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
</head>
<body>
</body>
</html>

{% endhighlight %}

In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/) utility to generate a custom script file with the required widgets for deployment purpose.

**Note:**

* For details about Spreadsheet internal and external dependencies refer following [link](https://help.syncfusion.com/js/spreadsheet/dependencies)

## Initialize Spreadsheet

Add a `div` container to render the Spreadsheet.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Spreadsheet"></div>
     </body>
</html>

{% endhighlight %}

Initialize the Spreadsheet in `app.ts` file by using the `ej.Spreadsheet` method. The Spreadsheet is rendered based on default width and height. You can also customize the Spreadsheet dimension by setting the `width` and `height` property in `scrollSettings`.

{% highlight js %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />
module SpreadsheetComponent {
    $(function () {
        var sample = new ej.Spreadsheet($("#Spreadsheet"), {});
    });
}

{% endhighlight %}

Finally build your application, so that the “app.js” file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file automatically.

Now, the Spreadsheet is rendered with default row and column count.

![](Getting-Started_images/Getting-Started_img1.png)

## Populate Spreadsheet with data

Now, this section explains how to populate JSON data to the Spreadsheet. You can set `dataSource` property in `sheet` settings to populate JSON data in Spreadsheet.

{% highlight js %}

module SpreadsheetComponent {
    $(function () {
        var sample = new ej.Spreadsheet($("#Spreadsheet"), {
            // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
            sheets: [{ rangeSettings: [{ dataSource: (<any>window).defaultData}] }]
        });
    });
}

{% endhighlight %}

![](Getting-Started_images/Getting-Started_img2.png)

## Apply Conditional Formatting 

Conditional formatting helps you to apply formats to a cell or range with certain color based on the cells values. You can use `allowConditionalFormats` property to enable/disable Conditional formats.

To apply conditional formats for a range use `cFormatRule` property. The following code example illustrates this,

{% highlight js %}

module SpreadsheetComponent {
    $(function () {
        var sample = new ej.Spreadsheet($("#Spreadsheet"), {
            sheets: [{
                rangeSettings: [{ dataSource: (<any>window).defaultData }],
                cFormatRule: [{ action: ej.Spreadsheet.CFormatRule.GreaterThan, inputs: ["10"], color: ej.Spreadsheet.CFormatHighlightColor.RedFill, range: "D2:D8" }]
            }]
        });
    });
}

{% endhighlight %}

![](Getting-Started_images/Getting-Started_img3.png)

## Export Spreadsheet as Excel File

The Spreadsheet can save its data, style, format into an excel file. To enable save option in Spreadsheet set `allowExporting` option in `exportSettings` as `true`. Since Spreadsheet uses server side helper to save documents set `excelUrl` in `exportSettings` option. The following code example illustrates this,

{% highlight js %}

module SpreadsheetComponent {
    $(function () {
        var sample = new ej.Spreadsheet($("#Spreadsheet"), {
            sheets: [{
                rangeSettings: [{ dataSource: (<any>window).defaultData }],
                cFormatRule: [{ action: ej.Spreadsheet.CFormatRule.GreaterThan, inputs: ["10"], color: ej.Spreadsheet.CFormatHighlightColor.RedFill, range: "D2:D8" }]
            }],
            exportSettings: {
                excelUrl:"http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/ExcelExport"
            }
        });
    });
}

{% endhighlight %}

Use shortcut `Ctrl + S` to save Spreadsheet as excel file.
