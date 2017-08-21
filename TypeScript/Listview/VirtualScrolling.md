---
layout: post
title: Virtual Scrolling
description: virtual scrolling
platform: Typescript
control: ListView
documentation: ug
---

# Virtual Scrolling

We can load large data on demand using [allowVirtualScrolling](https://help.syncfusion.com/api/js/ejlistview#members:allowvirtualscrolling) property. By default, "allowVirtualScrolling" set as boolean value of **"false"**. When it is set true, list items will be loaded on every scroll action. The number of items to be loaded per request can be specified using the [itemRequestCount](https://help.syncfusion.com/api/js/ejlistview#members:itemrequestcount)  property. By default “itemRequestCount” value will be 5. We have provided two type of option for virtualScrolling,
 
 ## Normal Mode 
 This mode allows you to load the list view data while scrolling i.e. each time the scroll bar is scrolled, it will send request to the server to load the data.
 
 ## Continuous Mode  
 This mode allows you to load the list view data when the scrollbar reaches the end point. In this mode, we can specify the number of items to be loaded per request.

Refer the following code example.

{% highlight html %}

    <div class="cols-sample-area">               
                    <div class="ctrllabel">Select a customer</div>
                      <div id="defaultlistbox">              
                      </div>
            </div>

  {% endhighlight %}

Add the following script in your code.
    
    {% highlight javascript %}

        var dataManger = ej.DataManager({
                url: "http://js.syncfusion.com/ejservices/Wcf/Northwind.svc/", crossDomain: true
            });
            // Query creation
            var query = ej.Query()
                   .from("Customers");
    $(function () {
        var sample = new ej.ListView($("#defaultlistview"), {
			dataSource: dataManger, 
			query: query,
			fieldSettings: { text: "CustomerID" },
			height:300,
            itemRequestCount:8,
			allowVirtualScrolling: true, 
			virtualScrollMode: ej.VirtualScrollMode.Continuous		
			});
    });

    {% endhighlight %}
