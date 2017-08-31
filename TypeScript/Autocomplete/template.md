---
layout: post
title: Template support in AutoComplete widget for Essential JS
description: Customizes the appearance of the suggestion list using a template
platform: TypeScript
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui,ej autocomplete
---

# Templates

The suggestion list can be customized based on different needs using templates. The desired templates can be defined using the “template” property.

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module AutocompleteComponent{
                var mobileList = [
                        { pName: "Galaxy Grand 2", quantity: "3" },
                { pName: "Galaxy S6", quantity: "5" },
                { pName: "IPhone S6", quantity: "8" },
                { pName: "Ipod Mini", quantity: "3" }, ];
        
            $(function () {   
                var autocompleteInstance =new ej.Autocomplete($("#autocomplete"), {  
                dataSource: mobileList,
                fields: { text: "pName" },
                template: "<div><div class='product-text'>${pName}</div> <span class='product-quantity' style='font-size:10px'> Quantity : ${quantity}</span></div>"
                });
        });
   }

        


{% endhighlight %}

![](template_images\template_img1.png)



