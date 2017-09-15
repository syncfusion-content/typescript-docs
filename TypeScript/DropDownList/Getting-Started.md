---
layout: post
title: Getting Started for DropDownList
description: Getting Started for DropDownList
platform: Typescript
control: DropDownList
documentation: ug
keywords: DropDownList, Populating data
---

# Getting Started

The external script dependencies of the DropDownList widget are,

* [jQuery 1.7.1](http://jquery.com/) and later versions.
* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing/) - to support the animation effects.

And the internal script dependencies of the DropDownList widget are:

<table>
	<tr>
		<th>File </th>
		<th>Description / Usage </th>
	</tr>
	<tr>
		<td>ej.core.min.js</td>
		<td>Must be referred always before using all the JS controls.</td>
	</tr>
	<tr>
		<td>ej.data.min.js</td>
		<td>Used to handle data operation and should be used while binding data to JS controls.</td>
	</tr>
	<tr>
		<td>ej.dropdownlist.min.js</td>
		<td>The dropdownlist’s main file</td>
	</tr>
	<tr>
		<td>ej.checkbox.min.js</td>
		<td>Should be referred when using checkbox functionalities in DropDownList.</td>
	</tr>
	<tr>
		<td>ej.scroller.min.js</td>
		<td>Should be referred when using scrolling in DropDownList.</td>
	</tr>
	<tr>
		<td>ej.draggable.min.js</td>
		<td>Should be referred when using popup resize functionality in DropDownList.</td>
	</tr>
</table>

For getting started you can use the ‘ej.web.all.min.js’ file, which encapsulates all the 'ej' controls and frameworks in one single file.<br/> 

For themes, you can use the ‘ej.web.all.min.css’ CDN link from the snippet given. To add the themes in your application, please refer [this link](http://help.syncfusion.com/js/theming-in-essential-javascript-components#adding-specific-theme-to-your-application).

## Creating DropDownList in Typescript

Create an **HTML** page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

      <!DOCTYPE html>
      <html>
      <head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
      </head>
      <body>
      </body>
      </html>

{% endhighlight %}

The DropDownList can be created from a HTML ‘input’ element with the HTML 'id' attribute and pre-defined options set to it. To create the DropDownList, you should call the 'ejDropDownList' jQuery plug-in function.

{% highlight html %}
	
	 <div class="control">
        <input type="text" id="dropdown1" />
    </div>
			
{% endhighlight %}
	
{% highlight html%}	
	
	  /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
     module DropDownListComponent {
       var items = [
        { text: "ListItem 1", value: "item 1" }, { text: "ListItem 2", value: "item 2" }, { text: "ListItem 3", value: "item 3"},
        { text: "ListItem 4", value: "item 4" }, { text: "ListItem 5", value: "item 5" }];
        $(function () {
        var sample = new ej.DropDownList($("#dropdown1"), {
            dataSource: items,
            fields: {text: "text", value: "value" }
        });
        
          });
       }

{% endhighlight %}

![](Getting-Started-images/Getting-Started_img1.jpeg)

## Populating data

The DropDownList can be bounded to both local array and remote data services .You can bind data to DropDownList through services or local data using  [dataSource](http://help.syncfusion.com/js/api/ejdropdownlist#members:datasource) property 
 
{% highlight html %}

     <div class="control">
        <input type="text" id="dropdown1" />
    </div>
	
{% endhighlight %}
	
{% highlight html%}	
	
	  /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
      module DropDownListComponent {
        $(function () {
         var customers = [
        { id: "1", text: "ALFKI" }, { id: "2", text: "ANATR" }, { id: "3", text: "ANTON" },
        { id: "4", text: "AROUT" }, { id: "5", text: "BERGS" }, { id: "6", text: "BLAUS" }
          ];

    var sample = new ej.DropDownList($("#dropdown1"), {
        dataSource: new ej.DataManager(customers),
        fields: { id: "id", text: "text", value: "text" }
    });
    
      }
{% endhighlight %}
	
![](Getting-Started-images/Getteing-Started_img2.jpeg)

## Setting Dimensions

DropDownList dimensions can be set using width and height API.
	
{% highlight html %}

     /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
	
	module DropDownListComponent {
    var items = [
        { text: "ListItem 1", value: "item 1" }, { text: "ListItem 2", value: "item 2" }, { text: "ListItem 3", value: "item 3"},
        { text: "ListItem 4", value: "item 4" }, { text: "ListItem 5", value: "item 5" }];

    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"), {
            dataSource: items,
            fields: { text: "text", value: "value" },
            width: "200px",
            height:"50px"
               });
        
          });
      }
{% endhighlight %}
	
**Setting dimensions to Popup list**

PopupWidth and popupHeight can be used to create a fixed size popup list.

{% highlight html %}

     /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
	module DropDownListComponent {
    var items = [
        { text: "ListItem 1", value: "item 1" }, { text: "ListItem 2", value: "item 2" }, { text: "ListItem 3", value: "item 3"},
        { text: "ListItem 4", value: "item 4" }, { text: "ListItem 5", value: "item 5" }];

    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"), {
            dataSource: items,
            fields: { text: "text", value: "value" },
            width: "200px",
            height: "50px",
            popupHeight: "100px",
            popupWidth:"200px"
               });
        
           });
      }

{% endhighlight %}
	
## Setting and Getting Value

You can select single or multiple values from DropDownList widget. To assign a value initially to the DropDownList, you can use [value](http://help.syncfusion.com/js/api/ejdropdownlist#members:value) property.

N> To select multiple items based on index, refer [here](functionalities#selection).


{% highlight html %}	

      /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
	
     module DropDownListComponent {
      var items = [
        { text: "ListItem 1", value: "item 1" }, { text: "ListItem 2", value: "item 2" }, { text: "ListItem 3", value: "item 3"},
        { text: "ListItem 4", value: "item 4" }, { text: "ListItem 5", value: "item 5" }];

      $(function () {
        var sample = new ej.DropDownList($("#dropdown1"), {
            dataSource: items,
            fields: { text: "text", value: "value" },
            value: "item 3",
            change: function ()
            {
                var obj = $('#dropdown1').data("ejDropDownList");

                console.log("Selected Item's Text - " + obj.option("text"));

                console.log("selected Item's Value - " + obj.option("value"));  
            }
         });
        
       });


     }

{% endhighlight %}

