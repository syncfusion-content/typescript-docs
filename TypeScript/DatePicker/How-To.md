---
layout: post
title: How-to
description: How-to section
platform: TypeScript
control: DatePicker
documentation: ug
---
# How to?

## Customizing template with range selection between two DatePicker. 

You can customize the date field to emphasize the particular dates in DatePicker calendar with help of [specialDates](https://help.syncfusion.com/api/js/ejdatepicker#members:specialdates) and set the date range using [minDate](https://help.syncfusion.com/api/js/ejdatepicker#members:mindate) and [maxDate](https://help.syncfusion.com/api/js/ejdatepicker#members:maxdate) property. Refer the sample from the link [Hotel Booking](http://jsplayground.syncfusion.com/bdr5k4cg#) to know how to customize date with date range.

## Localize DatePicker with browser specific culture

You can get the browser culture name at page load or document ready state. Based on the culture name, DatePicker can be initiated with that specific culture value by assigning to [locale](https://help.syncfusion.com/api/js/ejdatepicker#members:locale) property. Refer the sample from the link [Browser Specific Culture](http://www.syncfusion.com/kb/4904/datepicker-control-culture-have-to-change-based-on-the-browser-language#) to create DatePicker with browser specific culture.

## Disable specific dates to restrict user

DatePicker allows you to restrict date selection in specific range by using date range option. But you can also restrict selective date in DatePicker calendar by utilizing [beforeDateCreate](https://help.syncfusion.com/api/js/ejdatepicker#events:beforedatecreate) event. This event will get triggered at each date creation. So you can disable the selective date in this event to restrict the user.

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
       $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                beforeDateCreate: "restrictDate" // handler to listen each date create.

            });

        });
}

        //event get triggered for each date create.

        function restrictDate(args) {

            //date to disable in DatePicker calendar to restrict selection.

            var disableDate = new Date("09/22/2015");

            //compares two and adds the disable class.

            if (+args.date === +disableDate)

                args.element.addClass('e-disable');

            // args contains current date and its element.          

        }


{% endhighlight %}

## How to integrate with bootstrap grid system? 

DatePicker is responsive control, you have to just set the input element width as 100%. In Bootstrap grid layout use the below code example to get responsive textbox. 

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
        $(function () {

            // creates DatePicker from input

            var dateSample = new ej.DatePicker($("#datepicker"), {

                width: '100%'// sets width as 100 percentage

            });

        });
}

{% endhighlight %}

## How to use DatePicker in AngularJS?

You can use DatePicker control in AngularJS Framework. To know more about JS component with AngularJS refer here [JS component in AngularJS](https://help.syncfusion.com/js/angularjs).

