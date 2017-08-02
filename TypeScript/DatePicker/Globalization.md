---
layout: post
title: Globalization and Localization
description: Globalize formatting and Localize strings in DatePicker  
platform: TypeScript
control: DatePicker
documentation: ug
---
# Globalization

DatePicker has been provided with Built-in localization support, so that it will be able adapt based on culture specific locale defined for it. 

More than 350 culture specific files are available to localize the date. To know more about EJ globalize support, please refer the below link      
 [https://help.syncfusion.com/js/localization](https://help.syncfusion.com/js/localization) 

N> Seven culture-specific script files are available in the below specified location. For all other culture files, please download from the [GitHub](https://github.com/syncfusion/ej-global/tree/master/i18n) location.

<table>
<tr>
<td>

    (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n

    For example, If you have installed the Essential Studio package within C:\Program Files (x86), then navigate to the below location, 
    C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n

</td></tr>
</table>
To translate our control content from default English to any of the culture, say For example - German language, then you need to refer the ej.culture.de-DE.min.js file in your application,

The **en-US** locale is currently being used as default culture in DatePicker. You can set any other culture to DatePicker by using **Locale** property. Below code example shows German cultured DatePicker.

Refer the below German culture file in head section of HTML page after the reference of **ej.web.all.min.js** file.

 {% highlight javascript %}
   
           <script src="https://cdn.syncfusion.com/js/assets/i18n/ej.culture.de-DE.min.js"></script>
                
 {% endhighlight %}

Set German culture to DatePicker at initialization.

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DatePickerComponent {
        $(function () {

            // create DatePicker from input with current date value

            var dateSample = new ej.DatePicker($("#datepicker"), {

                value: new Date(), // sets the current date

                locale: "de-DE" // sets German culture

            });

        });
}

{% endhighlight %}

## Watermark and Today Button Text

By default DatePicker input has **“select date”** as watermark text, you can also change this value by using [watermarkText](https://help.syncfusion.com/api/js/ejdatepicker#members:watermarktext) property. Also there’s a today button in DatePicker calendar which allows you to quick select the current date and its value can be changed by using **‘buttonText’** property.

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            var dateSample = new ej.DatePicker($("#datepicker"), {

                watermarkText: "enter date value",// sets watermart text in input

                buttonText: "current date" // sets button text in DatePicker calendar

            });

        });

{% endhighlight %}

Based on culture specific, only date gets localized but by changing the watermark and button text, you can completely localize the DatePicker UI too.

Refer below code example to update those value based some culture say for example English and German.

{% highlight javascript %}

    ej.DatePicker.Locale['en-US'] = {
        watermarkText: "Select date",
        buttonText: 'Today'
    };

    ej.DatePicker.Locale['de-DE'] = {
        watermarkText: "Zeitraum auswählen",
        buttonText: 'Heute'
    };

{% endhighlight %}

