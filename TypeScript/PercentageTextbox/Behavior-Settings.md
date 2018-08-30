---
layout: post
title: Behavior-Settings
description: behavior settings
platform: typescript
control: PercentageTextBox 
documentation: ug
---

# Behavior Settings

## Decimal Places

The property **decimalPlaces** declares the decimal point to the value of **PercentageTextBox** control. The default value of **decimalPlaces** is 0 in **PercentageTextBox** control. To set the decimalPlaces to “-1”, that allows the decimals without any limit in PercentageTextBox control.

### Configure Decimal Places

The following steps explain the implementation of **decimalPlaces** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



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
            value: 22,
            decimalPlaces: 2
        });
    });
}

{% endhighlight %}


The output for **PercentageTextBox** with **decimalPlaces** is as follows.



![](Behavior-Settings_images/Behavior-Settings_img1.png) 

## Persistence Support

The **PercentageTextBox** widgets provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

### Configure Persistence Support 

The following steps explain the implementation of **enablePersistence** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.


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
            value: 22,
            enablePersistence: true
        });
    });
}


{% endhighlight %}


The output for **PercentageTextBox** with **enablePersistence** is as follows. You can change the value of **PercentageTextBox** and reload the web page.



![](Behavior-Settings_images/Behavior-Settings_img2.png)

PercentageTextBox at initial load
{:.caption}

![](Behavior-Settings_images/Behavior-Settings_img3.png)

PercentageTextBox after changing the value and a page load 
{:.caption}


## Strict Mode Support

The **PercentageTextBox** widget allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. When the Textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the Textbox value goes below **minValue**, it restricts the new value and returns the **minValue**.When this property is true, it will not restrict the specified value and an error class will be added to indicate wrong value is provided to the PercentageTextBox.

### Configure Strict Mode Support 

The following steps explain the implementation of **enableStrictMode** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 


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
            value: -10,//value(-10) is under minValue(-5),so Error class will be added.
            minValue: -5,
            maxValue: 3,
            enableStrictMode: true
        });
    });
}


{% endhighlight %}


The output for **PercentageTextBox** when **enableStrictMode** is **“true”** is as follows**.**



![](Behavior-Settings_images/Behavior-Settings_img4.png) 

## Enabled or Disabled

The **PercentageTextBox** control has an option to enable or disable its element. You can set the **enabled** property as “**true**” to enable the **PercentageTextBox** control.
Also you can enable/disable the **PercentageTextBox** by using [enable](https://help.syncfusion.com/api/js/ejtextboxes#methods:enable) and [disable](https://help.syncfusion.com/api/js/ejtextboxes#methods:disable) methods.

### Configure Enabled or Disabled 

The following steps explains the implementation of **enabled** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 


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
            value: 2,
            enabled: false
        });
    });
}   


{% endhighlight %}


The output for **PercentageTextBox** when **enabled** is **“true”** and when **enabled** is “**false**”**.**



![](Behavior-Settings_images/Behavior-Settings_img5.png)

PercentageTextBox with enabled as true
{:.caption}

![](Behavior-Settings_images/Behavior-Settings_img6.png)

PercentageTextBox with enabled as false
{:.caption}

## Adjusting PercentageTextBox Size

The **PercentageTextBox** size can be modified by using the **height** and **width** properties. You can customize the size of **PercentageTextBox** by using these properties.

### Configure Height and Width 

The following steps explain the implementation of **height** and **width** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 


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
        value: 2,
        width: 100,
        height: 40
    });
 });
}


{% endhighlight %}


The output for **PercentageTextBox** after setting “**height**” and “**width**” is as follows**.**



![](Behavior-Settings_images/Behavior-Settings_img7.png) 

## Increment Step

The **incrementStep** property is used to increase or decrease the amount of value in the **PercentageTextBox** control. 

### Configure Increment Step

The following steps explain the implementation of **incrementStep** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.


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
            value:1,
            incrementStep: 3
        });
    });
}  


{% endhighlight %}


The output for **PercentageTextBox** with **incrementStep** is as follows**.**



![](Behavior-Settings_images/Behavior-Settings_img8.png)

PercentageTextBox at initial load
{:.caption}



![](Behavior-Settings_images/Behavior-Settings_img9.png)

PercentageTextBox after increasing one step
{:.caption}

## Define Name

When you have placed the **PercentageTextBox** in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

### Configure Name

The following steps explain the implementation of **name** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.


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
            name: "percent"         
        });
    });
}   


{% endhighlight %}


## Define Value

The value of **PercentageTextBox** can be assigned by using the **value** property. The default value for **value** property is null.
You can get the value of **PercentageTextBox** by using [getValue](https://help.syncfusion.com/api/js/ejtextboxes#methods:getvalue) method.

### Configure Value

The following steps explain the implementation of **value** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 


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
            value: 21               
        });
    });
}  


{% endhighlight %}


The output for **PercentageTextBox** with the **value** property is as follows**.**

![](Behavior-Settings_images/Behavior-Settings_img11.png) 

## Define maxValue and minValue

### maxValue

The maximum limit value can be assigned to the **PercentageTextBox** by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

### minValue

The minimum limit value can be assigned to the **PercentageTextBox** by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

### Configure maxValue and minValue

The following steps explain the implementation of **maxValue** and **minValue** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



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

        //PercentageTextBox with maxValue
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module EditorComponent {
    $(function () {
        var number = new ej.PercentageTextbox($("#percent"), {
            maxValue: 3,
            value:5
        });
    });
}
         //PercentageTextBox with minValue

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module EditorComponent {
    $(function () {
        var number = new ej.PercentageTextbox($("#percent"), {
            minValue: -2,
            value:-5
        });
    });
}  


{% endhighlight %}


The output for **PercentageTextBox** with basic properties is as follows**.**



![](Behavior-Settings_images/Behavior-Settings_img12.png)

PercentageTextBox with maxValue
{:.caption}



![](Behavior-Settings_images/Behavior-Settings_img13.png)

PercentageTextBox with minValue
{:.caption}

## Read Only Support

The **PercentageTextBox** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the **PercentageTextBox**. You can set the **readOnly** property as “**true”** to enable this option.

### Configure Read Only

The following steps explain the implementation of **readOnly** in **PercentageTextBox**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



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
            value: 3,
            readOnly: true
        });
    });
}  


{% endhighlight %}


The output for **PercentageTextBox** when **readOnly** is “**true**” is as follows**.** The **PercentageTextBox** values cannot be edited or changed.



![](/js/PercentageTextBox/Behavior-Settings_images/Behavior-Settings_img14.png) 

## Appearance

### Theme

The **PercentageTextBox** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Textbox** control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.web.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.web.all.min.css** is the combination of these two. 

By default, there are 17 themes support available for **PercentageTextBox** control namely:

* bootstrap
* flat-azure
* flat-azure-dark
* fat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* high-contrast-01
* high-contrast-02
* material
* office-365

### CSS Class

The **CSS** can be customized by using the **cssClass** in the **PercentageTextBox**. You can customize the **PercentageTextBox** with various **cssClass** properties to appear like your desired control.

### Configure CSS Class

The following steps explain the implementation of **cssClass** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



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
            value: 2,
            cssClass: "customCss"
        });
    });
}   


{% endhighlight %}


Customize the CSS properties in custom CSS class.



{% highlight css %}


<style>
    .customCss .e-box {
        border-color: #9d241b;
    }
    .customCss .e-input {
        background-color: #f6db8d;            
    }
    .customCss .e-select {
        background-color: #ecf6ac;
        border-color: #3c36e7;
    }
</style>



{% endhighlight %}



The output for **PercentageTextBox** after applying **cssClass** is as follows.



![](Behavior-Settings_images/Behavior-Settings_img15.png) 

## Rounded Corner Support

The **PercentageTextBox** provides you with rounded corner support whose appearance is different from normal textbox controls.

### Configure Rounded Corner Support

The following steps explain the implementation of **showRoundedCorner** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



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
            value: 2,
            showRoundedCorner: true
        });
    });
}  


{% endhighlight %}


The output for **PercentageTextBox** when **showRoundedCorner** is “**true**”.



![](Behavior-Settings_images/Behavior-Settings_img16.png) 

## Spin Button Support

The **PercentageTextBox** provides you the option as to whether to display the spin button in the widget or remove it from the control by using **showSpinButton** property.

### Configure Spin Button

The following steps explain the implementation of **showSpinButton** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 


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
            value: 2,
            showSpinButton: true
        });
    });
}   


{% endhighlight %}


The output for **PercentageTextBox** when **showSpinButton** is “**true**”.



![](Behavior-Settings_images/Behavior-Settings_img17.png)

PercentageTextBox with showSpinButton is true
{:.caption}

![](Behavior-Settings_images/Behavior-Settings_img18.png)

PercentageTextBox with showSpinButton is false
{:.caption}

## Water Mark Text Support

The **PercentageTextBox** provide water mark text support. You can display the initial value in the control by water mark.

### Configure Water Mark Text

The following steps explain the implementation of **watermarkText** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** controls. 


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
            watermarkText: "Percentage"
        });
    });
}   


{% endhighlight %}


The output for **PercentageTextBox** after applying **watermarkText** is as follows.



![](Behavior-Settings_images/Behavior-Settings_img19.png) 

