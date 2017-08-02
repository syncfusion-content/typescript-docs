---
layout: post
title: Validation
description: Validate the date using jQuery
platform: TypeScript
control: DatePicker
documentation: ug
---
# Validation

DatePicker is a form control and therefore its value to be validated before processing. Client side validation provides a better user experience by responding quickly at browser level. Most common client side validation plugin is [jQuery Validation](http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js). 

DatePicker supports this validation by built-in, so you can do client validation with simple steps to validate and respond validation message. The jQuery validate plugin rules and custom methods can be used in the DatePicker control with the help of two properties,[validationRules](https://help.syncfusion.com/api/js/ejdatepicker#members:validationrules) and [validationMessage](https://help.syncfusion.com/api/js/ejdatepicker#members:validationmessage). 

Before using those properties, you need to add the jQuery validate plugin to your HTML page.

Refer the below jQuery validation plugin script after jQuery script reference.

{% highlight html %}

     <script src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>

{% endhighlight %}

{% highlight html %}

    <!--form to submit-->

    <form>

        <!--input element to create DatePicker-->

        <input id="datePicker" />

        <!-- submit button -->

        <input type="submit" value="submit" />

    </form>


{% endhighlight %}

jQuery validation library contains some default settings for validating the form. By default, it ignores hidden elements in from validation. If validation gets fail, in-built “error” class will be added to corresponding element. Here you can specify a custom class with your own style using “errorClass” API and you can place the error message in necessary position using “errorPlacement” API. Refer following code block to customize the default jQuery validation settings.

   {% highlight javascript %}
       
      $.validator.setDefaults({
           //if we don’t set custom class, default “error” class will be added
           errorClass: 'e-validation-error',
           //it specifies the error message display position
           errorPlacement: function (error, element) {
               $(error).insertAfter(element.closest(".e-widget"));
           }
       });

   {% endhighlight %}


{% highlight javascript %}
/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                validationRules: { required: true },// sets the field to be required

                validationMessage: { required: "Required Date value" } // sets validation message

            });

        });
}

{% endhighlight %}

N>  jQuery validation works only within the form element.

