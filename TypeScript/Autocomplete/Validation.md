---
layout: post
title: Validation in AutoComplete widget
description: How to use jQuery validation for the AutoComplete.
platform: TypeScript
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, ej autocomplete
---

## Validation

You can validate the Autocomplete value on form submission by applying “validationRules” and “validationMessage” to the Autocomplete. 

N> [jquery.validate.min](http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js) script file should be referred for validation, for more details, refer [here](http://jqueryvalidation.org/documentation).

### Validation Rules

The validation rules help you to verify the selected text by adding validation attributes to the input element. This can be set by using [validationRules](https://help.syncfusion.com/api/js/ejautocomplete#members:validationrules) property.

### Validation Messages 

You can set your own custom error message by using [validationMessage](https://help.syncfusion.com/api/js/ejautocomplete#members:validationmessage) property. To display the error message, specify the corresponding annotation attribute followed by the message to display.

N> jQuery predefined error messages to that annotation attribute will be shown when this property is not defined. The below given example explain this behavior of ‘required’ attribute,

When you initialize the Autocomplete widget, it creates an input hidden element which is used to store the selected items value. Hence, the validation is performed based on the value stored in this hidden element.

Required field and min value validation is demonstrated in the below given example.

{% highlight html %}

    <form id="form1">
    	<input type="text" id="autocomplete1" />
   
    	<input type="submit" value="Validate" />
	</form>
                
{% endhighlight %}

{% highlight javascript %}
	
    $.validator.setDefaults({
        ignore: [],
        errorClass: 'e-validation-error', // to get the error message on jQuery validation
        errorPlacement: function (error, element) {
            $(error).insertAfter(element.closest(".e-widget"));
        }
        // any other default options and/or rules
    });
    //If necessary, we can create custom rules as below. here method defined for min
    $.validator.addMethod("min",
        function (value, element, params) {
            if (!/Invalid|NaN/.test(value)) {
                return parseInt(value) > params;
            }
        }, 'Must be greater than 30.');
    $(function() {
        var items = [{
            text: "10",
            value: 10
        }, {
            text: "20",
            value: 20
        }, {
            text: "30",
            value: 30
        }, {
            text: "40",
            value: 40
        }, {
            text: "50",
            value: 50
        }];
          var autocompleteInstance =new ej.Autocomplete($("#autocomplete1"), {    
            dataSource: items,
            fields: {
                text: "text"
            },
            validationRules: {
                required: true,
                min: 30
            },
            validationMessage: {
                required: "* Required",
                min: "Select > 30"
            }
        });
    });
	
{% endhighlight %}

![](Validation_images\validation_img1.png)

