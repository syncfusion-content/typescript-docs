---
layout: post
title: Databinding in AutoComplete widget for Essential JS
description: How to populate data for the suggestion list.
platform: TypeScript
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui
---

# Data Binding

In order to render the Autocomplete widget, the data needs to be bound to it in a proper way. The below sections explain about binding local or remote data to the Autocomplete widget.

## Fields

The Autocomplete widget has a field property (object) which holds the properties to map with dataSource fields. Whenever we bind a data to Autocomplete, corresponding fields must be mapped using this property.

The field object contains the following properties.

<table>
<tr>
<th>Fields property</th>
<th>Description</th>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-text">text</a> </td>
<td>Maps the display text in the suggestion list </td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-key">key</a> </td>
<td>Maps to the unique key field in the data source</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-groupBy">groupBy</a> </td>
<td>Allows to enable grouping based on the assigned field</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-htmlAttributes">htmlAttributes</a> </td>
<td>Maps to set the HTML attribute for the list items</td>
</tr>
</table>


### Local data

The local data must be an array of JSON objects which is assigned for the Autocomplete widget dataSource property. 

In the below example name and index fields are mapped with text and key properties of the field object respectively.

{% highlight html %}

        <input type="text" id="autocomplete" />

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

 module AutocompleteComponent {       
         var countriesField = [
                { name: "Austria", index: "C1" },
                { name: "Australia", index: "C2" }, { name: "Antarctica", index: "C3" },
                { name: "Bangladesh", index: "C4" }, { name: "Belgium", index: "C5" },
                { name: "Brazil", index: "C6" },
                { name: "Canada", index: "C7" }, { name: "China", index: "C8" },
                { name: "Cuba", index: "C9" },
                { name: "Denmark", index: "C10" }, { name: "Dominica", index: "C11" },
                { name: "Europe", index: "C12" }, { name: "Egypt", index: "C13" },
                { name: "England", index: "C14" },
                { name: "India", index: "C15" }, { name: "Indonesia", index: "C16" }
                ];
        
    $(function () {        
        var autocompleteInstance =new ej.Autocomplete($("#autocomplete"), { 
                         dataSource: countriesField,
                          fields: { key: "index", text: "name" }, 
                          width: 205
         });
    });
 }   
        
{% endhighlight %}

![](local-data_images\local-data_img1.png)



### Remote data

#### OData

[OData](https://help.syncfusion.com/js/datamanager/data-binding) is a standardized protocol for creating and consuming the data. You can retrieve data from OData service by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started) and the queries can be added using [ej.Query()](https://help.syncfusion.com/js/datamanager/query).

Here ContactName and SupplierID fields are mapped with text and key properties respective to the field object.

{% highlight html %}

        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Create DataManager */
                var dataManger = ej.DataManager({
                /* OData service */
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });
                /* Create Query */
                var query = ej.Query().from("Suppliers").select("SupplierID", "ContactName");
        
                  var autocompleteInstance =new ej.Autocomplete($("#autocomplete"), {     
                        dataSource: dataManger, 
                        query: query,
                        fields: { text: "ContactName", key: "SupplierID" }, 
                        width: 205 
                });
        
        </script>

{% endhighlight %}

![](odata_images\odata_img1.png)



