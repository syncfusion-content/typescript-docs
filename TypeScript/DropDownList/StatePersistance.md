---
layout: post
title: State Persistance with DropDownList widget 
description: State Persistence support to DropDownList widget
platform: Typescript
control: DropDownList
documentation: ug
keywords: Persistence, DropDownList, dropdown, State Persistence
---

# State Persistence

DropDownList stores its model is local storage by defining the property [enablePersistence](https://help.syncfusion.com/api/js/ejdropdownlist#members:enablepersistence).
You can sustain the below given functionalities in DropDownList by enabling persistence property,

* selected items value in the textbox 
* item’s selection state in the popup list 

Widget model will be stored in local storage / cookies of browser before page refreshes and reinitialized with the restored model after refresh.
The following properties are not included while maintaining DropDownList’s state in local storage to keep localStorage compact.

* Fields
* Data source
* Query 

{% highlight html %}

    <form id="form1">

        <input type="text" id="dropdown1" />

        <input type="submit" value="Post" />

    </form>
     
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
	    var items = [{
	        text: "Adams",
	        value: "emp1"
	    }, {
	        text: "James",
	        value: "emp2"
	    }, {
	        text: "Maria",
	        value: "emp3"
	    }, {
	        text: "Jessica",
	        value: "emp4"
	    }, {
	        text: "Jenneth",
	        value: "emp5"
	    }];

    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"),{
	        dataSource: items,
	        fields: {
	            text: "text",
	            value: "value"
	        },
	        enablePersistence: true
	    });
	});      		
}
{% endhighlight %}

## Accessing currently stored state

Persisted state can be accessed through local storage using corresponding key name. Key name formation would be in below order. It is combination of plugin name and control id.

{% highlight javascript %}

	// DropDownList state as string
	var dropdownlistStateString = window.localStorage.ejDropDownListdropdown;

	//DropDownList state as object
	var dropdownlistStateObject = JSON.parse(window.localStorage.ejDropDownListdropdown);

{% endhighlight %}

N> In the above example, ‘ejDropDownList’ is plugin name and ‘dropdown’ is control id.           
