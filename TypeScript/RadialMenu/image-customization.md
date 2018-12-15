---
layout: post
title: Syncfusion Radial Menu Image Customization
description: image customization
platform: Typescript
control: RadialMenu
documentation: ug
---

## Image Customization

You can customize the **Radial Menu’s** Center and Back images by using the **ImageClass** and **BackImageClass** properties. Every menu item can be added with image using **url** property. By using this **data-ej-imageClass** attribute, you can customize the **Radial Menu** center image. 

Sub-Items are also supported in the **Radial Menu**. To navigate Sub-Items, click the arrows in the outer ring and it displays the corresponding sub-items group. Clicking the center button when a sub-items group is shown, displays the items on the previous level. Nested **Radial Menu** has the second level back button. In this case, you can use the **data-ej-backImageClass** attribute to change your second level back button. **BackImageClass** is used to customize the **nestedRadialMenu** back image. Refer to the following code example.

You can add the page content with text-area by referring to this section.

{% highlight html %}


    <div id="nestedRadialMenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Font">
                <ul>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f1.png" data-ej-text="Italic"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f2.png" data-ej-text="Bold"></li>
                </ul>
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/table.png" data-ej-text="Table"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/list.png" data-ej-text="List">
                <ul>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l1.png" data-ej-text="List"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l2.png" data-ej-text="List"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l3.png" data-ej-text="List"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l4.png" data-ej-text="List"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/l5.png" data-ej-text="List"></li>
                </ul>
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste">
                <ul>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/c1.png" data-ej-text="Paste"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/c2.png" data-ej-text="Paste"></li>

                </ul>
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/sort.png" data-ej-text="Sort">
                <ul>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/s1.png" data-ej-text="Sort"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/s2.png" data-ej-text="Sort"></li>

                </ul>
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/align.png" data-ej-text="Alignment">
                <ul>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a1.png" data-ej-text="Left"></li>
                    <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/a2.png" data-ej-text="Right"></li>

                </ul>
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/draw.png" data-ej-text="Draw"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
          var radialMenuInstance = new ej.RadialMenu($("#nestedRadialMenu"), {
                imageClass: "imageClass",
                 backImageClass: "backImageClass" });
        });
        
        $("#rteSampleOne").select(function (e) {
            $('#nestedRadialMenu').ejRadialMenu("show");
        });
    
{% endhighlight %}

Add the following styles in your code.
    
{% highlight css %}

    <style type="text/css" class="cssStyles">
        .e-radialmenu .imageClass {
            background-image: url(http://js.syncfusion.com/UG/web/Content/radial/main.png);
        }

        .e-radialmenu .backImageClass {
            background-image: url(http://js.syncfusion.com/UG/web/Content/radial/Back_button.png);
        }
    </style>


{% endhighlight %}



The following screenshot illustrates the output.

![Image customizations](image-customization_images\image-customization_img1.png)

Radial Menu - Image Customization – Main menu
{:.caption}

When you click the arrow, it navigates to the child item as illustrated in the following screenshot.

![Radial Menu Image customizations](image-customization_images\image-customization_img2.png)

Radial Menu- Image Customization – Child menu 
{:.caption}



