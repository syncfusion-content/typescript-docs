---
layout: post
title: Rating-Customization
description: rating customization
platform: Typescript
control: Rating
documentation: ug
---

# Rating Customization

## Setting Value

The **Value** property sets the display value of the Rating. For example, when the **Value** property is set to be **four**, the Rating control renders four ratings. By default, **Value** property’s value is **one**.

The following code example is used to render the **Rating** control with customized value.

 Add the following HTML to render Rating with customized value.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

    // Add the following script to render Rating with customized value.
    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {
       var sample = new ej.Rating($("#rating"),{ 
        value: 4 
        });
    });
} 
{% endhighlight %}

The following screenshot illustrates the **Rating** with custom defined value.

![](Rating-Customization_images/Rating-Customization_img1.png) 

### Min Value

**EJ Rating** control provides support for setting **minimum** **value**. This is achieved by adding minValue property. When the minValue property is set, the Rating value starts with **minValue**+1.

The following code example is used to render the **Rating** control with **minimum** **rating**.

 Add the following HTML to render Rating with minimum value.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
   <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Add the following script to render Rating with minimum value.
    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {
       var sample = new ej.Rating($("#rating"),{  
        minValue: 3
        });
      });
    }   
   
{% endhighlight %}

The following screenshot illustrates **Rating** with **minimum** **value**.         

![](Rating-Customization_images/Rating-Customization_img2.png) 

### Max Value

**EJ** **Rating** **control** provides support for setting **maximum** **value**. This is achieved by adding the **maxValue** property**.** By default, maxValue is five.

The following code example is used to render the Rating control with **maximum** **rating**.

 Add the following HTML to render Rating with maximum value.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
   <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

    // Add the following script to render Rating with minimum value.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {
       var sample = new ej.Rating($("#rating"),{ 
        maxValue: 10
        });
    });
} 
{% endhighlight %}

The following screenshot illustrates the **Rating** with **maximum** **value**.

![](/Rating-Customization_images/Rating-Customization_img3.png) 

## Set Precision

In a real-time movie **Rating** scenario, you can set **Precision** between two whole numbers such as 2.5 or 3.7 and it is done using the property **Precision** by changing the value to **ej.Rating.Precision.Half** or **ej.Rating.Precision.Exact.** By default, **Precision** is **Full.**

The following code example is used to render the **Rating** control with **Precision**.

 Add the following HTML to render Rating with Precision.
{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Full Precision:
            </td>
            <td>
                <input id="rating" type="text" />
               
            </td>
        </tr>   
        <tr>
            <td valign="top">Half Precision:
            </td>
            <td>
                <input id="halfRating" type="text" />
               
            </td>
        </tr>  
        <tr>
            <td valign="top">Exact Precision:
            </td>
            <td>
                <input id="exactRating" type="text" />
               
            </td>
        </tr>         
    </table>
</div>
    
{% endhighlight %}

{% highlight javascript %}

    
    // Add the following script to render Rating with Precision.
 /// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {
       var sample = new ej.Rating($("#rating"),{  
            value: 4 
       });
      var sample1 = new ej.Rating($("#halfRating"),{  
            precision: ej.Rating.Precision.Half,
            value: 3.5
       });
      var sample2 = new ej.Rating($("#exactRating"),{  
            precision: ej.Rating.Precision.Exact,
            value: 3.7
       });
    });
 } 
{% endhighlight %}

The following screenshot illustrates the **Rating** with **Precision**.

![](Rating-Customization_images/Rating-Customization_img4.png) 

## Increment Step

**EJ Rating** control supports customized **increment** value for Rating. This is achieved by adding the **incrementStep** property.

The following code example is used to render the **Rating** control with customized **increment**.

 Add the following HTML to render Rating with customized increment.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

    // Add the following script to render Rating with customized increment.

 /// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {
         var sample = new ej.Rating($("#rating"),{  
         incrementStep: 2, 
         maxValue: 10
    });
 });
}
{% endhighlight %}

The following screenshot illustrates the **Rating** with customized increment.

![](Rating-Customization_images/Rating-Customization_img5.png) 

## Resetting values

**EJ Rating** control provides support for value **reset** at runtime. This is achieved by enabling the **allowReset** property to be **‘True’.** By default, the property value is set to **‘True’.**

The following code example is used to render the **Rating** control with **allowReset**.

 Add the following HTML to render Rating with allowReset.

{% highlight javascript %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
               
            </td>
        </tr>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                 <input id="rest" type="text" />                    
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Add the following script to render Rating with allowReset.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {  
        var sample = new ej.Rating($("#rating"),{  
            allowReset: true
        });
      var sample = new ej.Rating($("#rest"),{  
           allowReset: false 
           });
     });
}
{% endhighlight %}

The following screenshot illustrates the **Rating** with **allowReset**.

![](Rating-Customization_images/Rating-Customization_img6.png) 

## Read only

**Rating** control provides support for changeable or unchangeable values for **Rating** control. This is achieved by the **readOnly** property. When this property is set to **‘True’** the **Rating** value becomes unchangeable. By default, this property value is set to **‘False’.**

The following code example is used to render the **Rating** control with **readOnly**.

 Add the following HTML to render Rating with readOnly.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

     // Add the following script to render Rating with readOnly .

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {  
        var sample = new ej.Rating($("#rating"),{  
          readOnly: true
           });
    });
}    
 
{% endhighlight %}


The following screenshot illustrates the **Rating** with **readOnly.**

![](/js/Rating/Rating-Customization_images/Rating-Customization_img7.png) 

## Enable or Disable

**Rating** control provides support to **enable** or **disable** the control. This is achieved by the **enabled** property. By default the property value is **‘True’.**

The following code example is used to render the **Rating** control with **enable** or **disable** support.

 Add the following HTML to render Rating with enable or disable support.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
            </td>
            <td>
                <input id="rating" type="text" />
            </td>
        </tr>
    </table>
</div>
    
{% endhighlight %}

{% highlight javascript %}

    // Add the following script to render Rating in disabled form.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RatingComponent {
    $(function () {  
        var sample = new ej.Rating($("#rating"),{  
        enabled: false 
        });
    });
}  
{% endhighlight %}



The following screenshot illustrates the **Rating** in **disabled** form.

![](Rating-Customization_images/Rating-Customization_img8.png) 

