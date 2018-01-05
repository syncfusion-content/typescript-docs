---
layout: post
title: Easy-Customization
description: easy customization
platform: TypeScript
control: RadioButton
documentation: ug
---

# Easy Customization

## Checked status

You have options to set the state of the radio button as either checked or unchecked. When you select any option from the group of radio buttons, a dot mark appears inside the circle. This is called the **checked** **state**. Previously selected radio buttons in this group are unselected that is they go to the **unchecked state**. The **checked** property is used to set the state of the radio button.

The following steps explain the details about rendering the **RadioButton** with the **checked** option

In the **HTML** page, add the following input elements to configure **RadioButton** widget.

{% highlight html %}


<div class="page-align">
    <table>
        <tr>
            <td>
                <input type="radio" id="Radio_checked" />
            </td>
            <td>
                <label for="Radio_checked" >Male</label>
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="Radio_unchecked" />
            </td>
            <td>
                <label for="Radio_unchecked">Female</label>
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RadioButtonComponent {
    $(function () {
        // Here we render checked and unchecked type of radio buttons in same group
        // set checked state of radio button as follows
         var radioButton = new ej.RadioButton($("#Radio_checked"), {
             name: "Gender",
             checked: true 
         });
         var radioButton1 = new ej.RadioButton($("#Radio_unchecked"), {
             name: "Gender" 
             });
        });
} 
{% endhighlight %}


Configure the CSS styles to align the radio buttons.



{% highlight css %}

<style>
    .page-align {
        margin: 100px;
    }
</style>


{% endhighlight %}


The following image is displayed as the output for the above steps.



![](Easy-Customization_images/Easy-Customization_img1.png) 

## Text

Specifies the text content for the radio button. In previous programs, separate labels were created for each radio button. But now you have the option to set the text for radio button using the **text** property. So here you do not have to add a label tag for each radio button in the **HTML** code.

The following steps explain the details about rendering the **RadioButton** with **text** and without using the label tag options.

In the **HTML** page, add the following input elements to configure the **RadioButton** widget.

{% highlight html %}


<div class="page-align">
    <table>
        <tr>
            <td>
                <!--here we did not use label tag-->
                <input type="radio" id="RadBtu_male" />
            </td>
        </tr>
        <tr>
            <td>
               <!-- here we did not use label tag-->
                <input type="radio" id="RadBtu_female" />
            </td>
        </tr>
    </table>
</div>


{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RadioButtonComponent {
    $(function () {
        // radio button with text property
    var radioButton = new ej.RadioButton($("#RadBtu_male"), {
             name: "Gender", 
             checked: true,
             text: "Male"
         });
    var radioButton1 = new ej.RadioButton($("#RadBtu_female"), {
            name: "Gender", 
            text: "Female" 
        });
    });
}
{% endhighlight %}


Configure the CSS styles to align the radio buttons.



{% highlight css %}

<style>
    .page-align {
        margin: 100px;
    }
</style>


{% endhighlight %}



The following image is displayed as the output for the above steps.

![](Easy-Customization_images/Easy-Customization_img2.png) 

## Size

You can render the **RadioButton** in different sizes. There are some predefined size options available for rendering a **RadioButton** in an easy way. Each size option has different height and width. It mainly avoids the complexity in rendering **RadioButton** with complex CSS class. 

Size

<table>
<tr>
<th>Property</th><th>Description</th></tr>
<tr>
<td>
small</td><td>
Creates radio button with Built-in small size height, width specified.</td></tr>
<tr>
<td>
medium</td><td>
Creates radio button with Built-in medium size height, width specified.</td></tr>
</table>


The following steps explain the details about rendering **RadioButton** with different size options.

In the HTML page, add the following input elements to configure RadioButton widget.

{% highlight html %}


<div class="page-align">
    <table>
        <tr>
            <td>Small size Radio buttons
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="RadBtu_male" />
                <label for="Radio_Male">Male</label>
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="RadBtu_male" />
                <label for="Radio_Female">Female</label>
            </td>
        </tr>
    </table>
    <table>
        <tr>
            <td>Medium size Radio buttons
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="Radio1_Male" />
                <label for="Radio1_Male">Male</label>
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="Radio1_Female" />
                <label for="Radio1_Female">Female</label>
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RadioButtonComponent {
    $(function () {
     // small size of radio buttons in same group   
      var radioButton = new ej.RadioButton($("#RadBtu_male"), {       
            name: "Gender",
            size: "small",
            checked: true 
        });
     var radioButton1 = new ej.RadioButton($("#RadBtu_male"), {     
             name: "Gender", 
             size: "small" 
        });
        // Medium size of radio buttons in same group
    var radioButton2 = new ej.RadioButton($("#Radio1_Male"), {            
             name: "Gender1", 
             size: "medium",
             checked: true 
             });
    var radioButton3 = new ej.RadioButton($("#Radio1_Female"), {     
            name: "Gender1", 
            size: "medium"
         });
    
    });
}
{% endhighlight %}


Configure the CSS styles to align the radio buttons.


{% highlight css %}

<style>
    .page-align {
        margin: 100px;
    }
</style>


{% endhighlight %}


The following image is displayed as the output for the above steps.

![](Easy-Customization_images/Easy-Customization_img3.png) 


## RTL Support 

In some cases you need to use right-to-left alignment. You can give RTL support by using **enableRTL** property.  **RTL** mode works when you use the **text** property in **RadioButton**. The **RadioButtons** and text are aligned in the right-to-left format. For example, when text is right-aligned and RadioButton is left-aligned, after you apply right-to-left alignment, these positions are interchanged. 

The following steps explain the details about rendering the **RadioButton** with right-to-left alignment support. Here the **text** property is necessary.

In the HTML page, add the following button elements to configure RadioButton widget.

{% highlight html %}


<div class="page-align">
    <table class="rightAlign">
        <tr>
            <td>
                <input type="radio" id="RadBtu_male" />
            </td>
        </tr>
        <tr>
            <td>
                <input type="radio" id="RadBtu_female" />
            </td>
        </tr>
    </table>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RadioButtonComponent {
    $(function () {
        //set radio button with right to left format
       var radioButton = new ej.RadioButton($("#RadBtu_male"), {      
            name: "Gender", 
            checked: true,
            text: "Male",
            enableRTL: true
        });
     var radioButton1 = new ej.RadioButton($("#RadBtu_female"), {      
            name: "Gender",
            text: "Female",
            enableRTL: true
        });
    });
}
{% endhighlight %}


In the above mentioned code, the **text** property has been used. In **LTR** format, the **RadioButton** is on the left side. In **RTL** format, the **RadioButton** appears on the right side. Here the **text** property is used and the **enableRTL** property is set as “**true**”**.** It changes the alignment to right-to-left.

Configure the CSS styles to align the RadioButtons.



{% highlight css %}

<style>
    .page-align {
        margin: 100px;
    }
    .rightAlign {
        text-align: right;
    }
</style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



![](Easy-Customization_images/Easy-Customization_img4.png) 

