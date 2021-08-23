---
layout: post
title: Getting started with Typescript Grid Control | Syncfusion
description: Learn here all about getting started with Syncfusion Essential TypeScript Grid Control, its elements, and more.
platform: Typescript
control: Grid
documentation: ug
---
# Getting started with Typescript Grid

Before we start with the Grid,for common getting started of TypeScript please refer [this page](https://help.syncfusion.com/js/typescript) provides general information regarding integrating Syncfusion widget's.

To render the grid control in TypeScript platform, the important step you need to do is to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (grid.ts file), so that you will get the intellisense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the jquery.d.ts file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

In your TypeScript app folder, create “grid.ts” file and now refer these two files within the grid.ts file as shown below, 

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

## Script and CSS Reference

Add the scripts and CSS references to the “index.html” page as the order mentioned below and also define the Grid control.

The Grid control has the following list of external JavaScript dependencies.

* [jQuery](http://jquery.com/) 1.7.1 and later versions

* [jsRender](https://github.com/borismoore/jsrender) - to render the templates.


Refer to the internal dependencies in the following table.

<table>
<tr>
<th>
File                          </th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle data operation and is used while binding data to the JS controls.</td></tr>
<tr>
<td>
ej.touch.min.js</td><td>
Used to handle touch operations in touch-enabled devices</td></tr>
<tr>
<td>
ej.print.min.js</td><td>
Used to handle print operation in JS controls.</td></tr>
<tr>
<td>
ej.globalize.min.js</td><td>
It is referred when using localization in Grid.</td></tr>
<tr>
<td>
ej.draggable.min.js</td><td>
Used for drag and drop an element in JS controls.</td></tr>
<tr>
<td>
ej.grid.min.js</td><td>
The grid's main file.</td></tr>
<tr>
<td>
ej.pager.min.js</td><td>
It is referred when paging is used in the Grid.  </td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
It is referred when scrolling is used in the Grid.  </td></tr>
<tr>
<td>
ej.waitingpopup.min.js</td><td>
It is referred when the remote data binding is used in the Grid. The waiting popup shows while requesting the server for data.</td></tr>
<tr>
<td>
ej.dropdownlist.min.js</td><td rowspan = "8">
These files are used while enable the Editing and Filtering feature in the Grid.</td></tr>
<tr>
<td>
ej.dialog.min.js</td></tr>
<tr>
<td>
ej.button.min.js</td></tr>
<tr>
<td>
ej.autocomplete.min.js</td></tr>
<tr>
<td>
ej.datepicker.min.js</td></tr>
<tr>
<td>
ej.datetimepicker.min.js</td></tr>
<tr>
<td>
ej.timepicker.min.js</td></tr>
<tr>
<td>
ej.checkbox.min.js</td></tr>
<tr>
<td>
ej.editor.min.js</td></tr>
<tr>
<td>
ej.tooltip.js</td><td rowspan = "2">
It is referred when toolbar is enabled in Grid.</td></tr>
<tr>
<td>
ej.toolbar.min.js</td></tr>
<tr>
<td>
ej.menu.js</td><td>
It is referred when excel like filter menu or context menu is enabled.</td></tr>
<tr>
<td>
ej.radiobutton.js</td><td>
It is referred when filtering is enabled.</td></tr>
<tr>
<td>
ej.excelfilter.js</td><td>
It is referred when excel like filter menu is enabled.</td></tr>
</table>


To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file. So the complete boilerplate code is

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Essential Studio for JavaScript">
    <meta name="author" content="Syncfusion">
    <title></title>
    <!-- Essential Studio for JavaScript  theme reference -->
    <link rel="stylesheet" href="http://cdn.syncfusion.com/14.4.0.15/js/web/flat-azure/ej.web.all.min.css" />

    <!-- Essential Studio for JavaScript  script references -->
    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/14.4.0.15/js/web/ej.web.all.min.js"> </script>

    <!-- Add your custom scripts here -->
    <script type="text/javascript" src="grid.js"></script>    <!--Also refer grid.js file here -->
</head>
<body>
    <div id="Grid"></div>       <!-- Define the Grid control-->
</body>
</html>

{% endhighlight %}

N> In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/custom-script-generator)  to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server.

For themes, you can use the `ej.web.all.min.css` CDN link from the code example given. To add the themes in your application, please refer to [this link](http://help.syncfusion.com/js/theming-in-essential-javascript-components).In addition to that, refer the grid.js file in the script section.

Finally build your application, so that the “grid.js” file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in grid.ts file will be reflected in grid.js file automatically.


## Create a Grid

 The TypeScript grid can be created from a HTML `DIV` element with the HTML `id` attribute set to it and define these steps in “index.html” page.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
         <script>
	       var shipDetails = [
              { Name: 'Hanari Carnes', City: 'Brazil' },
              { Name: 'Split Rail Beer & Ale', City: 'USA' },
              { Name: 'Ricardo Adocicados', City: 'Brazil' }
           ];
        </script>
    </body>
</html>

{% endhighlight %}

Initialize the Grid in grid.ts file by using the `ej.Grid` method. Refer to the following code example.


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
           dataSource: shipDetails,
         });
    });
}

{% endhighlight %}

![Getting-started_images1](Getting-started_images/Getting-started_img1.png)
{:.image }


## Data Binding

[`Data binding`](http://help.syncfusion.com/js/grid/data-binding) in the grid is achieved by assigning an array of JavaScript objects to the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:columns-datasource) property. Refer to the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
          //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
          dataSource: window["gridData"];  
          columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"];
      });
    });
}

{% endhighlight %}


![Getting-started_images2](Getting-started_images/Getting-started_img2.png)
{:.image }

## Enable Paging

[`Paging`](http://help.syncfusion.com/js/grid/paging) can be enabled by setting the [`allowPaging`](http://help.syncfusion.com/js/api/ejgrid#members:allowpaging) to true. The Paging feature in Grid offers complete navigation support to easily switch between the pages, using the page bar available at the bottom of the Grid control

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"],
            allowPaging: true,
            pageSettings: { pageSize: 8 }         
      });
    });
}

{% endhighlight %}


![Getting-started_images3](Getting-started_images/Getting-started_img3.png)
{:.image }

N> Pager settings can be customized by using the `pageSize` of [`pageSettings`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-pagesize) property. When it is not given the default values for `pageSize` and `pageCount` are 12 and 8 respectively.


## Enable Filtering

[`Filtering`](/js/grid/filter) can be enabled by setting the [`allowFiltering`] (https://help.syncfusion.com/js/api/ejgrid#members:allowfiltering) to be `true`. By default, the filter bar row is displayed to perform filtering, you can change the filter type by using `filterType` of [`filterSetting`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings) property.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"],
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowFiltering: true         
      });
    });
}

{% endhighlight %}


![Getting-started_images4](Getting-started_images/Getting-started_img4.png)
{:.image }

## Enable Grouping

[`Grouping`](/js/grid/grouping) can be enabled by setting the [`allowGrouping`](http://help.syncfusion.com/js/api/ejgrid#members:allowgrouping) to `true`.  Columns can be grouped dynamically by drag and drop the grid column header to the group drop area. The initial grouping can be done by adding required column names in the `groupedColumns` of [`groupSettings`](http://help.syncfusion.com/js/api/ejgrid#members:groupsettings-groupedcolumns) property. 


{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"],
            allowPaging: true,
            pageSettings: { pageSize: 8 },           
            allowGrouping: true       
      });
    });
}

{% endhighlight %}


![Getting-started_images5](Getting-started_images/Getting-started_img5.png)
{:.image }

Refer to the following code example for initial grouping.


{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"],
            allowPaging: true,
            pageSettings: { pageSize: 8 },           
            allowGrouping: true,
            groupSettings: { groupedColumns: ["ShipCountry", "CustomerID"] }       
      });
    });
}

{% endhighlight %}


![Getting-started_images6](Getting-started_images/Getting-started_img6.png)
{:.image }


## Add Summaries

[`Summaries`](http://help.syncfusion.com/js/grid/summary) can be added by setting the [`showSummary`](http://help.syncfusion.com/js/api/ejgrid#members:showsummary) to true and adding required summary rows and columns in the [`summaryRows`](http://help.syncfusion.com/js/api/ejgrid#members:summaryrows) property. For demonstration, Freight column's sum value is displayed as summary.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="Grid"></div>
     </body>
</html>

{% endhighlight %}


{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"],
            allowPaging: true,
            pageSettings: { pageSize: 8 },           
            allowGrouping: true,
            groupSettings: { groupedColumns: ["CustomerID"] },
            showSummary: true,
            summaryRows: [
                {
                  	title: "Sum",
                  	summaryColumns: [
                    { summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Freight", dataMember: "Freight" }
              	  ]
              }
           ]       
      });
    });
}

{% endhighlight %}


![Getting-started_images7](Getting-started_images/Getting-started_img7.png)
{:.image }


