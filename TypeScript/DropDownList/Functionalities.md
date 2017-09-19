---
layout: post
title: Functionalities in the DropDownList widget
description: Functionalities in the DropDownList widget
platform: Typescript
control: DropDownList
documentation: ug
keywords: DropDownList, dropdown, Selection, Grouping, Sorting
---
# Functionalities

## Selection

By default only one item can be selected from the popup list. For multiple selection, you have to enable [checkboxes](Checkbox). The selected item consist of active class (“e-active”) to differentiate it from other items.

The following API’s, select the items in the DropDownList via text or value or indices.

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
            {{'[value](https://help.syncfusion.com/api/js/ejdropdownlist#members:value)'| markdownify }} 
            <br/>
        </td>
        <td>
            To select an item initially, you can pass the item’s value via value property.
            <br/>
            Multiple items can select via value property, the given values should be separated by delimiter character.
        </td>
    </tr>
    <tr>
        <td>
            {{'[text](https://help.syncfusion.com/api/js/ejdropdownlist#members:text)'| markdownify }} 
            <br/>
        </td>
        <td>
            To select an item initially, you can pass the item’s text via text property.
            <br/>
            Multiple items can select via text property, the given values should be separated by delimiter character.
        </td>
    </tr>
    <tr>
        <td>
            {{'[selectedIndex](https://help.syncfusion.com/api/js/ejdropdownlist#members:selectedindex)'| markdownify }} 
            <br/>
        </td>
        <td>
            Select a single item by passing an index value to the selectedIndex property.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
             {{'[selectedIndices](https://help.syncfusion.com/api/js/ejdropdownlist#members:selectedindices)'| markdownify }}
            <br/>
        </td>
        <td>
            Select more than one items by passing index values to the selectedIndices property when multi selection enabled. 
            <br/>
        </td>
    </tr>
</table>

N> Index starts from 0 here.
N> To use “selectedIndices” property, you should enable with showCheckbox or multiSelectMode property.

The following methods, select the items in the DropDownList.

<table>
    <tr>
        <th>
            Methods
            <br/>
        </th>
        <th>
            Description
            <br/>
        </th>
    </tr>
    <tr>
        <td>
            {{'[selectItemByIndices](https://help.syncfusion.com/api/js/ejdropdownlist#methods:selectitembyindices)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to select the list of items in the DropDownList through the Index of the items.
        </td>
    </tr>
    <tr>
        <td>
            {{'[selectItemByText](https://help.syncfusion.com/api/js/ejdropdownlist#methods:selectItemByText)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to select an item in the DropDownList by using the given text value.
        </td>
    </tr>
    <tr>
        <td>
            {{'[selectItemByValue](https://help.syncfusion.com/api/js/ejdropdownlist#methods:selectitembyvalue)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to select an item in the DropDownList by using the given value.
            <br/>
        </td>
    </tr>
</table>

The following methods, used to retrieve the items from the DropDownList.

<table>
    <tr>
        <th>
            Methods
            <br/>
        </th>
        <th>
            Description
            <br/>
        </th>
    </tr>
    <tr>
        <td>
            {{'[getListData](https://help.syncfusion.com/api/js/ejdropdownlist#methods:getlistdata)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to retrieve the items that are bound with the DropDownList.
        </td>
    </tr>
    <tr>
        <td>
            {{'[getSelectedItem](https://help.syncfusion.com/api/js/ejdropdownlist#methods:getselecteditem)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to get the selected items in the DropDownList.
        </td>
    </tr>
    <tr>
        <td>
            {{'[getSelectedValue](https://help.syncfusion.com/api/js/ejdropdownlist#methods:getSelectedValue)'| markdownify }}
            <br/>
        </td>
        <td>
            This method is used to retrieve the items value that are selected in the DropDownList.
            <br/>
        </td>
    </tr>
</table>

I> When multiSelectMode is enabled in a DropDownList and selected items having same text but its value is different means, the items can be selected. Please refer the online [link](http://jsplayground.syncfusion.com/Sync_5fgywhmb)

### Using value or text

To select an item initially you can pass the item’s value via [value](https://help.syncfusion.com/api/js/ejdropdownlist#members:value) property or [selectItemByValue](https://help.syncfusion.com/api/js/ejdropdownlist#members:selectitembyvalue) method. To achieve this DropDownList widget must be initiated with the associate value. 

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
$(function() {         
    var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            value: "item3"
        });
    });
}

{% endhighlight %}

![](Functionalities_images/Functionalities_img1.jpeg)

N> To retrieve the selected item’s LI elements and value you can use [getSelectedItem](https://help.syncfusion.com/api/js/ejdropdownlist#methods:getselecteditem), [getSelectedValue](https://help.syncfusion.com/api/js/ejdropdownlist#methods:getselectedvalue) methods respectively.

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
      $(function() {      
        var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            selectedIndex: 0
        });
        var obj = $('#dropdown1').data("ejDropDownList");
        //the below given code will return the li element of the selected item
        console.log(obj.getSelectedItem());
        //the below given code will return the JSON object of the selected item
        console.log(JSON.parse(obj.getSelectedValue()));
    });
}
	
{% endhighlight %}

### Using indices

You can select a single or more than one item by passing index values to the properties [selectedIndex](https://help.syncfusion.com/api/js/ejdropdownlist#members:selectedindex) or [selectedIndices](https://help.syncfusion.com/api/js/ejdropdownlist#members:selectedindices) respectively. Index starts from 0 here.

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
     $(function() {       
       var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            selectedIndex: 1
        });
    });
  }  

{% endhighlight %}

![](Functionalities_images/Functionalities_img2.jpeg)

I> To use "selectedIndices" property, you should enable either showCheckbox or multiSelectMode property First.

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
     $(function() {       
       var sample = new ej.DropDownList($("#dropdown1"),{
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            showCheckbox: true,
            selectedIndices: [1, 2]
        });
		
    });
}
{% endhighlight %}

### Unselect items

Similarly, you can unselect a single or multiple items by using [unselectItemByValue](https://help.syncfusion.com/api/js/ejdropdownlist#methods:unselectitembyvalue) or [unselectItemByIndices](https://help.syncfusion.com/api/js/ejdropdownlist#methods:unselectitembyindices) or [unselectItemByText](https://help.syncfusion.com/api/js/ejdropdownlist#methods:unselectitembytext) methods. This will remove the selection state of the corresponding data item from the popup list and textbox. 

{% highlight html %}

            <input type="text" id="dropdown1" />

            <input type="button" value="Unselect" onclick="unselect()" />

     
{% endhighlight %}

{% highlight javascript %}

    var obj;

    $(function() {
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
      $('#dropdown1').ejDropDownList({
          width: 300,
          dataSource: items,
          fields: {
              text: "text",
              value: "value"
          },
          showCheckbox: true,
          selectedIndices: [1, 2, 3]
      });
      obj = $('#dropdown1').data("ejDropDownList");
      console.log("Selected Item's Text - " + obj.option("text"));
      console.log("selected Item's Value - " + obj.option("value"));
    });

    function unselect() {
      obj.unselectItemByValue("item2");
      obj.unselectItemByIndices(2);
      obj.unselectItemByText("ListItem 4");
    }			
{% endhighlight %}

## Grouping

The DropDownList items can be categorized by using a specific field in the popup list. This is enabled by using [groupBy](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-groupby) field on data source binding. By default grouping is disabled in DropDownList.
The below given example explains the behavior of grouping with JSON array binding.

{% highlight html %}

            <input type="text" id="dropdown1" />

                
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
	    var skills = [{
	        skill: "Cabbage",
	        category: "Leafy and Salad"
	    }, {
	        skill: "Pea",
	        category: "Leafy and Salad"
	    }, {
	        skill: "Spinach",
	        category: "Leafy and Salad"
	    }, {
	        skill: "Wheat grass",
	        category: "Leafy and Salad"
	    }, {
	        skill: "Yarrow",
	        category: "Leafy and Salad"
	    }, {
	        skill: "Chickpea",
	        category: "Beans"
	    }, {
	        skill: "Green bean",
	        category: "Beans"
	    }, {
	        skill: "Horse gram",
	        category: "Beans"
	    }, {
	        skill: "Peanut",
	        category: "Beans"
	    }, {
	        skill: "Pigeon pea",
	        category: "Beans"
	    }, {
	        skill: "Garlic",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Garlic Chives",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Lotus root",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Nopal",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Onion",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Shallot",
	        category: "Bulb and Stem"
	    }, {
	        skill: "Beetroot",
	        category: "Root and Tuberous"
	    }, {
	        skill: "Carrot",
	        category: "Root and Tuberous"
	    }, {
	        skill: "Ginger",
	        category: "Root and Tuberous"
	    }, {
	        skill: "Potato",
	        category: "Root and Tuberous"
	    }, {
	        skill: "Radish",
	        category: "Root and Tuberous"
	    }, {
	        skill: "Turmeric",
	        category: "Root and Tuberous"
	    }];
    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"),{
	        width: 150,
	        popupHeight: 300,
	        watermarkText: "Select a vegetable",
	        dataSource: skills,
	        fields: {
	            text: "skill",
	            groupBy: "category"
	        }
	    });
	});
}
{% endhighlight %}

![](Functionalities_images/Functionalities_img3.jpeg)

N> Grouping has restrictions in the following scenarios,<BR>
1.  It is not supported on using HTML "select" element with predefined set of options<BR>
2.  When using UL-LI elements you need to use “e-category” class in LI element to specify it as the grouping header. The following code will explain this behavior,<BR>
3.  The sorting behavior varies when grouping is enabled in the DropDownList, based on browser as we have used browser based stable sorting method when there is multiple level of sorting. <BR>
4.  To overcome this behavior on sorting order with browser, we suggest you to set ej.support.stableSort as false from the script when the page is loaded or in document ready function.
  
   {% highlight javascript %}
   

            $(document).ready(function () {
                ej.support.stableSort = false;            
            });
    
   {% endhighlight %}

{% highlight html %}

            <input type="text" id="dropdown1" />
                
{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
	$(function() {
	    var sample = new ej.DropDownList($("#dropdown1"),{
	        targetID: "dropDownItems"
	    });
	}); 
}          
    
{% endhighlight %}

![](Functionalities_images/Functionalities_img4.jpeg)

I> Virtual scrolling is not supported with Grouping.

## Sorting

Sorting is enabled to order to display the items alphabetically in either ascending or descending order. By default the items is displayed in the initialized order, use [enableSorting](https://help.syncfusion.com/api/js/ejdropdownlist#members:enablesorting) property to automatically sort strings based on text field value. You can assign either “ascending” or “descending” string values to the [sortOrder](https://help.syncfusion.com/api/js/ejdropdownlist#members:sortorder) property to sort out the list items. By default ascending order is followed when "sortOrder" property is not specified. 

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
	        text: "ListItem 5",
	        value: "item5"
	    }, {
	        text: "ListItem 4",
	        value: "item4"
	    }, {
	        text: "ListItem 2",
	        value: "item2"
	    }, {
	        text: "ListItem 3",
	        value: "item3"
	    }, ];
     $(function() {   
	    var sample = new ej.DropDownList($("#dropdown1"),{
	        dataSource: items,
	        fields: {
	            text: "text",
	            value: "value"
	        },
	        enableSorting: true,
	        sortOrder: "ascending"
	    });
	});             
}
{% endhighlight %}

I> Virtual scrolling is not supported with Sorting.

## Cascading

This works for series of DropDownList in which items are filtered based on the previous DropDownList‘s selection. Cascading is performed based on the value field and this field should be bounded with a foreign key. To perform cascading, specify the child DropDownList’s id in [cascadeTo](https://help.syncfusion.com/api/js/ejdropdownlist#members:cascadeto) property and use delimiter (“,”) to specify more than one child DropDownList.

Configuring the data items for cascading to the series of DropDownList is demonstrated below

{% highlight html %}

    <div style="width: 400px;">
    	<div style="float: left;">
        	<span>Select Group</span>
        	<input id="groups" type="text" />
    	</div>

    	<div style="float: right;">
        	<span>Select Country</span>
        	<input id="countries" type="text" />
    	</div>
	</div>
                
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
        //first dropdown
        var groups = [{
            parentId: 'a',
            text: "Group A"
        }, {
            parentId: 'b',
            text: "Group B"
        }, {
            parentId: 'c',
            text: "Group C"
        }, {
            parentId: 'd',
            text: "Group D"
        }, {
            parentId: 'e',
            text: "Group E"
        }];
        //second dropdown
        var countries = [{
            value: 11,
            parentId: 'a',
            text: "Algeria"
        }, {
            value: 12,
            parentId: 'a',
            text: "Armenia"
        }, {
            value: 13,
            parentId: 'a',
            text: "Bangladesh"
        }, {
            value: 14,
            parentId: 'a',
            text: "Cuba"
        }, {
            value: 15,
            parentId: 'b',
            text: "Denmark"
        }, {
            value: 16,
            parentId: 'b',
            text: "Egypt"
        }, {
            value: 17,
            parentId: 'c',
            text: "Finland"
        }, {
            value: 18,
            parentId: 'c',
            text: "India"
        }, {
            value: 19,
            parentId: 'c',
            text: "Malaysia"
        }, {
            value: 20,
            parentId: 'd',
            text: "New Zealand"
        }, {
            value: 21,
            parentId: 'd',
            text: "Norway"
        }, {
            value: 22,
            parentId: 'd',
            text: "Poland"
        }, {
            value: 23,
            parentId: 'e',
            text: "Romania"
        }, {
            value: 24,
            parentId: 'e',
            text: "Singapore"
        }, {
            value: 25,
            parentId: 'e',
            text: "Thailand"
        }, {
            value: 26,
            parentId: 'e',
            text: "Ukraine"
        }];
     $(function() {   
	    var sample = new ej.DropDownList($("#groups"),{
            dataSource: groups,
            fields: {
                text: "text",
                value: "parentId"
            },
            cascadeTo: 'countries'
        });
        var sample = new ej.DropDownList($("#countries"),{
            dataSource: countries,
            enabled: false
        });
    });
}
{% endhighlight %}

![](Functionalities_images/Functionalities_img5.jpeg)

![](Functionalities_images/Functionalities_img6.jpeg)

### Binding the data source to the cascading DropDownList using cascade event

Bind the data source to the cascading DropDownList dynamically using [cascade](https://help.syncfusion.com/api/js/ejdropdownlist#events:cascade) event as demonstrated below,

{% highlight html %}

    <div style="width: 530px;">
    <div style="float: left;">
        <span>Select Group</span>
        <input id="groups" type="text" />
    </div>

    <div style="float: left; padding-left: 50px;">
        <span>Select Country</span>
        <input id="countries" type="text" />
    </div>

    <div style="float: right;">
        <span>Select Players</span>
        <input id="players" type="text" />
    </div>
	</div>
                
{% endhighlight %}

{% highlight javascript %}
  
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
        //first dropdown
        var groups = [{
            parentId: 'a',
            text: "Group A"
        }, {
            parentId: 'b',
            text: "Group B"
        }];
      var sample = new ej.DropDownList($("#groups"),{
            dataSource: groups,
            fields: {
                text: "text",
                value: "parentId"
            },
            cascadeTo: "countries,players",
            cascade: 'onChange'
        });
    var sample1 = new ej.DropDownList($("#countries"),{
            enabled: false
        });
    var sample2 = new ej.DropDownList($("#players"),{
            enabled: false
        });
    });

    function onChange(args) {
        var countries = [{
            parentId: 'a',
            text: "Algeria"
        }, {
            parentId: 'a',
            text: "Armenia"
        }, {
            parentId: 'a',
            text: "Bangladesh"
        }, {
            parentId: 'a',
            text: "Cuba"
        }, {
            parentId: 'b',
            text: "Denmark"
        }, {
            parentId: 'b',
            text: "Egypt"
        }];

        var players = [{
            parentId: 'a',
            text: "Adams"
        }, {
            parentId: 'a',
            text: "Clarke"
        }, {
            parentId: 'b',
            text: "Brett"
        }, {
            parentId: 'b',
            text: "James"
        }];

        sample1.option({
            "dataSource": countries,
            "enabled": true
        });
        sample2.option({
            "dataSource": players,
            "enabled": true
        });
    }
		
{% endhighlight %}

![](Functionalities_images/Functionalities_img7.jpeg)

### Multi-Level Cascading

The below scenario can be explained with three DropDownList for the multi-level cascading

{% highlight html %}

    <div class="frame">
        <div class="control" style="float: left; padding:10px;">
            <span class="txt">Select Continent</span>
            <input id="groups" type="text" />
        </div>
        <div class="control" style="float: left; padding:10px;">
            <span class="txt">Select Country</span>
            <input id="countries" type="text" />
        </div>
        <div class="control" style="float: left; padding:10px;">
            <span class="txt">Select State</span>
            <input id="capitalList" type="text" />
        </div>
    </div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {   
           // declaration
           var groups = [
           { parentId: 'a', text: "Africa" },
           { parentId: 'b', text: "Asia" },
           { parentId: 'c', text: "Europe" },
           { parentId: 'd', text: "North America" },
           { parentId: 'e', text: "South America" },
           { parentId: 'f', text: "Oceania" },
           { parentId: 'g', text: "Antarctica" }]
           //Countries List
           var countries = [
           { value: 11, parentId: 'a', text: "Algeria" },
           { value: 12, parentId: 'a', text: "Egypt" },
           { value: 13, parentId: 'b', text: "Armenia" },
           { value: 14, parentId: 'b', text: "Bangladesh" },
           { value: 15, parentId: 'b', text: "India" },
           { value: 16, parentId: 'c', text: "Denmark" },
           { value: 17, parentId: 'c', text: "Finland" },
           { value: 18, parentId: 'd', text: "Cuba" },
           { value: 19, parentId: 'd', text: "USA" },
           { value: 20, parentId: 'e', text: "Brazil" },
           { value: 21, parentId: 'e', text: "Peru" },
           { value: 22, parentId: 'f', text: "Australia" },
           { value: 23, parentId: 'f', text: "New Zealand" },
           { value: 24, parentId: 'g', text: "French Southern" },
           { value: 25, parentId: 'g', text: "South Georgia" }]
           //Capital List
           var capital = [
           { value: 11, text: "Algiers" },
           { value: 12, text: "Cairo" },
           { value: 13, text: "Yerevan" },
           { value: 14, text: "Dhaka" },
           { value: 15, text: "New Delhi" },
           { value: 16, text: "Copenhagen" },
           { value: 17, text: "Helsinki" },
           { value: 18, text: "Havana" },
           { value: 19, text: "Washington, D.C." },
           { value: 20, text: "Brasilia" },
           { value: 21, text: "Lima" },
           { value: 22, text: "Canberra" },
           { value: 23, text: "Wellington" },
           { value: 24, text: "Alfred Faure" },
           { value: 25, text: "King Edward Point" }]

  $(function() {   
      var sample1 = new ej.DropDownList($("#groups"),{         
               dataSource: groups,
               fields: { value: "parentId" },
               cascadeTo: 'countries'
           });
      var sample2 = new ej.DropDownList($("#countries"),{      
               dataSource: countries,
               fields: { value: "value" },
               cascadeTo: 'capitalList',
               enabled: false
           });
        var sample3 = new ej.DropDownList($("#capitalList"),{       
               dataSource: capital,
               fields: { value: "value" },
               enabled: false
           });
       });
}
    
{% endhighlight %}

First two DropDownList cascaded based on the parentId, and then from second to third, cascading performed based on the value field.

![](Functionalities_images/multipCascade.png)

## Search

Items are searched based on the keyed in values to the textbox. There are two types of searches,

* Incremental Search
* Filter Search

### Incremental Search

Selects the item in the popup list based on the keyed in value. If the time taken to type exceeds 1000 milliseconds then filtered items will be reset based on the current input value. By default this mode of search is enabled. Incremental search can be case sensitive or case insensitive. To make case sensitive, you can use [caseSensitiveSearch](https://help.syncfusion.com/api/js/ejdropdownlist#members:casesensitivesearch) property.

{% highlight html %}

    <input type="text" id="dropdown1" />
                
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
    $(function() {     
       var sample = new ej.DropDownList($("#dropdown1"),{ 
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            enableIncrementalSearch: true,
            caseSensitiveSearch: true
        });
    });
  }  
	
{% endhighlight %}

![](Functionalities_images/Functionalities_img8.jpeg)

### Filter search

You can quickly locate specific item within a large data source by filtering matches with a search box. A text box appears in the popup list for searching when [enableFilterSearch](https://help.syncfusion.com/api/js/ejdropdownlist#members:enablefiltersearch) property is enabled. By default, filtering returns the matched items list based on text in search textbox. 
You can configure the search filter by using [filterType](https://help.syncfusion.com/api/js/ejdropdownlist#members:filtertype) property. There is two types of filter options,

* Starts With 
* Contains

N> Items are filtered based on “contains” filter type by default.

{% highlight html %}

    <input type="text" id="dropdown1" />
                
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
    $(function() {     
        var sample = new ej.DropDownList($("#dropdown1"),{ 
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            enableFilterSearch: true,
            filterType: "startsWith"
        });
    });
}   
{% endhighlight %}

![](Functionalities_images/Functionalities_img9.jpeg)


