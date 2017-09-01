---
layout: post
title: Responsive-Layout
description: responsive layout
platform: TypeScript
control: Toolbar
documentation: ug
---

# Responsive Layout

**Responsive Layout** is aimed at crafting sites to provide an optimal viewing experience easy reading and navigation with a minimum of resizing, panning, and scrolling—across a wide range of devices (from mobile phones to desktop computer monitors). You can achieve **Responsive Layout** by using default functionality of **Toolbar** with **isResponsive** as **true** and also you need to give **Toolbar** width as in percentage value and add **ej.responsive.css** file in this sample. **CDN** link for the responsive CSS file is as follows.

[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css)

Add the above **css** link in the code sample.        

Add the following code example in your **HTML** page.

{% highlight html %}

    <div class="control">
        <!—list of toolbar items-->
        <div id="ToolbarItem">
            <ul>
                <li id="OtherFormat" title="Convert PDF files to Word or Excel Online..">
                    <div class="PdfDocument e-icon convertToOthers "></div>
                </li>
                <li id="PDFOnline" title="Convert files to PDF Online">
                    <div class="PdfDocument e-icon convertToPdf "></div>
                </li>
                <li id="Signature" title="Sign, add text or send a document for signature">
                    <div class=" PdfDocument e-icon signature "></div>
                </li>
                <li id="Save" title="Save file ( Ctrl+S )">
                    <div class=" PdfDocument e-icon save "></div>
                </li>
                <li id="Print" title="Print file ( Ctrl+P ) ">
                    <div class=" PdfDocument e-icon print "></div>
                </li>
                <li id="Message" title="Message">
                    <div class=" PdfDocument e-icon msg "></div>
                </li>
            </ul>
            <ul>
                <li id="Previous" title="Show previous page ( Left Arrow )">
                    <div class=" PdfDocument e-icon previous "></div>
                </li>
                <li id="Next" title="Show next page ( Right Arrow )">
                    <div class="PdfDocument e-icon next "></div>
                </li>
                <li id="page">
                    <div class="PdfDocument">
                        <input type="text" value="1" />
                    </div>
                </li>
                <li id="count">
                    <span>/ 1</span>
                </li>
            </ul>
            <ul>
                <li id="ZoomOut" title="Zoom Out">
                    <div class=" PdfDocument e-icon zoomOut "></div>
                </li>
                <li id="ZoomIn" title="Zoom In">
                    <div class=" PdfDocument e-icon zoomIn "></div>
                </li>
                <li id="ZoomValue">
                    <div class=" PdfDocument">
                        <input type="text" id="selectPercent" />
                    </div>
                </li>
            </ul>
            <ul>
                <li id="FitFull" title="Fit one full page to window">
                    <div class=" PdfDocument e-icon fitOne "></div>
                </li>
                <li id="StickyNote" title="Add stick note ( Ctrl+6 ) ">
                    <div class=" PdfDocument e-icon sticky "></div>
                </li>
                <li id="ReadMode" title="View File in Read Mode">
                    <div class=" PdfDocument e-icon readMode "></div>
                </li>
            </ul>
        </div>
    </div>

{% endhighlight %}

{% highlight css %}

<style type="text/css" class="cssStyles">
    .e-tooltxt .PdfDocument.e-icon {
        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon.png');
        background-repeat: no-repeat;
        display: block;
        height: 30px;
        width: 30px;
    }

    .e-tooltxt .PdfDocument.e-icon:hover {
        background-image: url('http://js.syncfusion.com/UG/Web/Content/pdf-icon-white.png');
    }

    .PdfDocument.e-icon.convertToOthers {
        background-position: -349px 0px;
    }

    .PdfDocument.e-icon.convertToPdf {
        background-position: -527px 0px;
    }

    .PdfDocument.e-icon.signature {
        background-position: 2px 0px;
    }

    .PdfDocument.e-icon.save {
        background-position: -87px 0px;
    }

    .PdfDocument.e-icon.msg {
        background-position: -483px 0px;
    }

    .PdfDocument.e-icon.previous {
        background-position: -395px 0px;
    }

    .PdfDocument.e-icon.next {
        background-position: -439px 0px;
    }

    .PdfDocument.e-icon.zoomIn {
        background-position: -175px 0px;
    }

    .PdfDocument.e-icon.zoomOut {
        background-position: -219px 0px;
    }

    .PdfDocument.e-icon.fitOne {
        background-position: -264px 0px;
    }

    .PdfDocument.e-icon.sticky {
        background-position: -131px -1px;
    }

    .PdfDocument.e-icon.readMode {
        background-position: -308px 0px;
    }

    .PdfDocument.e-icon.print {
        background-position: -43px 0px;
    }

    #ZoomValue .PdfDocument {
        width: 90px;
    }

    #page .PdfDocument input {
        text-align: center;
        width: 20px;
        height: 21px;
    }

    #count span {
        width: 30px;
        height: 30px;
        position: relative;
        top: 2px;
        text-align: center;
        vertical-align: middle;
    }
</style>

{% endhighlight %}

{% highlight js %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ToolbarComponent {
    $(function () {
        var sample = new ej.Toolbar($("#ToolbarItem"),{
            width: "600px", // width of the Toolbar
            height: "33px", // height of the Toolbar
            isResponsive: true // responsive support for toolbar
        });
        var percentList = ["10%", "25%", "50%", "100%", "400%", "800%", "1600%", "3200%", "6400%"];
        var sample1 = new ej.DropDownList($("#selectPercent"),{
            width: "90px",
            height: "27px",
            dataSource: percentList, // Assign List of Dropdown value to data Source
            value: "100%" // Initialize drop down value.
        });
    });
}
{% endhighlight %}

Execute the above code to render the following output.

![](Responsive-Layout_images/Responsive-Layout.png)


## responsiveType:Inline

We can set the responsiveType property to inline to display the overflown toolbar items as inline toolbar.

{% highlight js %}

    $(function () {
        var sample = new ej.Toolbar($("#ToolbarItem"),{
            width: "600px", // width of the Toolbar
            isResponsive: true // responsive support for toolbar
            responsiveType:"inline"//responsive Type API to display overflow items as inline toolbar.
        });
      
    });

{% endhighlight %}


While setting inline responsiveType the following output will be displayed.

![](Responsive-Layout_images/Responsive-Layout-img2.png)

## responsiveType:Popup

We can set the responsiveType property to popup to display the overflown toolbar items as popup.

{% highlight js %}

    $(function () {
         var sample = new ej.Toolbar($("#ToolbarItem"),{
            width: "600px", // width of the Toolbar
            height: "33px", // height of the Toolbar
            isResponsive: true // responsive support for toolbar
            responsiveType:"popup"//responsive Type API to display overflow items as popup.
        });
      
    });

{% endhighlight %}


While setting popup as responsiveType the  following output will be displayed.

![](Responsive-Layout_images/Responsive-Layout.png)