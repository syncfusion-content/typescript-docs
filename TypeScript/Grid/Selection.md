---
layout: post
title: Selection with Grid widget for Syncfusion Essential Typescript
description: How to enable selection and its functionalities
platform: Typescript
control: Grid
documentation: ug
--- 
# Selection

The Selection provides an interactive support to highlight the row, cell or column that you select. Selection can be done through simple Mouse down or Keyboard interaction. To enable selection, set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") as `true`. 

## Types of Selection

There are two types of selections available in Grid. They are as follows:

1. Single 
2. Multiple 

### Single Selection

Single selection is an interactive support to select a specific row, cell or column in grid by mouse or keyboard interactions. To enable single selection set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `single` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

### Multiple Selections

Multiple selections is an interactive support to select a group of rows, cells or columns in grid by mouse or keyboard interactions. To enable multiple selections set the [`selectionType`](https://help.syncfusion.com/api/js/ejgrid#members:selectiontype "selectionType") property as `multiple` and also set the [`allowSelection`](https://help.syncfusion.com/api/js/ejgrid#members:allowselection "allowSelection") property as `true`.

## Row Selection

Row selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `row`. For random row selection, press **"Ctrl + mouse left"** click and for continuous row selection press **"Shift + mouse left"** click on the grid rows. To unselect the selected rows, press **"Ctrl + mouse left"** click on the selected row.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging : true,
            allowSelection : true,
            selectionType : "multiple",
            selectionSettings: {selectionMode: ["row"] },
            columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img1.png)

## Multiple Row Selection using Checkbox Column

Select multiple rows in grid by using the Checkbox column and it can be enabled by setting column `type` as `checkbox`. It also provides the option to select/deselect all the rows in Grid using a checkbox in the corresponding column header.

If the `field` property of Checkbox column is not defined, then it acts as a template column. So, the `field` property is necessary to perform grid actions like sorting, editing, etc., for the corresponding Checkbox column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
            columns: [
                { type: "checkbox", width: 50 }, //enables the checkbox column
                { field: "OrderID", isPrimaryKey: true, width: 80, textAlign: ej.TextAlign.Right },
                { field: "CustomerID", headerText: "Customer ID", width: 75 },
                { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                { field: "Freight", headerText: "Freight", width: 75, textAlign: ej.TextAlign.Right, format: "{0:C}" },
            ]
        });
    });
}
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img6.png)

## Cell Selection

Cell selection is enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `cell`. For random cell selection, press **"Ctrl + mouse left"** click and for continuous cell selection, press **"Shift + mouse left"** click on the grid cells. To unselect selected cells, press **"Ctrl + mouse left"** on the selected cell.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
            allowSelection: true,
            selectionType: "multiple",
            selectionSettings: { selectionMode: ["cell"] },
            columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img2.png)


### Cell Selection Mode

There are two types of cell selection available in grid. They are as follows:

1. Continuous Selection
2. Box Selection

Box cell selection is to select multiple cells vertically based on the initial column index selection.  

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
            allowSelection: true,
            selectionType: "multiple",
            selectionSettings: { selectionMode: ["cell"], cellSelectionMode: ej.Grid.CellSelectionMode.Box },
            columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img3.png)


## Column Selection

[Column selection](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "Column selection") can be enabled by setting the [`selectionMode`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-selectionmode "selectionMode") property of [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `column`. For random column selection, press **"Ctrl + mouse left click"** and for continuous column selection, press **"Shift + mouse left click"** on the top of the column header. To unselect selected columns, press **"Ctrl + mouse left click"** on top of the selected column header.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
            allowSelection: true,
            selectionType: "multiple",
            selectionSettings: { selectionMode: ["column"] },
            columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](selection_images/selection_img4.png)


## Touch options

While using the Grid in a [touch](https://help.syncfusion.com/api/js/ejgrid#members:enabletouch "touch") device environment, there is an option for multi selection through single tap on the row and it will show a popup with multi-selection symbol. Tap the icon to enable multi selection in a single tap.

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging : true,
            allowSelection : true,
            selectionType : "multiple",
            columns : ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}



The following output is displayed as a result of the above code example.

![](selection_images/selection_img5.png)


## Toggle Selection

The [Toggle](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-enabletoggle "Toggle") selection allows to perform selection and unselection of the particular row, cell or column.  To enable toggle selection, set [`enableToggle`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings-enabletoggle "enableToggle") property of the [`selectionSettings`](https://help.syncfusion.com/api/js/ejgrid#members:selectionsettings "selectionSettings") as `true`. If you click on the selected row, cell or column then it will be unselected and vice versa. 

N> If multi selection is enabled, then first click on any selected row (without pressing Ctrl key), it will clear the multi selection and in second click on the same row, it will be unselected. 

The following code example describes the above behavior. 

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight ts %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var gridInstance = new ej.Grid($("#Grid"), {
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
            enableRowHover: false,
            selectionSettings: { enableToggle: true },
            columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
        });
    });
}
{% endhighlight %}