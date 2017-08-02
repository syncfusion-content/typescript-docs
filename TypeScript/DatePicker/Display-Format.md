---
layout: post
title: Display Format
description: Formatting - Date and Time, Headers.
platform: TypeScript
control: DatePicker
documentation: ug
---
# Formatting

Formatting is the way of displaying the date or number as string in some standard format which is based on culture specific or user need.

Below table shows the patterns to format date value.

<table>
<tr>
<th>
Format Pattern </th><th>
Description </th><th>
Result</th></tr>
<tr>
<td>
d<br/><br/></td><td>
The day of the month between 1 and 31.  <br/><br/></td><td>
"1"  to "31"<br/><br/></td></tr>
<tr>
<td>
dd<br/><br/></td><td>
The day of the month with leading zero if required.<br/><br/></td><td>
"01" to "31"<br/><br/></td></tr>
<tr>
<td>
ddd<br/><br/></td><td>
Abbreviated day name.<br/><br/></td><td>
"Mon" to "Sun"<br/><br/></td></tr>
<tr>
<td>
dddd<br/><br/></td><td>
The full day name<br/><br/></td><td>
"Monday" to "Sunday"<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
M<br/><br/></td><td>
The month of the year between 1 - 12<br/><br/></td><td>
"1" to "12"<br/><br/></td></tr>
<tr>
<td>
MM<br/><br/></td><td>
The month of the year with leading zero if required<br/><br/></td><td>
"01" to "12"<br/><br/></td></tr>
<tr>
<td>
MMM<br/><br/></td><td>
Abbreviated month name<br/><br/></td><td>
"Jan" to "Dec"<br/><br/></td></tr>
<tr>
<td>
MMMM<br/><br/></td><td>
The full month name<br/><br/></td><td>
"January" to "December"<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
yy<br/><br/></td><td>
The year as a two-digit number<br/><br/></td><td>
"99" or "08"<br/><br/></td></tr>
<tr>
<td>
yyyy<br/><br/></td><td>
The full four digit year<br/><br/></td><td>
"1999" or "2008"<br/><br/></td></tr>
</table>

## Date Format

Each culture has some specific date format. Date format defines a format or structure of the displayed date in the textbox. You can change the date format by using [dateFormat](https://help.syncfusion.com/api/js/ejdatepicker#members:dateformat) property

The standard formats are listed as follows

<table>
<tr>
<th>
Format Name <br/><br/></th><th>
Formats <br/><br/></th></tr>
<tr>
<td>
default<br/><br/></td><td>
"M/d/yyyy"<br/><br/></td></tr>
<tr>
<td>
Short<br/><br/></td><td>
“d M, y”<br/><br/></td></tr>
<tr>
<td>
Medium <br/><br/></td><td>
“d MM, y”<br/><br/></td></tr>
<tr>
<td>
Full <br/><br/></td><td>
“dddd, d MMMM, yy”<br/><br/></td></tr>
<tr>
<td>
UTC<br/><br/></td><td>
“yyyy-MM-dd”<br/><br/></td></tr>
</table>
By default ‘en-US’ culture date format is "M/d/yyyy".

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
        $(function () {

            // create DatePicker from input

           var dateSample = new ej.DatePicker($("#datepicker"), {

                value: new Date(), // sets the current date

                locale: "en-US", // sets English -US culture

                dateFormat: "yyyy/dd/MM" // sets the date format to display in input.

            });

        });
}

{% endhighlight %}

To get the culture and date format of DatePicker, refer the below code example

{% highlight javascript %}

        // create instance for datePicker

        // only after control creation we can get dateObj otherwise it throws exception

        var dateObj = $("#datePicker").ejDatePicker('instance');

        dateObj.option('locale'); //returns the culture in string

        dateObj.option('dateFormat');// returns the date Format in string  

{% endhighlight %}

N> by default date format is based on culture specific. You have to refer the required culture specific files in head section of HTML page in order to localize DatePicker and customize different format for that culture. 

## Header Format

DatePicker calendar consists of header, day header, days and footer section. In which header section shows the current view of DatePicker calendar by displaying the selected day or month or year. It can be formatted as like date format by using [headerFormat](https://help.syncfusion.com/api/js/ejdatepicker#members:headerformat) property.

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            var dateSample = new ej.DatePicker($("#datepicker"), {

                headerFormat: "yyyy MMMM" //sets the selected header format to display in header.

            });

        });

{% endhighlight %}

## Day Header

Day header determines the days name to be displayed in terms of short, medium and long in DatePicker calendar by using [dayHeaderFormat](https://help.syncfusion.com/api/js/ejdatepicker#members:dayheaderformat) property. Also the DatePicker calendar size varies with this specified values.

{% highlight javascript %}

        $(function () {

            // create DatePicker from input

            var dateSample = new ej.DatePicker($("#datepicker"), {

                dayHeaderFormat: ej.DatePicker.Header.Long //sets the day header as long

            });

        });

{% endhighlight %}

## Tooltip with Formatting

DatePicker calendar shows tooltip on hovering the date by specifying the formatted date of hovered date. Its helps you to get clear view about the date going to select. You can show or hide this tooltip option by using [showTooltip](https://help.syncfusion.com/api/js/ejdatepicker#members:showtooltip ) property.

You can also change the format of tooltip by using “**tooltipFormat**” property. Below codes example allows to show tooltip and format its value. 

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            var dateSample = new ej.DatePicker($("#datepicker"), {

                showTooltip: true, //show tooltip on hovering date on DatePicker calendar

                tooltipFormat: "dd/MM/yy"// sets tooltip for dates in DatePicker calendar

            });

        });

{% endhighlight %}

