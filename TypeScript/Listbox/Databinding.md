---
layout: post
title: Databinding
description: databinding
platform: typescript
control: ListBox
documentation: ug
---

# Data binding

## Field mapping

The ListBox widget has a field property (object) which holds the properties to map with datasource fields. For example, the field object has a text property which is necessary to map with specific field in the datasource to render the items in the ListBox widget.

The field object contains the following properties.

* [text](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [toolTipText](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [id](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [selectBy](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [groupBy](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [checkBy](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [tableName](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [imageUrl](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [imageAttributes](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [spriteCssClass](https://help.syncfusion.com/api/js/ejlistbox#members:fields)

* [htmlAttributes](https://help.syncfusion.com/api/js/ejlistbox#members:fields)


## Local data

The local data can be an array of JSON objects which is assigned for the ListBox widget’s datasource property. Refer the below example. 

Here the bikeName and bikeId fields are mapped with text and id properties of the field object respectively.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module ListBoxComponent {
    $(function () {
            bikeList = [{ bikeId: "bk1", bikeName: "Apache RTR" },
                { bikeId: "bk2", bikeName: "CBR 150-R" },
                { bikeId: "bk3", bikeName: "CBZ Xtreme" },
                { bikeId: "bk4", bikeName: "Discover" },
                { bikeId: "bk5", bikeName: "Dazzler" },
                { bikeId: "bk6", bikeName: "Flame" },
                { bikeId: "bk7", bikeName: "Fazer" },
                { bikeId: "bk8", bikeName: "FZ-S" },
                { bikeId: "bk9", bikeName: "Pulsar" },
                { bikeId: "bk10", bikeName: "Shine" },
                { bikeId: "bk11", bikeName: "R15" },
                { bikeId: "bk12", bikeName: "Unicorn" }];

          var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource:bikeList,
                fields: { id: "bikeId", text: "bikeName" }
            });
        });
}

{% endhighlight %}



![](Databinding_images\Databinding_img1.png)

## Remote data

### OData

[OData](https://help.syncfusion.com/js/datamanager/data-binding) is a standardized protocol for creating and consuming the data. You can retrieve data from OData service by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started).

Here the CustomerID field is mapped with text property of the field object. The queries can be created using [ej.Query()](https://help.syncfusion.com/js/datamanager/query).

{% highlight html %}

<ul id="listbox">
</ul>
    <script type="text/javascript">
           $(function () {
            //create data manager
            var dataManager = ej.DataManager({
                //OData service
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // create query
            var query = ej.Query().from("Customers").take(10);
            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: dataManager,
                fields: { text: "CustomerID" },
                query: query
            });
        });
    </script>


{% endhighlight %}



![](Databinding_images\Databinding_img2.png)

### WebAPI



[ASP.NET Web API](https://msdn.microsoft.com/en-us/library/hh833994%28v=vs.108%29.aspx) is a Framework for building HTTP services. You can retrieve data from ASP.NET Web API by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started).



{% highlight javascript %}


         $(function () {
            //create data manager
            var dataManager = ej.DataManager({
                //ASP.NET Web API
                url: "http://mvc.syncfusion.com/UGService/api/Orders",
                crossDomain: true
            });

            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: dataManager,
                fields: { text: "CustomerID" }
            });

        });



{% endhighlight %}



N>  In the above data manager configuration, “crossDomain” must be set to true to access the data from Web API.

 {% seealso %} [Cross domain](https://help.syncfusion.com/js/grid/data-binding) {% endseealso %}

![](Databinding_images\Databinding_img3.png)

### Virtual Scrolling

 The ListBox widget provides support to load its data on demand via scrolling behavior to improve the application’s performance. This can be achieved using `allowVirtualScrolling` property. There are two ways to load data based on the scrolling type.

1. Normal scrolling

2. Continuous Scrolling

The scrolling type can be defined via `virtualScrollMode` property.

#### Normal Scrolling

This mode allows you to load the list box data while scrolling i.e. each time the scroll bar is scrolled, it will send request to the server to load the data.

{% highlight javascript %}


        $(function () {
            //create data manager
            var dataManager = ej.DataManager({
                //OData service
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // create query
            var query = ej.Query().from("Customers");

            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: dataManager,
                fields: { text: "CustomerID" },
                query: query,
                allowVirtualScrolling: true

            });
        });




{% endhighlight %}



N> By default, the value of “virtualScrollMode” property is normal.

![](Databinding_images\Databinding_img4.png)

![](Databinding_images\Databinding_img5.png)


#### Continuous Scrolling

This mode allows you to load the list box data when the scrollbar reaches the end point. In this mode, we can specify the number of items to be loaded per request.

The number of items to be loaded per request can be specified using the “itemRequestCount” property.

{% highlight javascript %}


       $(function () {
            //create data manager
            var dataManager = ej.DataManager({
                //OData service
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // create query
            var query = ej.Query().from("Customers");

            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: dataManager,
                fields: { text: "CustomerID" },
                query: query,
                allowVirtualScrolling: true,
                // specifying the scroll mode
                virtualScrollMode: ej.VirtualScrollMode.Continuous,
                //specifying the number of items to be loaded per request
                itemRequestCount: 10
            });
        });



{% endhighlight %}


![](Databinding_images\Databinding_img6.png)

![](Databinding_images\Databinding_img7.png)


### Handling errors

 In remote binding, the server might not return data sometimes due to various reasons. In such cases we need to handle the error properly. We can handle it using the “actionFailure” event. 

{% seealso %} [actionComplete](https://help.syncfusion.com/api/js/ejlistbox#events:actioncomplete) and [actionSuccess](https://help.syncfusion.com/api/js/ejlistbox#events:actionsuccess) {% endseealso %}



{% highlight javascript %}


     $(function () {
            //create data manager
            var dataManager = ej.DataManager({
                //OData service
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // create query
            var query = ej.Query()
                   .from("Customers").take(10);

            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: dataManager,
                fields: { text: "CustomerID" },
                query: query,
                actionFailure: "onFailure"
            });
        });

        function onFailure(args) {
            //handle errors
        }



{% endhighlight %}


![](Databinding_images\Databinding_img8.png)













