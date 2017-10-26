---
layout: post
title: Globalization-Support
description: globalization support
platform: Typescript
control: NumericTextbox
documentation: ug
---

# Globalization Support

**Globalization** is language support based on the culture in **NumericTextBox** . You can achieve the **Globalization** using “**locale”** property in **NumericTextBox** . 

The widget provides multi-language support using globalization. You can customize the NumericTextBox with your own language style by using this feature. You can change the globalization by using the **locale** property. The default value for **locale** property is **en-US** in NumericTextBox control.

More than 350 culture specific files are available to localize the value. To know more about EJ globalize support, please refer the below link      
 [https://help.syncfusion.com/js/localization](https://help.syncfusion.com/js/localization) 
 
 N> All the culture-specific script files are available within the below specified location, once you have installed Essential Studio in your machine, therefore it is not necessary to download these files explicitly.

<table>
<tr>
<td>

    '(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n'
</td>
</tr>
<tr>
<td>
    For example, If you have installed the Essential Studio package within C:\Program Files (x86), then navigate to the below location, 
    C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n

</td></tr>
</table>

Refer the below German culture file in head section of HTML page after the reference of **ej.web.all.min.js** file.

 {% highlight javascript %}
   
           <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/i18n/ej.culture.de-DE.min.js"></script>
                
 {% endhighlight %}


You can dynamically change the language based on their culture.

**Configure Globalization**

The following example describes the way to use Globalization for NumericTextBox widget.

{% highlight html %}

<input id="numeric" type="text" />
        
{% endhighlight %}

{% highlight javascript %}

        /* Numeric Textbox */
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module EditorComponent {
    $(function () {
        var number = new ej.NumericTextbox($("#numeric"), {
            value: 12345,
            decimalPlaces: 2,
            locale: "de-DE"
        });
    });
} 

{% endhighlight %}







The output for **NumericTextBox** with Globalization.



![](Globalization-Support_images/Globalization-Support_img1.png)

NumericTextBox with de-DE locale
{:.caption}



![](Globalization-Support_images/Globalization-Support_img2.png)

NumericTextBox with en-US locale
{:.caption}

