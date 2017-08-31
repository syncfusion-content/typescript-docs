---
layout: post
title: Data-binding
description: data binding
platform: Typescript
control: Menu
documentation: ug
---

# Data binding

Data binding enables you to synchronize the elements with different sources of data. You can bind data using two ways, Local data and remote data. 

##Field Members

Field is a property that includes the object type. Fields are used to bind the data source and it includes following field members to make binding easier.

List of Field members

<table>
<tr>
<th>Name</th><th>Description</th></tr>
<tr>
<td>
dataSource</td><td>
datasource receives  Essential DataManager object and JSON object. </td></tr>
<tr>
<td>
Query</td><td>
It receives query to retrieve data from the table (query is same as SQL). Example:  ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);</td></tr>
<tr>
<td>
tableName</td><td>
It receives table name to execute query on the corresponding table</td></tr>
<tr>
<td>
Id</td><td>
Specifies the id to menu items list</td></tr>
<tr>
<td>
parentId</td><td>
Specifies the parent id of the table.</td></tr>
<tr>
<td>
Text</td><td>
Specifies the text of menu items list</td></tr>
<tr>
<td>
spriteCssClass</td><td>
Specifies the sprite CSS class to “li” item list</td></tr>
<tr>
<td>
linkAttribute</td><td>
Specifies the link attribute to “a” tag in item list</td></tr>
<tr>
<td>
imageAttribute</td><td>
Specifies the image attribute to “img” tag inside items list </td></tr>
<tr>
<td>
htmlAttribute</td><td>
Specifies the HTML attributes to “li” item list</td></tr>
<tr>
<td>
imageUrl</td><td>
Specifies the image URL to “img” tag inside item list. </td></tr>
</table>

##Local data

To define the local data to the **Menu** control, map the user-defined **JSON** data names with its appropriate dataSource column names.

Add the following code in your **HTML** page.

{% highlight html %}


<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <ul id="menu"></ul>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    // In JavaScript, you can initialize the Menu control.
    var data = [
        { id: 1, text: "Group A", parentId: null },
        { id: 2, text: "Group B", parentId: null },
        { id: 3, text: "Group C", parentId: null },
        { id: 4, text: "Group D", parentId: null },
        { id: 5, text: "Group E", parentId: null },
        //first level child
        { id: 11, parentId: 1, text: "Algeria" },
        { id: 12, parentId: 1, text: "Armenia" },
        { id: 13, parentId: 1, text: "Bangladesh" },
        { id: 14, parentId: 1, text: "Cuba" },
        { id: 15, parentId: 2, text: "Denmark" },
        { id: 16, parentId: 2, text: "Egypt" },
        { id: 17, parentId: 3, text: "Finland" },
        { id: 18, parentId: 3, text: "India" },
        { id: 19, parentId: 3, text: "Malaysia" },
        { id: 20, parentId: 4, text: "New Zealand" },
        { id: 21, parentId: 4, text: "Norway" },
        { id: 22, parentId: 4, text: "Poland" },
        { id: 23, parentId: 5, text: "Romania" },
        { id: 24, parentId: 5, text: "Singapore" },
        { id: 25, parentId: 5, text: "Thailand" },
        { id: 26, parentId: 5, text: "Ukraine" },
        //second level child
        { id: 111, parentId: 11, text: "First Place" },
        { id: 112, parentId: 12, text: "Second Place" },
        { id: 113, parentId: 13, text: "Third place" },
        { id: 114, parentId: 14, text: "Fourth Place" },
        { id: 115, parentId: 15, text: "First Place" },
        { id: 116, parentId: 16, text: "Second Place" },
        { id: 117, parentId: 17, text: "Third Place" },
        { id: 118, parentId: 18, text: "First Place" },
        { id: 119, parentId: 19, text: "Second Place" },
        { id: 120, parentId: 20, text: "First Place" },
        { id: 121, parentId: 21, text: "Second Place" },
        { id: 122, parentId: 22, text: "Third place" },
        { id: 123, parentId: 23, text: "Fourth Place" },
        { id: 120, parentId: 24, text: "First Place" },
        { id: 121, parentId: 25, text: "Second Place" },
        { id: 122, parentId: 26, text: "Third place" }
    ];
/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            fields: { dataSource: data, id: "id", parentId: "parentId", text: "text" }
        });
    });
}

{% endhighlight %}


The following screenshot displays the output of the above code.

![](Data-binding_images/Data-binding_img1.png) 


## Remote data

The **Menu** control also provides support for Remote data binding. Here the remote data is placed in Web service and you can render the menu items from the web service using Service **URL**. The data is in **JSON** format. 

DataManager is used to manage relational data in **JavaScript**. DataManager uses two different classes, **ej.DataManager** for processing, and **ej.Query** for serving data. **ej.DataManager** communicates with data source and **ej.Query** generates data queries that are to be read by DataManager. To know more about DataManager and Query refer the following link location.

<https://help.syncfusion.com/js/datamanager>

In the following example, [http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/) is used as the **URL**. This acts as web service that is located in the **Syncfusion** server. The web service with the name Northwind.svc is used here.

Add the following code in your **HTML** page.


{% highlight html %}


<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <ul id="shipDetails"></ul>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

   
    // Initialize the Menu control in JavaScript.
    $(function () {
        // DataManager creation
        var dataManger = ej.DataManager({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);
       var sample = new ej.Menu($("#shipDetails"),{
            fields: {
                dataSource: dataManger, query: query, id: "CategoryID", text: "CategoryName",
                child: { dataSource: dataManger, tableName: "Products", id: "ProductID", parentId: "CategoryID", text: "ProductName" }
            }
        });
    });


{% endhighlight %}

The following screenshot displays the output of the above code. 

![](Data-binding_images/Data-binding_img2.png) 