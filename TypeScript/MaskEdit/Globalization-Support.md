---
layout: post
title: Globalization-Support
description: globalization support
platform: Typescript
control: MaskEdit  
documentation: ug
---

# Globalization Support in MaskEdit

We have provided the globalization support in **MaskEdit** control. Our **MaskEdit** control mainly rendered based on the **maskFormat** property, so we have provided the globalization support based on the maskFormat literals. We have given this globalization support option on below maskFormat literals in **MaskEdit** control. You can change the globalization by using the [locale](https://help.syncfusion.com/api/js/ejmaskedit#members:locale) property. The default value for **locale** property is 'en-US' in **MaskEdit** control.

<table class="props">
<thead>
<tr>
<th>Formats</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="formats">
$</td>
<td class="description">Currency symbol value will be changed based on the corresponding culture.</td>
</tr>
<tr>
<td class="formats">
.</td>
<td class="description">Decimal Separator value will be changed based on the corresponding culture.</td>
</tr>
<tr>
<td class="formats">
,</td>
<td class="description">Thousand Separator will be changed based on the corresponding culture.</td>
</tr>
</tbody>
</table>

To know more about EJ globalize support, please refer the below link

[https://help.syncfusion.com/js/localization](https://help.syncfusion.com/js/localization)


The following example describes the way to use localization for **MaskEdit** widgets.

Refer the below German culture file in head section of HTML page after the reference of **ej.web.all.min.js** file.

 {% highlight javascript %}
   
           <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/i18n/ej.culture.de-DE.min.js"></script>
                
 {% endhighlight %}

{% highlight html %}

<table cellpadding="10">
    <tbody>
        <tr>
            <td>
                <label for="mask">Mask Edit</label>
            </td>
            <td>
                <input id="maskEdit" type="text" />
            </td>
        </tr>
    </tbody>
</table>

{% endhighlight %}

{% highlight javascript %}
    
/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
    var mask = new ej.MaskEdit($("#maskEdit"), {
                     locale: "de-De", //specifies the culture for MaskEdit control
                     width: "100%",
                     maskFormat:"$99,999.99",
			         value:”1234567”
        })
}

{% endhighlight %}

The output for **MaskEdit** with Globalization.

![](Globalization-Support_images/Globalization-Support_img1.jpg)

MaskEdit with `de-DE` locale
{:.caption}

![](Globalization-Support_images/Globalization-Support_img2.jpg)

MaskEdit with en-US locale
{:.caption}