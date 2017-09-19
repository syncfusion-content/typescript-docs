---
layout: post
title: Data binding in DropDownList widget 
description: Describes about the data binding in DropDownList widget 
platform: Typescript
control: DropDownList
documentation: ug
keywords: DropDownList, dropdown, data binding, REStFul Binding, WebAPI, Web Method, OData, OData4
---

# Data Binding

To populate data in the DropDownList widget, define [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property with associated fields. In DropDownList, can bind either local array or OData, WebApi and other [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) services.

## Fields

The below listed fields are the data collection fields which maps fields for the data items of the DropDownList. 

<table>
    <tr>
        <th>
            Properties
            <br/>
        </th>
        <th>
            Description
            <br/>
        </th>
    </tr>
    <tr>
        <td>
            dataSource
            <br/>
        </td>
        <td>
            The data source contains the list of data for generating the popup list items.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            query
            <br/>
        </td>
        <td>
            It specifies the query to retrieve the data from the online server.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            fields
            <br/>
        </td>
        <td>
            It specifies the mapping fields for the data items of the DropDownList widget.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            id
            <br/>
        </td>
        <td>
            It specifies the ID of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            text
            <br/>
        </td>
        <td>
            It specifies the text content of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            value
            <br/>
        </td>
        <td>
            It specifies the value of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            groupBy
            <br/>
        </td>
        <td>
            It is used to categorize the items based on a specific field.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            imageUrl
            <br/>
        </td>
        <td>
            It defines the image location.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            imageAttributes
            <br/>
        </td>
        <td>
            It defines the image attributes such as height, width, styles, etc.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            spriteCssClass
            <br/>
        </td>
        <td>
            It defines the sprite CSS for the image tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            htmlAttributes
            <br/>
        </td>
        <td>
            It defines the HTML attributes such as class and styles for an item.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            selected
            <br/>
        </td>
        <td>
            This field defines the tag value to be selected initially. Corresponding field mapped has Boolean values to select the list items on control creation. The data with value true in this field is selected automatically when the control is initialized with checkbox.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            tableName
            <br/>
        </td>
        <td>
            It defines the table name for the tag value or displays text while rendering remote data.
            <br/>
        </td>
    </tr>
</table>

## Local Data

Define a JSON array and initialize the widget with [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property. Specify the column names in the [fields](#Fields) property.

N> The columns are bounded automatically when the fields are specified with the default names like id, text, etc...

{% highlight html %}

	<input type="text" id="dropdown1" />
    
{% endhighlight %}

{% highlight css %}

    	.imgId {
        	margin: 0;
        	padding: 3px 10px 3px 3px;
        	border: 0 none;
        	width: 60px;
        	height: 60px;
        	float: none;
    	}

{% endhighlight %}

{% highlight javascript %}
	
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
        var List = [{
            text: "Erik Linden",
            role: "Representative",
            country: "England",
            img: "images/Employee/3.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "John Linden",
            role: "Representative",
            country: "Norway",
            img: "images/Employee/6.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "Louis",
            role: "Representative",
            country: "Australia",
            img: "images/Employee/7.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "Lawrence",
            role: "Representative",
            country: "India",
            img: "images/Employee/8.png",
            attr: {
                class: "imgId"
            }
        }];
    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: List,
            fields: {
                text: "text",
                value: "country",
                groupBy: "role",
                imageUrl: "img",
                imageAttributes: "attr"
            },
            width: "200px"
        });
    });	
}
{% endhighlight %}

![](DataBinding_images/DataBinding_img1.jpeg)

N> Images for this sample are available in (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\samples\web\themes\images<br/>
I> htmlAttributes and imageAttributes should have JSON type value and sample for spriteCSSClass field is available in [here](http://jsplayground.syncfusion.com/Sync_px3jew3i) 
	
The JSON array to the [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property can also be provided as an instance of the [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager). When the JSON array is passed as an instance of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager), the [ej.JsonAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#json-adaptor) will be used to manipulate the DropDownList data source. The following code explains this behavior,

{% highlight html %}

	<input type="text" id="dropdown1" />
	
{% endhighlight %}

{% highlight javascript %}	
  
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
        var items = [{
            text: "ListItem 1",
            value: "item1"
        }, {
            text: "ListItem 2",
            value: "item2"
        }, {
            text: "ListItem 3",
            value: "item3"
        }, {
            text: "ListItem 4",
            value: "item4"
        }, {
            text: "ListItem 5",
            value: "item5"
        }];
  
        //Passing as instance to the DataManager 
    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: ej.DataManager(items)
        });
  
    });
}
{% endhighlight %}


## Binding Remote Data Service

To bind remote data to the DropDownList, assign a service data as an instance of `ejDataManager` to the `dataSource` property.

### OData

OData is a standardized protocol for creating and consuming data. Provide the [OData service](http://www.odata.org/) URL directly to the "ej.DataManager" class and then you can assign it to DropDownList "dataSource".

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
     $(function() {
        var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders");
        var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: dataManager,
            fields: {
                text: "ShipCountry",
                value: "OrderID"
            }
        });
    });       
}
{% endhighlight %}
           
          
## Virtual Scrolling 

To improve the performance when displaying large data set, you can use “allowVirtualScrolling” and [virtualScrollMode](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) property. This retrieves only a fixed amount of list items and loads remaining data on scrolling. The items will be fetched via AJAX request.

This supports two modes of virtualization. They are,

* Normal Mode
* Continuous Mode

I> 1. Sorting and Grouping is not supported with Virtual Scrolling
I> 2. “virtualScrollMode” property accepts both the string and ej.VirtualScrollMode enum value.

### Normal Mode

It loads the data on scrolling the list of items. This can be achieved by setting [normal](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) value to the "virtualScrollMode" property.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
 /// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent { 
        $(function() { 
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders"
            });
            
      var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: dataManager,
            fields: {
                text: "ShipName",
                value: "ShipCountry"
            },
            allowVirtualScrolling: true,
            virtualScrollMode: ej.VirtualScrollMode.Normal,
            itemsCount: 7
        });
    });
}  

{% endhighlight %}

### Continuous Mode

It loads the set of items when the scroller reaches at the end. This behaves like infinity scrolling. So when scroll reaches the end, it will fetch the remaining set of items and bind with your DropDownList. This can be achieved by setting [continuous](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) value to the "virtualScrollMode" property.

N> In both modes, set of items will be fetched based on the count specified in the [itemsCount](https://help.syncfusion.com/api/js/ejdropdownlist#members:itemscount) property and next set of items will be loaded on scrolling.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {   
   $(function() {        
        var dataManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders"
       });
        
     var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: dataManager,
            fields: {
                text: "ShipName",
                value: "ShipCountry"
            },
            allowVirtualScrolling: true,
            virtualScrollMode: ej.VirtualScrollMode.Continuous,
            itemsCount: 7
            });
        });
 }  

{% endhighlight %}
