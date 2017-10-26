---
layout: post
title: Globalization-Support
description: globalization support
platform: typescript
control: PercentageTextBox 
documentation: ug
---

# Globalization Support

**Globalization** is language support based on the culture in **Textboxes**. You can achieve the **Globalization** using “**locale”** property in **PercentageTextBox** . 

The **PercentageTextBox** widget provides multi-language support using globalization. You can customize the **PercentageTextBox** with your own language style by using this feature. You can change the globalization by using the **locale** property. The default value for **locale** property is **en-US** in **PercentageTextBox** control.


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

## Configure Globalization

The following example describes the way to use Globalization for **PercentageTextBox** widget.

{% highlight html %}


<table cellpadding="10">
    <tbody>
        <tr>
            <td>
                <label for="percent">Percent</label>
            </td>
            <td>
                <input id="percent" type="text" />
            </td>
        </tr>
    </tbody>
</table>

{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module EditorComponent {
    $(function () {
        var number = new ej.PercentageTextbox($("#percent"), {
            value: 21234,
            decimalPlaces: 3,
            locale: "de-DE"
        }); 
    });
}     


{% endhighlight %}

The output for **PercentageTextBox** with Globalization.



![](Globalization-Support_images/Globalization-Support_img1.png)

PercentageTextBox with de-DE locale
{:.caption}



![](Globalization-Support_images/Globalization-Support_img2.png)

PercentageTextBox with en-US locale				
{:.caption}

