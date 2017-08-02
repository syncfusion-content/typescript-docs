---
layout: post
title: Behaviour Settings
description: Configure DatePicker Behaviour settings
platform: TypeScript
control: DatePicker
documentation: ug
---
# Behavior Settings

DatePicker has some default behavior settings which helps you to perform more operation by Built-in.

## Selected Date

DatePicker value can be selected through picking date from DatePicker calendar or you can set it by using [value](https://help.syncfusion.com/api/js/ejdatepicker#members:value) property.

{% highlight javascript %}
  
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
    $(function () {
        var dateSample = new ej.DatePicker($("#datepicker"), {

            value: new Date(), // sets the current date

            change: "onChange" // sets handler to listen value change

        });
    });
}

    function onChange(args) {

        //args contains entire model of DatePicker to get the value of all properties.

        //alert DatePicker shows the previous date and selected date.

        alert(" previous date is : " + args.prevDate + " \n selected date is : " + args.value);

    }    

{% endhighlight %}

DatePicker allows only the valid date to be entered and it should be within the specified range. By default, strict mode is enabled in DatePicker, so it will restrict invalid date and resets to previous date if it’s not valid. To know more about strict mode refer [Strict Mode](#strict-mode).

## Date Range

DatePicker provides an option to restrict the user to pick the date from specified range of value. You can utilize this option by make use of [minDate](https://help.syncfusion.com/api/js/ejdatepicker#members:mindate) and [maxDate](https://help.syncfusion.com/api/js/ejdatepicker#members:maxdate) property.

**minDate** - specifies the minimum date to be picked in DatePicker calendar by disabling below date of minDate.

**maxDate** -  specifies the maximum date to be picked in DatePicker calendar by disabling above date of maxDate. 

{% highlight javascript %}
     
	   $(function () {

            // creates DatePicker from input with current date value
 
            var dateSample = new ej.DatePicker($("#datepicker"), {

                value: new Date(), // sets the current date

                minDate: new Date("2014/06/03"), // sets min date to be pick able in DatePicker calendar

                maxDate: new Date("2014/06/19") // sets max date to be pick able in DatePicker calendar

            });

        });      

{% endhighlight %}

N> You can change the ‘**minDate’** and ‘**maxDate’** value dynamically like ‘**value’** property

## Start and Depth Level

Start and depth represents the view of DatePicker calendar. DatePicker calendar has four different level of views, which are month, year, decade and century. It allows you to quick pick date from different months and years by drilling down or up. 

By default DatePicker starts with month view and can be drill down into year, decade and century. You can also change the start and depth level view by using [startLevel](https://help.syncfusion.com/api/js/ejdatepicker#members:startlevel) and [depthLevel](https://help.syncfusion.com/api/js/ejdatepicker#members:depthlevel) property. So that you can initiate DatePicker calendar to view at any level and control the navigation.

* “month”   – shows the days in month to pick.
* “year”    – shows the months in year to pick.
* “decade”  – shows the years in decade to pick.
* “century” – shows the decades in century to pick.

{% highlight javascript %}

    $(function () {

        // creates DatePicker from input with current date value

         var dateSample = new ej.DatePicker($("#datepicker"), {

            value: new Date(), // sets the current date.

            startLevel: ej.DatePicker.Level.Year, //sets the start view in DatePicker calendar.

            depthLevel: ej.DatePicker.Level.Year, //defines when the DatePicker calendar to return date.

            dateFormat: "MMMM yyyy" //sets the date format to display in input.

        });

    });

{% endhighlight %}

## Display Inline Mode

DatePicker provides an option to act as calendar by setting the [displayInline](https://help.syncfusion.com/api/js/ejdatepicker#members:displayinline) property as true. In this mode the DatePicker calendar has been placed open state constantly to pick the date. 

You can make use of ‘div’ element to create DatePicker when you going for inline mode, which gives good visualization as like calendar in page instead of creating with ‘input’ element. 

{% highlight html %}

    <!--div element to create inline mode DatePicker-->

    <div id="datePicker"></div>

{% endhighlight %}

{% highlight javascript %}

        $(function () {

            // create DatePicker from div

             var dateSample = new ej.DatePicker($("#datepicker"), {

                displayInline: true //sets inline to represent datePicker as DatePicker calendar

            });

        });

{% endhighlight %}

## Strict Mode

Strict mode in DatePicker allows you to enter valid or invalid date in input textbox, but an error class will get added to exhibit if it’s an invalid date. When you set [enableStrictMode](https://help.syncfusion.com/api/js/ejdatepicker#members:enablestrictmode) to false, DatePicker allows you to enter only the valid date or else it will resets with previous value. 

Also the valid date should be defined in specified range or else it resets to min or maximum date when the entered date is out of range

By default “**enableStrictMode**” is true, so you can enter any value other than date too, but an **error** class (**‘.** **e** **-** **error’**) will get added to wrapper to highlight the invalid date.

{% highlight javascript %}

        $(function () {

            // create DatePicker from input

             var dateSample = new ej.DatePicker($("#datepicker"), {

                enableStrictMode: false //sets active strict mode

            });

        });

{% endhighlight %}

You can also override the **“** **error** **”** class to highlight when invalid date is entered.

{% highlight javascript %}

        $(function () {

            // create DatePicker from input

             var dateSample = new ej.DatePicker($("#datepicker"), {

                enableStrictMode: true //sets inactive strict mode

            });

        });
		
{% endhighlight %}

{% highlight css %}

    <style>
        /* error class to highlight invalid date */

        .e-error .e-input {
            color: Red; /* highlights invalid date font color in input */
        }
    </style>

{% endhighlight %}

