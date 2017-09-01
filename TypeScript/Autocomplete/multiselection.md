---
layout: post
title: Multi Selection in AutoComplete widget
description: How to pick multiple values from the AutoComplete suggestion items.
platform: TypeScript
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui
---

# MultiSelection

The AutoComplete widget helps you to select multiple values from the suggestion list using the multiSelect property.

There are two types of multi-selection mode.

1. VisualMode – Selection values are displayed in separate box with close like button.

2. Delimiter – Selection values are separated using the delimiter character which can be specified using delimiterChar API. 

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module AutocompleteComponent{
        
                /* Local Data */
                var carList = [
                        "Audi S6", "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                        "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                        "Chevrolet Camaro", "Cadillac ",
                        "Duesenberg J ", "Dodge Sprinter",
                        "Elantra", "Excavator",
                        "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
                        "GAZ Siber"];
        
             var autocompleteInstance =new ej.Autocomplete($("#autocomplete"), {  
                   dataSource: carList,
                   width: 205,
                   multiSelectMode:ej.MultiSelectMode.VisualMode
         });
        
        </script>
        


{% endhighlight %}



![](multiselection_images\multiselection_img1.png)

