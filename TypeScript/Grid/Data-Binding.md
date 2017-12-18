---
layout: post
title: DataBinding with Grid widget for Syncfusion Essential Typescript
description: How to bind in-memory JSON and remote web services in Grid
platform: Typescript
control: Grid
documentation: ug
--- 
# Data binding

The Grid control uses [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview# "ej.DataManager") which supports both RESTful JSON data services binding and local JSON array binding.  The [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property can be assigned either with the instance of [`ej.DataManger`](https://help.syncfusion.com/api/js/ejdatamanager# "ej.DataManager") or JSON data array collection. It supports different kinds of data binding methods such as

1. Local data
2. Remote data

## Local Data

To bind local data to the Grid, you can assign a JSON array to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property.

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
            //The datasource "window['gridData'] is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window["gridData"],
            allowPaging: true,
			columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]   
      });
    });
}
   
{% endhighlight %}


The following output is displayed as a result of the above code example.

![](dataBinding_images/dataBinding_img1.png)


N> 1. There is no in-built support to bind the XML data to the grid. But you can achieve this requirement with the help of [custom adaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor) concept. 
N> 2. Refer this [Knowledge Base link](http://www.syncfusion.com/kb/3377/how-to-process-xml-data-from-server-using-datamanager-and-bound-to-grid#) for bounding XML data to grid using custom adaptor. 

## Remote Data

To bind remote data to Grid Control, you can assign a service data as an instance of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property.

### OData

OData is a standardized protocol for creating and consuming data. You can provide the [OData service](http://www.odata.org/#) URL directly to the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") class and then you can assign it to Grid [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "datasource").

The following code example describes the above behavior.

{% highlight html %}

<div id="Grid"></div>

{% endhighlight %}

{% highlight ts %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GridComponent {
    $(function () {
        var dataManager = new ej.DataManager("http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/");
        var gridInstance = new ej.Grid($("#Grid"), {
            dataSource: dataManager,
			allowPaging:true,
			columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
      });
    });
}
	
{% endhighlight %}

	
The following output is displayed as a result of the above code example.

![](dataBinding_images/dataBinding_img2.png)

N> By default, if no adaptor is specified for [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") and only the url link is mentioned it will consider as ODataService. 