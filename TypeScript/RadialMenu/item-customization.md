---
layout: post
title: item-customization
description: item customization
platform: Typescript
control: RadialMenu
documentation: ug
---

## Item Customization

You can customize individual **Radial Menu** items by using the items properties. 

### Adding image and text to RadialMenu items

The **data-ej-imageUrl** property specifies the URL of the image for the items. **data-ej-text** attribute is used to specify the item text. Refer to the following code example.

{% highlight html %}


    <div id="defaultradialmenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
                var radialmenuInstance = new ej.RadialMenu($("#defaultradialmenu"), {
                radius: "150"
             });
        });

        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });


{% endhighlight %}



The following screenshot illustrates the output.

![](item-customization_images\item-customization_img1.png)


### Adding events to Radial Menu items

You can specify the click event to corresponding image/text of **Radial Menu** items for performing some specific action. You need to handle the click event in script manually for each item click.

{% highlight html %}


    <div id="defaultradialmenu">

          <ul>
               <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy" data-ej-click="copy"></li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/Font_letter.png" data-ej-text="Font"></li>
                <li data-ej-imageurl=".http://js.syncfusion.com/UG/web/Content/radial/list.png" data-ej-text="List">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/list.png" data-ej-text="List"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l5.png" data-ej-text="List"></li>
                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold" data-ej-click="bold">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f1.png" data-ej-text="Italic" data-ej-click="italic"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold" data-ej-click="bold"></li>
                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo"data-ej-enabled="false">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo" data-ej-enabled="false"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo" data-ej-enabled="false"></li>

                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/align.png" data-ej-text="Alignment">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a1.png" data-ej-text="Left"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a2.png" data-ej-text="Right"></li>

                    </ul>
                </li>
            </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
             var radialmenuInstance = new ej.RadialMenu($("#defaultradialmenu"), {
                 radius: "150"
             });
        });

        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });
        function italic(e) {
            rteObj.executeCommand("italic");
        }
        function bold(e) {
            rteObj.executeCommand("bold");
        }
        function copy(e) {
            rteObj.executeCommand("copy");
        }


{% endhighlight %}


The following screenshot illustrates the output.

![](item-customization_images\item-customization_img2.png)


### Badge Customization in Radial Menu Items

You can specify set badges for the items by using badge settings in the radial menu. You can set value for the badge and enable badge with a default value.

The **data-ej-badge-enabled** property to enable or disable badges. **data-ej-badge-value** attribute is to set the badge value.

{% highlight html %}

  <div id="defaultradialmenu">
            
            <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy" data-ej-click="copyevent" data-ej-enabled="true" data-ej-badge-enabled="true" data-ej-badge-value="3"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo"></li>
        </ul>

{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
            $('#defaultradialmenu').ejRadialMenu();
        });

        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });       


{% endhighlight %}


The following screenshot illustrates the output.

![](item-customization_images\item-customization_img3.png)

### Slider support for Radial Menu Items

You can customize the Radial Menu with slider settings.The **data-ej-type** property specifies the type of radial menu item, where you can set the type for RadialMenu item.

You can customize the **Radial Menu** slider settings by using the **ticks**, **strokeWidth** and **labelSpace** properties. The **data-ej-sliderSettings-ticks** property specifies the slider ticks for radial menu item.**data-ej-sliderSettings-strokeWidth** attribute is used to specify the slider's stroke width value.**data-ej-sliderSettings-labelSpace** attribute is used to specify the value of slider label space.

Refer to the following code example.

{% highlight html %}

        <div id="radialslidermenu">

            <ul>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy" data-ej-click="copy"></li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/Font_letter.png" data-ej-text="Font" data-ej-click="font" data-ej-badge-value="2" data-ej-badge-enabled="true" data-ej-type="slider" data-ej-slidersettings-ticks="[0, 2, 4, 6, 8, 10, 12, 14]" data-ej-slidersettings-strokewidth="1"></li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/list.png" data-ej-text="List">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/list.png" data-ej-text="List"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l5.png" data-ej-text="List"></li>
                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f1.png" data-ej-text="Italic"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold"></li>
                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo" data-ej-enabled="false">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo" data-ej-enabled="false"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo" data-ej-enabled="false"></li>

                    </ul>
                </li>
                <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/align.png" data-ej-text="Alignment">
                    <ul>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a1.png" data-ej-text="Left"></li>
                        <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a2.png" data-ej-text="Right"></li>

                    </ul>
                </li>
            </ul>
        </div>

{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
         var radialmenuInstance = new ej.RadialMenu($("#radialslidermenu"), {
                radius: "150" 
                });
        });

        $("#rteSampleone").select(function (e) {
            $('#radialslidermenu').ejRadialMenu("show");
        });       


{% endhighlight %}

The following screenshot illustrates the output.

![](item-customization_images\item-customization_img4.png)