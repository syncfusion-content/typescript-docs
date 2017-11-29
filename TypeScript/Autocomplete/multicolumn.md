---
layout: post
title: Multiple columns in AutoComplete widget for Essential JS
description: How to assign multiple column values into the AutoComplete suggestion items.
platform: TypeScript
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui
---

# Multiple Columns

The Autocomplete adds support for selecting multiple columns in the dropdown list. This multiple column options can be enabled and customized through the [MultiColumnSettings](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings) property.
 
In AutoComplete Multiple Column search is based on [searchColumnIndices](https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-searchColumnIndices) property which allows user to search text for any number of fields in the suggestion list without modifying the selected text format.

In AutoComplete Multiple Column searched value is updated to autocomplete input box based on [stringFormat](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings-stringFormat) property which specifies column indices values to  updated.


<table><tr><th>Name</th><th>Description</th></tr>
<tr><td>multiColumnSettings.enable</td><td>Allow list of data to be displayed in several columns.</td></tr>
<tr><td>multiColumnSettings.showHeader</td><td>Allow header text to be displayed in corresponding columns.</td></tr>
<tr><td>multiColumnSettings.stringFormat</td><td>Specifies the format for displaying a selected value and columns to be searched.</td></tr>
<tr><td>multiColumnSettings.columns</td><td>Field and Header Text collections can be defined and customized through this field.</td></tr>
<tr><td>multiColumnSettings.columns.field</td><td>Field to be mapped from the dataSource to the columns in Autocomplete suggestion list.</td></tr>
<tr><td>multiColumnSettings.columns.headerText</td><td>Get or set a value that indicates to display the title of that particular column.</td></tr>
<tr><td>multiColumnSettings.columns.cssClass</td><td>Field to be mapped for to add user defined CSS class for the specific column.</td></tr>
<tr><td>multiColumnSettings.columns.type</td><td>Get or set the data type for a individual column.</td></tr>
<tr><td>multiColumnSettings.columns.filterType</td><td>Get or set the search filter type for the column.</td></tr>
<tr><td>multiColumnSettings.columns.headerTextAlign</td><td>Used to align or position the header value in the column.</td></tr>
<tr><td>multiColumnSettings.columns.textAlign</td><td>Used to align or position all the values in a column.</td></tr>
</table>


## Example 
{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
                /* Local Data */
                var carList = [
            { "EmployeeID": 1, "FirstName": "Nancy" ,"City": "Seattle" },
            { "EmployeeID": 10, "FirstName": "Laura",  "City": "Seattle" },
            { "EmployeeID": 11,  "FirstName": "Janet",  "City": "Kirkland" },
            { "EmployeeID": 12,  "FirstName": "Michael", "City": "London" },
            { "EmployeeID": 13,  "FirstName": "Steven",  "City": "London"},
            { "EmployeeID": 14,  "FirstName": "Andrew","City": "Tacoma" },
            { "EmployeeID": 15,  "FirstName": "Robert", "City": "London" },
            { "EmployeeID": 16,  "FirstName": "Margaret",  "City": "Redmond" },
            { "EmployeeID": 17,  "FirstName": "Steven",  "City": "London" },
            { "EmployeeID": 18,  "FirstName": "Michael",  "City": "London" },
            { "EmployeeID": 19,  "FirstName": "Robert",  "City": "London"}, ];
        
                var autocompleteInstance =new ej.Autocomplete($("#selectCar"), {       
                    dataSource: carList, 
                    width: 400, 
                    multiColumnSettings:{
                        enable:true,
                        showHeader:true,
                        stringFormat:"{1}",
						searchColumnIndices[0,1,2],
                        columns:[
							{"field": "EmployeeID" , "headerText":"EmployeeID"},
							{"field": "FirstName" , "headerText":"FirstName"},
							{"field": "City" , "headerText":"City"}
						]                        
                    }
             });
        
        


{% endhighlight %}

N> Here [stringFormat](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings-stringFormat) is “{0} ({1}) ({2})” so the search will be based on column indices 0, 1 and 2.


![](multicolumn_images\multicolumn_img1.png)
