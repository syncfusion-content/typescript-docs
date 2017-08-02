---
layout: post
title: Localization
description: localization
platform: TypeScript
control: DateTimePicker
documentation: ug
---

# Globalization

DateTimePicker has been provided with built-in localization support, so that it can adapt based on culture specific locale defined for it. 

More than 350 culture specific files are available to localize the datetime. To know more about EJ globalize support, please refer the below link      
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
To translate our control content from default English to any of the culture, say For example - Spanish language, then you need to refer the ej.culture.es-ES.min.js file in your application,

The **en-US** locale is currently being used as default culture in DateTimePicker. You can set any other culture to DateTimePicker using **Locale** property. Below code example shows Spanish cultured DateTimePicker.

Refer the below Spanish culture file in head section of HTML page after the reference of **ej.web.all.min.js** file.

 {% highlight javascript %}
   
           <script src="https://cdn.syncfusion.com/js/assets/i18n/ej.culture.es-ES.min.js"></script>
                
 {% endhighlight %}

If you want to change month names to your culture month just replace month names with your culture month names or your customized format.

The following code example is used to set DateTimePicker in Spanish language.

{% highlight javascript %}

    calendars: {
       standard: {
          firstDay: 1,
          days: {
             names: ["domingo", "lunes", "martes", "miércoles", "jueves", "viernes", "sábado"],
             namesAbbr: ["do.", "lu.", "ma.", "mi.", "ju.", "vi.", "sá."],
             namesShort: ["D", "L", "M", "X", "J", "V", "S"]
          },
          months: {
             names: ["enero", "febrero", "marzo", "abril", "mayo", "junio", "julio", "agosto", "septiembre", "octubre", "noviembre", "diciembre", ""],
             namesAbbr: ["ene.", "feb.", "mar.", "abr.", "may.", "jun.", "jul.", "ago.", "sep.", "oct.", "nov.", "dic.", ""]
          },
          AM: null,
          PM: null,
          eras: [{
             "name": "d. C.",
             "start": null,
             "offset": 0
          }],
          patterns: {
             d: "dd/MM/yyyy",
             D: "dddd, d' de 'MMMM' de 'yyyy",
             t: "H:mm",
             T: "H:mm:ss",
             f: "dddd, d' de 'MMMM' de 'yyyy H:mm",
             F: "dddd, d' de 'MMMM' de 'yyyy H:mm:ss",
             M: "d' de 'MMMM",
             Y: "MMMM' de 'yyyy"
          }
       }
    }

{% endhighlight %}



The following code example can be used to get Spanish culture in **DateTimePicker**.

Add the following code in your **HTML** page.


{% highlight html %}
  
<div class="control">
   <input type="text" id="dateTime" />
</div>

{% endhighlight %}


{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateTimePickerComponent {
    $(function () {
    // Add the code in your script section to render the DateTimePicker with Spanish culture
    var datetimeSample = new ej.DateTimePicker($("#datetimepick"), {
       locale: "es-ES",
       buttonText: { today: "hoy", timeNow: "ahora", done: "hecho", timeTitle: "tiempo" },
    });
    });
}

{% endhighlight %}

![](Globalization_images/Globalization_img1.png)

