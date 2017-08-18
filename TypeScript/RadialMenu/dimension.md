---
layout: post
title: radius
description: radius
platform: Typescript
control: RadialMenu
documentation: ug
---

## Dimension

You can customize **Radial Menu** dimension by using **radius** and **position** properties.

### Radius

You can customize the **Radial Menu** size by using the **radius** property. By default, the **Radial Menu** radius is set as 150px. Refer to the following code example.

{% highlight html %}

    <!-- RTE code for setting target for Radial menu -->

    <div id="defaultradialmenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f1.png" data-ej-text="Italic"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/align.png" data-ej-text="Align"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/sort.png" data-ej-text="Sort"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RadialMenuComponent {
        $(function () {
            var radialmenuInstance = new ej.RadialMenu($("#defaultradialmenu"), {
                 radius: "200"
                 });
        });
        
        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });
    } 

{% endhighlight %}


The following screenshot illustrates the **Radial Menu** while clicking on the settings icon.

![](dimension-images\dimension_img2.png)

### Position 

To display the **Radial Menu** in the web page in a specific area, we can use the **position** property. By default, the **Radial Menu** position is set as null. 

Refer to the following code example.

{% highlight html %}

        <ul>
        
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo"></li>

        </ul>

{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
            var radialmenuInstance = new ej.RadialMenu($("#defaultradialmenu"), {
                 radius: "200",
                 position:{x:10,y:10}
            });
        });
        
        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");

        });

{% endhighlight %}



The following screenshot illustrates the output while selecting the text in the page.

![](dimension-images\dimension_img4.png)