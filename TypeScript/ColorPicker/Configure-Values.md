---
layout: post
title: Configure-Values
description: configure values
platform: TypeScript
control: ColorPicker
documentation: ug
---

# Configure Values

## opacityValue

The **ColorPicker** control allows you to change the opacity value by using the **opacityValue** property. The selected color opacity is adjusted by using the opacityValue. 

The **opacityValue** property is Number type and its default value is 10.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

   $(function () {

        var colorSample = new ej.ColorPicker($("#colorpick"), {

                  value: "#278787", 
                  opacityValue: 40
       });
    });

{% endhighlight %}

The following screenshot displays the output of the above code example.

![](Configure-Values_images/Configure-Values_img1.png) 

## button and tooltipText

### buttonText

The **ColorPicker** control allows you to define the text to be displayed in button elements. You can specify the text by using **buttonText** property. In **ColorPicker** control, popup contains two button elements “Apply” and “Cancel”.

To configure the **buttonText** property for the button elements, use the corresponding default values listed in the following table.

List of Button elements

<table>
    <tr>
        <th>
            Element</th>
        <th>
            Default value</th>
    </tr>
    <tr>
        <td>
            apply
        </td>
        <td>
            Apply
        </td>
    </tr>
    <tr>
        <td>
            cancel
        </td>
        <td>
            Cancel
        </td>
    </tr>
</table>

### tooltipText

The **ColorPicker** control consists of more number of sub controls and elements. To provide some information about each element and sub control, you can use the tooltip concept and you can achieve this by using **tooltipText** property.

To configure the **tooltipText,** use the following listed elements and its corresponding default value.

List of Tooltip elements

<table>
    <tr>
        <th>
            Element</th>
        <th>
            Default value</th>
    </tr>
    <tr>
        <td>
            switcher
        </td>
        <td>
            Switcher
        </td>
    </tr>
    <tr>
        <td>
            addbutton
        </td>
        <td>
            Add Color
        </td>
    </tr>
    <tr>
        <td>
            basic
        </td>
        <td>
            Basic
        </td>
    </tr>
    <tr>
        <td>
            monochrome
        </td>
        <td>
            Mono Chrome
        </td>
    </tr>
    <tr>
        <td>
            flatcolors
        </td>
        <td>
            Flat Colors
        </td>
    </tr>
    <tr>
        <td>
            seawolf
        </td>
        <td>
            Sea Wolf
        </td>
    </tr>
    <tr>
        <td>
            webcolors
        </td>
        <td>
            Web Colors
        </td>
    </tr>
    <tr>
        <td>
            sandy
        </td>
        <td>
            Sandy
        </td>
    </tr>
    <tr>
        <td>
            pinkshades
        </td>
        <td>
            Pink Shades
        </td>
    </tr>
    <tr>
        <td>
            misty
        </td>
        <td>
            Misty
        </td>
    </tr>
    <tr>
        <td>
            vintage
        </td>
        <td>
            Vintage
        </td>
    </tr>
    <tr>
        <td>
            moonlight
        </td>
        <td>
            Moon Light
        </td>
    </tr>
    <tr>
        <td>
            candycrush
        </td>
        <td>
            Candy Crush
        </td>
    </tr>
    <tr>
        <td>
            currentcolor
        </td>
        <td>
            Current Color
        </td>
    </tr>
    <tr>
        <td>
            selectedcolor
        </td>
        <td>
            Selected Color
        </td>
    </tr>
    <tr>
        <td>
            citrus
        </td>
        <td>
            Citrus
        </td>
    </tr>
</table>


When it is necessary to set the button text and tooltipText values in **Spanish** culture, the **ColorPicker** allow you to define the culture values to **buttonText** and **tooltipText** property. The following section explains on how to define the Spanish culture values to **ColorPicker** control.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget.

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
            value: "#278787",
            //spanish culture values
            buttonText: { apply: "aplicar ", cancel: "cancelar" }, tooltipText: { sandy: "arenoso" }
        });
    });

{% endhighlight %}


The following screenshot displays the output of the above code example.

![](Configure-Values_images/Configure-Values_img2.png) 

