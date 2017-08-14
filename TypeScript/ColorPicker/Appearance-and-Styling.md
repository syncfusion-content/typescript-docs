---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: TypeScript
control: ColorPicker
documentation: ug
---

# Appearance and Styling

## modelType

The **ColorPicker** allows you to define the model type to be displayed in control at initial time by using the property **modelType**. 

The **modelType** property is Enum type and its default value is **default**.

List of modelType

<table>
    <tr>
        <th>
            ModelType</th>
        <th>
            Syntax</th>
        <th>
            Description</th>
    </tr>
    <tr>
        <td>
            Default
        </td>
        <td>
            modelType: ej.ColorPicker.ModelType.Default
        </td>
        <td>
            Control rendered with both model. You can switch to palette or picker model.
        </td>
    </tr>
    <tr>
        <td>
            Picker
        </td>
        <td>
            modelType: ej.ColorPicker.ModelType.Picker
        </td>
        <td>
            Control rendered with picker model only.
        </td>
    </tr>
    <tr>
        <td>
            Palette
        </td>
        <td>
            modelType: ej.ColorPicker.ModelType.Palette
        </td>
        <td>
            Control rendered with palette model only.
        </td>
    </tr>
</table>


In the following code example, the **ColorPicker** popup model type is set as **palette** when you drop down the **ColorPicker** popup.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ColorPickerComponent {
    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
             modelType: "palette",
              value: "#278787"
               });
    });
}

{% endhighlight %}

The following screenshot displays the output of the above code example.

![](Appearance-and-Styling_images/Appearance-and-Styling_img1.png)

## palette

The **ColorPicker** allow you to define the palette type to be displayed in control at initial time by using the **palette** property. The **palette** property is Enum type and its default value is **basicpalette**.

List of palette

<table>
    <tr>
        <th>
            Palette</th>
        <th>
            Syntax</th>
        <th>
            Description</th>
        <td>
            <b>Dependent Property</b>
        </td>
    </tr>
    <tr>
        <td>
            BasicPalette
        </td>
        <td>
            palette: ej.ColorPicker.Palette.BasicPalette
        </td>
        <td>
            The palette model rendered with predefined color values.
        </td>
        <td rowspan="2">
            modelType : ej.ColorPicker.ModelType.Palette
        </td>
    </tr>
    <tr>
        <td>
            CustomPalette
        </td>
        <td>
            palette: ej.ColorPicker.Palette.CustomPalette
        </td>
        <td>
            The palette model renders with the specified custom color values.
        </td>
    </tr>
</table>

## basicpalette

The **basicpalette** type renders with predefined color values. The **basicpalette** model has 12 different preset patterns. Each pattern consists of 50 colors and over 600 colors are available by default. 

**presetType**

The **ColorPicker** control allows you to define the preset model to be rendered initially in palette type. This can be achieved by using the “presetType” property. Totally 12 types of presets are available.

The **presetType** property is Enum type and its default value is “basic”.

Property Table

<table>
    <tr>
        <th>
            PresetType</th>
        <th>
            Syntax</th>
        <th>
            Dependent Property</th>
    </tr>
    <tr>
        <td>
            Basic
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Basic
        </td>
        <td rowspan="12">
            palette: ej.ColorPicker.Palette.BasicPalette
        </td>
    </tr>
    <tr>
        <td>
            MonoChrome
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.MonoChrome
        </td>
    </tr>
    <tr>
        <td>
            FlatColors
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.FlatColors
        </td>
    </tr>
    <tr>
        <td>
            SeaWolf
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.SeaWolf
        </td>
    </tr>
    <tr>
        <td>
            WebColors
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.WebColors
        </td>
    </tr>
    <tr>
        <td>
            Sandy
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Sandy
        </td>
    </tr>
    <tr>
        <td>
            PinkShades
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.PinkShades
        </td>
    </tr>
    <tr>
        <td>
            Misty
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Misty
        </td>
    </tr>
    <tr>
        <td>
            Citrus
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Citrus
        </td>
    </tr>
    <tr>
        <td>
            Vintage
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Vintage
        </td>
    </tr>
    <tr>
        <td>
            MoonLight
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.MoonLight
        </td>
    </tr>
    <tr>
        <td>
            CandyCrush
        </td>
        <td>
            presetType: ej.ColorPicker.PresetType.Candycrush
        </td>
    </tr>
</table>


In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
          modelType: "palette", 
          value: "#278787",
           presetType: "flatcolors"
            });
    });

{% endhighlight %}


The following screenshot displays the output of the above code example.

![](Appearance-and-Styling_images/Appearance-and-Styling_img2.png) 

## custompalette

The **ColorPicker** control allows you to define the custom colors in the palette model by using **palette** property. Custom palettes are created by passing a comma delimited string of **HEX** values or an array of colors in **custom** property. The custompalette model is only applicable when you set modelType as **palette**.

The **custompalette** property is a dependent property of **palette** and **modelType** property.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
            value: "#9999ff", palette: "custompalette", modelType: "palette",
            custom: ["ffffff", "ffccff", "ff99ff", "ff66ff", "ff33ff", "ff00ff", "ccffff", "ccccff", "cc99ff", "cc66ff", "cc33ff", "cc00ff", "99ffff", "99ccff", "9999ff", "9966ff", "9933ff", "9900ff", "ffffcc", "ffcccc"]
        });
    });

{% endhighlight %}

The following screenshot displays the output of the above code example.

![](Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 

## displayInline

The **ColorPicker** control allows you to embed the popup in the order of DOM element flow by using the **displayInline** property. Using **displayInline** property to make **ColorPicker** popup always in visible state. Also associate ColorPicker with &lt;div&gt; element instead of input. 

The **displayInline** property is Boolean type and its default value is false.

The following steps explain you how to get the **ColorPicker** popup in **DisplayInline** state.

In the **HTML** page, add a **&lt;div&gt;** element to render **ColorPicker** widget

{% highlight html %}


 <div id="colorPicker" ></div>    

{% endhighlight %}

{% highlight javascript %}

 
     $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
            value: "#278787",
            displayInline: true 
             });
    });

{% endhighlight %}

The following screenshot displays the output of the above code example.

![](Appearance-and-Styling_images/Appearance-and-Styling_img4.png) 

## Theme Support

The **ColorPicker** control supports rich appearance. It supports 12 different themes of **Essential JavaScript** and bootstrap themes. To use these twelve themes, refer the themes files in HTML page. 

You require two style sheets to apply styles to ColorPicker control; one ej.widgets.core.min.css and one ej.theme.min.css. When you use ej.widgets.all.min.css then, it is not necessary to use ej.widgets.core.min.css and ej.theme.min.css because ej.widgets.all.min.css is a combination of these two.

The core style sheet applies styles related to positioning and size, but are not related to the color scheme and always require the control to look correct and function properly. The theme style sheet applies theme-specific styles like colors and backgrounds.

The following list is the twelve themes supported by ColorPicker:

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark


In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget.


{% highlight html %}


<!doctype html>
<html>
<head>
    <title>Essential Studio for JavaScript : ColorPicker – Built-in Theme Support</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"   />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
</head>
<body>
    <div id="control">
        <input id="colorPicker" type="text" />
    </div>
    <script>
    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
                value: "#278787" 
                });
        });
    </script>
</body>
</html>


{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.
The following screenshot displays the output of the above code example.


![](Appearance-and-Styling_images/Appearance-and-Styling_img5.png)

## CustomCss

The **ColorPicker** control also allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds. To apply custom themes use the **cssClass** property. **cssClass** property sets the root class for **ColorPicker** theme.

Using this property you can override the existing styles under the theme style sheet. The theme style sheet applies theme-specific styles like colors and backgrounds. In the following example, the value of **cssClass** property is set as **Light-Blue**. **Light-Blue** is added as root class to **ColorPicker** control at the runtime. From this root class you can customize the **ColorPicker** control theme.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
    $(function () {
        var colorSample = new ej.ColorPicker($("#colorpick"), {
            value: "#278787", cssClass: "Light-Blue"
        });
    });

{% endhighlight %}


Custom CSS Styles.



{% highlight css %}

<style>
    .Light-Blue.e-colorwidget.e-widget, .Light-Blue.e-colorpicker.e-popup, .Light-Blue.e-colorwidget .e-in-wrap.e-box .e-select, .Light-Blue.e-colorwidget .e-in-wrap.e-box, .Light-Blue.e-colorwidget .e-down-arrow {
        background: none repeat scroll 0 0 lightblue;
    }

    .Light-Blue.e-colorpicker .e-footer .e-cancelButton.e-btn, .Light-Blue.e-colorpicker .e-footer .e-applyButton.e-btn {
        background: none repeat scroll 0 0 white;
    }
</style>


{% endhighlight %}



The following screenshot displays the output of above steps.

![](Appearance-and-Styling_images/Appearance-and-Styling_img6.png)

