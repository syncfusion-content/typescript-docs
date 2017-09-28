---
layout: post
title: Customization
description: customization
platform: TypeScript
control: GroupButton
documentation: ug
---

# Customization

## Size

GroupButton component size can be varied based on the Size property values. Size is the enum type API and it is has the following Built-in values

List of predefined button size

<table>
<tr>
<th>
Button Types<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
Normal<br/><br/></td><td>
Creates GroupButton with content size.<br/><br/></td></tr>
<tr>
<td>
Mini<br/><br/></td><td>
Creates GroupButton with Built-in mini size height, width specified.<br/><br/></td></tr>
<tr>
<td>
Small<br/><br/></td><td>
Creates GroupButton with Built-in small size height, width specified.<br/><br/></td></tr>
<tr>
<td>
Medium<br/><br/></td><td>
Creates GroupButton with Built-in medium size height, width specified.<br/><br/></td></tr>
<tr>
<td>
Large<br/><br/></td><td>
Creates GroupButton with Built-in large size height, width specified.<br/><br/></td></tr>
</table>

## Set Dimension

By default GroupButton has standard height and width. You can change this height and width by using height and width property respectively. 

{% highlight js %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "checkbox",

                width: "300px",

                height: "50px",

                selectedItemIndex: [0]

            });
    });
}


{% endhighlight %}

![](Customization_images/Customization_img1.jpeg)


## ContentType

The content of the **Button** items in GroupButton can have a text and images. GroupButton provides the some predefined contentType options to easily customize the appearance of each button associated with GroupButton component without any complex CSS tricks. **GroupButton** items supports the following content types.

List of content types for button

<table>
<tr>
<th>
Content Types<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
textOnly<br/><br/></td><td>
Supports only for text content only.<br/><br/></td></tr>
<tr>
<td>
imageOnly<br/><br/></td><td>
Supports only for image content only<br/><br/></td></tr>
<tr>
<td>
imageBoth<br/><br/></td><td>
Supports image for both ends of the button.<br/><br/></td></tr>
<tr>
<td>
textAndImage<br/><br/></td><td>
Supports image with the text content.<br/><br/></td></tr>
<tr>
<td>
imageTextImage<br/><br/></td><td>
Supports image with both ends and middle in text.<br/><br/></td></tr>
</table>


## Icons

GroupButton has the option to add the icons to button elements which enhance the appearance. Icons inside the button can be added easily using **prefixIcon** and **suffixIcon** fields with dataSource property. GroupButton control also supports the Built-in icon libraries. The ej.widgets.core.min.css contains definitions for important icons that can be used in buttons. You can get the details about available icons with that corresponding class from [here](https://help.syncfusion.com/js/icon/ej-icons). 

Simply you can use these Built-in icons by mentioning the icon class name as value in **prefixIcon** and **suffixIcon** property. You can use any font icons that are defined in ej.widgets.core.min.css. It avoids the complexity in specifying icon using sprite image and CSS.

{% highlight html %}

        <div class="element">

            <div id="groupButton">

            </div>

        </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "checkbox",

                dataSource: [

                { contentType: "imageonly", prefixIcon: "e-icon e-bold_01" },

                { contentType: "imageonly", prefixIcon: "e-icon e-italic_01" },

                { contentType: "imageonly", prefixIcon: "e-icon e-underline_01" }],

                showRoundedCorner: true,

                width: "170px",

                selectedItemIndex: [0, 2]

            });

    });
} 

{% endhighlight %}

![](Customization_images/Customization_img2.jpeg)


## Orientation

GroupButton has two Built-in orientation support called vertical and horizontal orientations which defines the direction of rendered GroupButton component. You can set the value to this property as enum or string type.

 * ej.Orientation.Horizontal or “Horizontal”
 * ej.Orientation.Vertical or “Vertical”

{% highlight js %}



/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "checkbox",

                orientation: ej.Orientation.Vertical,

                selectedItemIndex: [1]

            });
    });
}  

{% endhighlight %}

![](Customization_images/Customization_img3.jpeg)


