---
layout: post
title: Range-Types
description: Range Types
platform: typescript
control: RangeNavigator
documentation: ug
---

### Range Types

**RangeNavigator** control is designed to visualize large number of data and navigate to particular data from the large collection at ease. The data for the **RangeNavigator** is either numeric values or **DateTime** values and the **valueType** property in **RangeNavigator** indicates the type of the data that should be passed for the control. By default the **valueType** of **RangeNavigator** is **DateTime**

* Numeric                 
* DateTime

## Numeric Type

**RangeNavigator** is also used with numeric data and the **valueType** for this data is “**numeric**”

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

 $(function () {

    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
      //...
        valueType: "numeric",
      //...	
    });

 });
}


{% endhighlight %}


The following screenshot displays the **RangeNavigator** with numeric data.



![](Range-Types_images/Range-Types_img1.png) 

## DateTime

By default the **valueType** of the **RangeNavigator** is “**datetime**” and represents the **DateTime** values.

{% highlight javascript %}


var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
      //...
        valueType: "datetime",
      //...	
       });


{% endhighlight %}



![](Range-Types_images/Range-Types_img2.png) 

## DateTime Intervals

The **DateTime** range type contains an **intervalType** property that sets the **DateTime** interval to one of the following:

* Years
* Quarters
* Months
* Weeks
* Days 
* Hours

By default **intervalType** for higher level labels are **years** and for lower level labels its **quarters.**


{% highlight javascript %}


var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
   //...
     labelSettings:
      { 
          higherLevel:
            {
                intervalType: 'years',
            },
        lowerLevel:
           {
               intervalType: ' quarters',
           }
      },    
  //...	
  });


{% endhighlight %}





![](Range-Types_images/Range-Types_img3.png) 
