---
layout: post
title: Globalization & Localization in TypeScript RangeNavigator | Syncfusion
description: Learn here about Globalization and Localization in Syncfusion Essential TypeScript RangeNavigator Control, its elements, and more.
platform: typescript
control: RangeNavigator
documentation: ug
---


# Globalization and Localization in TypeScript RangeNavigator

**RangeNavigator** supports Localization and Globalization to customize the labels based on a culture specific to a country. The culture defines specific information for the number formats, week and month names, date and time formats etc. 

## Localization

**Localization** is the process of customizing the user interface based on a culture specific to a particular country or region in order to display regional data.  The culture is represented by a unique string, for example, ―en-US‖ for U.S. English and ―fr-FR‖ for French (common), this is achieved by creating a JavaScript file “**rangeNavigatorSource.fr-FR.js**” and setting the equivalent word as illustrated in the following code sample.



{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

 $(function () {

var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
    locale:'fr-Fr',
    intervals: {
        //string to display the intervals on RangeNavigator
        quarter: {longQuarters: "Trimestre", shortQuarters: "T"},
        week: { longWeeks: "Semaine", shortWeeks: "S" }
    }
});
});
}


{% endhighlight %}

**Localization** is the key feature that provides solutions globally with the help of localized control. 

{% highlight javascript %}


               var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {   
                   // ...              
                   locale: 'fr-FR',
                   // ...             
               });


{% endhighlight %}



![TypeScript RangeNavigator localization and globalization](Globalization-And-Localization_images/Globalization-And-Localization_img1.png) 

### RTL

**Right-to-Left** or **RTL** describes the ability of application to handle and responds you to communicate with a right-to-left language, like Arabic or Japanese. **enableRTL** property is used to change the rendering format  to **"Right to Left"**, by default it renders from **"Left to Right"** in **RangeNavigator**.

{% highlight javascript %}


              var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), { 
                   // ...              
                   enableRTL:true,
                  // ...             
               });


{% endhighlight %}



![TypeScript RangeNavigator RTL](Globalization-And-Localization_images/Globalization-And-Localization_img2.png) 



