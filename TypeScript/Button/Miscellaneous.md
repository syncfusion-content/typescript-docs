---
layout: post
title: Miscellaneous
description: miscellaneous
platform: TypeScript
control: Button
documentation: ug
---

# Miscellaneous

## Text

You can display the user defined text for **Button**. Using **text** property, you can easily set text content for button. This text property overwrites the text that is provided on input button element.

The following steps explains you the details about rendering the button with specified text.

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

   <button id="button_text">button</button>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#button_text"), {
            size: "mini",
            //used to set the text content for button
            text: "Enter"
        });
    });
} 

{% endhighlight %}

In the above code, the content of button “button” is replaced by the text value “Enter” that is given using text property.

Execute the above code to render the following output.

![](Miscellaneous_images/Miscellaneous_img1.png) 

## Show Rounded Corner

Specifies the corner of button in round shape. By default button doesn’t have rounded corner. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the button with rounded corner.

In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

   <button id="button_roundedCorner">button</button>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#button_roundedCorner"), {
            size: "mini",
            //Enable or disable the rounded corner for button
            showRoundedCorner: true
        });
    });
}
{% endhighlight %}

Execute the above code to render the following output.

![](Miscellaneous_images/Miscellaneous_img2.png) 



