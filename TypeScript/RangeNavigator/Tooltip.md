---
layout: post
title: Tooltip
description: Tooltip
platform: typescript
control: RangeNavigator
documentation: ug
---


### Tooltip

**RangeNavigator** provides **Tooltip** support for sliders. Sliders are used to select data at particular range in the **RangeNavigator** control. **Tooltips** for sliders display the selected start and end **DateTime** values.

#### Customization

**RangeNavigator** provides support for you to customize the text display in the tooltip and background using **tooltipSettings** property. You can change font family, font color, font style, font weight. By default “**Segoe UI**” font family is set to tooltip text.


{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

 $(function () {


var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
                   // ...              
                tooltipSettings: {
                    visible: true,  
                    backgroundColor: "black",
                           //  To customize the tooltip text

                        font: {
                            color: 'red',
                            family: 'Segoe UI',
                            style: 'Normal',
                            size: '12px',
                            opacity: 1,
                            weight: 'regular'
                        }

                },
                   // ...             
               });
 });
}


{% endhighlight %}



![](Tooltip_images/Tooltip_img1.png) 

#### Label Format

By default, the **tooltip** texts are automatically determined based on the data points.  To make it readable and understandable you can format the **tooltip** text. For **DateTime** data, all globalized format are supported. By default the **labelFormat** is "MM/dd/yyyy".

Some of the **labelFormat** for **DateTime** data area as follows:

* 'MMM, yyyy'
* 'dd, MMM'
* 'dd/MM/yyyy'
* 'dd, hh:mm'
* 'hh:mm:ss'
* 'hh:mm:ss:tt'


{% highlight javascript %}


var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {   
                   // ...              
                 tooltipSettings: {
                    labelFormat:'MMM, yyyy',
                },              
                   // ...             
               });


{% endhighlight %}


![](Tooltip_images/Tooltip_img2.png) 

#### Tooltip display mode

By default the **tooltip** for RangeNavigator gets displayed. You can change this behavior using the **tooltipDisplayMode** property in the tooltip and it takes the following values.



<table>
<tr>
<td>
<b>Value</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
always</td><td>
Tooltip get displayed for RangeNavigator always.</td></tr>
<tr>
<td>
onDemand</td><td>
Tooltip get displayed only when we move the slider.</td></tr>
</table>


{% highlight javascript %}


var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
                   // ...              
                 tooltipSettings: {
                         tooltipDisplayMode: "onDemand",                    
                },              
                   // ...             
               });


{% endhighlight %}



![](Tooltip_images/Tooltip_img3.png) 
