---
layout: post
title: TypeScript Icons Library | Syncfusion
description: Learn here all about introduction of Syncfusion Essential TypeScript Icons Library, its elements, and more.
platform: TypeScript
control: Button
documentation: ug
---

# TypeScript Icons Library

The **Essential Studio for JavaScript** provide icons library that contains the number of in-built icons that can be applied for CSS class names to elements and refer “ej.widgets.all.core.min.css” file. Use the following syntax to apply class names.

**Syntax**: .e-icon .e-[icon description]

{% highlight html %}

.e-icon .e-search

{% endhighlight %}

## Adding icon in Button

For example, you can render the desired icon in the button by using the following table that contains the listed icons CSS class names in the “prefixIcon” property of button component. Also, use “contentType” property to display the icon in the button. In the following code example, specify the “**ContentType**” of the button as imageonly.    

Refer to the following link to know what are the values passed in the “**ContentType**” property

<https://help.syncfusion.com/api/js/global#members:contenttype>


Also in the button sample, you can use the icon class names as follows,

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#buttonId"), {
        contentType: "imageonly",
        prefixIcon: "e-icon e-handup"
    });
 }); 
}

{% endhighlight %}

Execute the above code to render the following output.

![Icons_images1](Icons_images/Icons_img1.png)

Icon library used in button component
{:.caption}

## List of Icons

The complete list of icons is listed in the following table.

List of icons

<table>
    <tr>
        <td>
            e-unpin
        </td>
        <td>
            <img src="Icons_images\Icons_img2.png" alt="Icons_images2" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-pin
        </td>
        <td>
            <img src="Icons_images\Icons_img3.png" alt="Icons_images3" width="14pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-upload
        </td>
        <td>
            <img src="Icons_images\Icons_img4.png" alt="Icons_images4" width="17pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-reload
        </td>
        <td>
            <img src="Icons_images\Icons_img5.png" alt="Icons_images5" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-collapse
        </td>
        <td>
            <img src="Icons_images\Icons_img6.png" alt="Icons_images6" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-cancel
        </td>
        <td>
            <img src="Icons_images\Icons_img7.png" alt="Icons_images7" width="15pt" height="18pt">
        </td>
    </tr>
    <tr>
        <td>
            e-expand
        </td>
        <td>
            <img src="Icons_images\Icons_img8.png" alt="Icons_images8" width="16pt" height="10pt">
        </td>
    </tr>
    <tr>
        <td>
            e-minimize
        </td>
        <td>
            <img src="Icons_images\Icons_img9.png" alt="Icons_images9" width="16pt" height="10pt">
        </td>
    </tr>
    <tr>
        <td>
            e-login
        </td>
        <td>
            <img src="Icons_images\Icons_img10.png" alt="Icons_images10" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-orientationlanscape
        </td>
        <td>
            <img src="Icons_images\Icons_img11.png" alt="Icons_images11" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-alignleft
        </td>
        <td>
            <img src="Icons_images\Icons_img12.png" alt="Icons_images12" width="15pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-aligncenter
        </td>
        <td>
            <img src="Icons_images\Icons_img13.png" alt="Icons_images13" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-alignright
        </td>
        <td>
            <img src="Icons_images\Icons_img14.png" alt="Icons_images14" width="15pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-alignjustify
        </td>
        <td>
            <img src="Icons_images\Icons_img15.png" alt="Icons_images15" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-alignnone
        </td>
        <td>
            <img src="Icons_images\Icons_img16.png" alt="Icons_images16" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-filterset
        </td>
        <td>
            <img src="Icons_images\Icons_img17.png" alt="Icons_images17" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-filternone
        </td>
        <td>
            <img src="Icons_images\Icons_img18.png" alt="Icons_images18" width="11pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheadup-2x
        </td>
        <td>
            <img src="Icons_images\Icons_img19.png" alt="Icons_images19" width="14pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheaddown-2x
        </td>
        <td>
            <img src="Icons_images\Icons_img20.png" alt="Icons_images20" width="12pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheadleft-2x
        </td>
        <td>
            <img src="Icons_images\Icons_img21.png" alt="Icons_images21" width="10pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheadright-2x
        </td>
        <td>
            <img src="Icons_images\Icons_img22.png" alt="Icons_images22" width="10pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-numbering
        </td>
        <td>
            <img src="Icons_images\Icons_img23.png" alt="Icons_images23" width="14pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-bullets
        </td>
        <td>
            <img src="Icons_images\Icons_img24.png" alt="Icons_images24" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-maximize
        </td>
        <td>
            <img src="Icons_images\Icons_img25.png" alt="Icons_images25" width="13pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-delete
        </td>
        <td>
            <img src="Icons_images\Icons_img26.png" alt="Icons_images26" width="12pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-scroll
        </td>
        <td>
            <img src="Icons_images\Icons_img27.png" alt="Icons_images27" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-right-scroll
        </td>
        <td>
            <img src="Icons_images\Icons_img28.png" alt="Icons_images28" width="16pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-search
        </td>
        <td>
            <img src="Icons_images\Icons_img29.png" alt="Icons_images29" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaback
        </td>
        <td>
            <img src="Icons_images\Icons_img30.png" alt="Icons_images30" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaforward
        </td>
        <td>
            <img src="Icons_images\Icons_img31.png" alt="Icons_images31" width="11pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-medianext
        </td>
        <td>
            <img src="Icons_images\Icons_img32.png" alt="Icons_images32" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaprev
        </td>
        <td>
            <img src="Icons_images\Icons_img33.png" alt="Icons_images33" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaeject
        </td>
        <td>
            <img src="Icons_images\Icons_img34.png" alt="Icons_images34" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaclose
        </td>
        <td>
            <img src="Icons_images\Icons_img35.png" alt="Icons_images35" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediapause
        </td>
        <td>
            <img src="Icons_images\Icons_img36.png" alt="Icons_images36" width="12pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-mediaplay
        </td>
        <td>
            <img src="Icons_images\Icons_img37.png" alt="Icons_images37" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-righttick
        </td>
        <td>
            <img src="Icons_images\Icons_img38.png" alt="Icons_images38" width="15pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-smile
        </td>
        <td>
            <img src="Icons_images\Icons_img39.png" alt="Icons_images39" width="16pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-information
        </td>
        <td>
            <img src="Icons_images\Icons_img40.png" alt="Icons_images40" width="16pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-left-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img41.png" alt="Icons_images41" width="12pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-right-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img42.png" alt="Icons_images42" width="10pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-file-delete
        </td>
        <td>
            <img src="Icons_images\Icons_img43.png" alt="Icons_images43" width="12pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-file-percentage-success
        </td>
        <td>
            <img src="Icons_images\Icons_img44.png" alt="Icons_images44" width="15pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-file-cancel
        </td>
        <td>
            <img src="Icons_images\Icons_img45.png" alt="Icons_images45" width="11pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-file-percentage-failed
        </td>
        <td>
            <img src="Icons_images\Icons_img46.png" alt="Icons_images46" width="11pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-file-retry
        </td>
        <td>
            <img src="Icons_images\Icons_img47.png" alt="Icons_images47" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-resize-handle
        </td>
        <td>
            <img src="Icons_images\Icons_img48.png" alt="Icons_images48" width="12pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-down-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img49.png" alt="Icons_images49" width="14pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-time
        </td>
        <td>
            <img src="Icons_images\Icons_img50.png" alt="Icons_images50" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-up-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img51.png" alt="Icons_images51" width="12pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-date
        </td>
        <td>
            <img src="Icons_images\Icons_img52.png" alt="Icons_images52" width="14pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-datetime
        </td>
        <td>
            <img src="Icons_images\Icons_img53.png" alt="Icons_images53" width="16pt" height="18pt">
        </td>
    </tr>
    <tr>
        <td>
            e-collapse-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img54.png" alt="Icons_images54" width="13pt" height="11pt">
        </td>
    </tr>
    <tr>
        <td>
            e-expand-arrow
        </td>
        <td>
            <img src="Icons_images\Icons_img55.png" alt="Icons_images55" width="12pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-restore
        </td>
        <td>
            <img src="Icons_images\Icons_img56.png" alt="Icons_images56" width="16pt" height="19pt">
        </td>
    </tr>
    <tr>
        <td>
            e-plus
        </td>
        <td>
            <img src="Icons_images\Icons_img57.png" alt="Icons_images57" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-minus
        </td>
        <td>
            <img src="Icons_images\Icons_img58.png" alt="Icons_images58" width="16pt" height="10pt">
        </td>
    </tr>
    <tr>
        <td>
            e-handup
        </td>
        <td>
            <img src="Icons_images\Icons_img59.png" alt="Icons_images59" width="12pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-clock
        </td>
        <td>
            <img src="Icons_images\Icons_img60.png" alt="Icons_images60" width="13pt" height="11pt">
        </td>
    </tr>
    <tr>
        <td>
            e-cursor
        </td>
        <td>
            <img src="Icons_images\Icons_img61.png" alt="Icons_images61" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-hyperlink
        </td>
        <td>
            <img src="Icons_images\Icons_img62.png" alt="Icons_images62" width="20pt" height="12pt">
        </td>
    </tr>
    <tr>
        <td>
            e-hyperlinkbreak
        </td>
        <td>
            <img src="Icons_images\Icons_img63.png" alt="Icons_images63" width="20pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-settings
        </td>
        <td>
            <img src="Icons_images\Icons_img64.png" alt="Icons_images64" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-shoppingcart
        </td>
        <td>
            <img src="Icons_images\Icons_img65.png" alt="Icons_images65" width="16pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-palette
        </td>
        <td>
            <img src="Icons_images\Icons_img66.png" alt="Icons_images66" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-warningmessage
        </td>
        <td>
            <img src="Icons_images\Icons_img67.png" alt="Icons_images67" width="15pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-cut
        </td>
        <td>
            <img src="Icons_images\Icons_img68.png" alt="Icons_images68" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-copy
        </td>
        <td>
            <img src="Icons_images\Icons_img69.png" alt="Icons_images69" width="14pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-paste
        </td>
        <td>
            <img src="Icons_images\Icons_img70.png" alt="Icons_images70" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-edit
        </td>
        <td>
            <img src="Icons_images\Icons_img71.png" alt="Icons_images71" width="18pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-swapleft
        </td>
        <td>
            <img src="Icons_images\Icons_img72.png" alt="Icons_images72" width="16pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-swapright
        </td>
        <td>
            <img src="Icons_images\Icons_img73.png" alt="Icons_images73" width="16pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-swapup
        </td>
        <td>
            <img src="Icons_images\Icons_img74.png" alt="Icons_images74" width="16pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-swapdown
        </td>
        <td>
            <img src="Icons_images\Icons_img75.png" alt="Icons_images75" width="16pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-zoomin
        </td>
        <td>
            <img src="Icons_images\Icons_img76.png" alt="Icons_images76" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-zoomout
        </td>
        <td>
            <img src="Icons_images\Icons_img77.png" alt="Icons_images77" width="16pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-star
        </td>
        <td>
            <img src="Icons_images\Icons_img78.png" alt="Icons_images78" width="12pt" height="11pt">
        </td>
    </tr>
    <tr>
        <td>
            e-home
        </td>
        <td>
            <img src="Icons_images\Icons_img79.png" alt="Icons_images79" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-clipboard
        </td>
        <td>
            <img src="Icons_images\Icons_img80.png" alt="Icons_images80" width="14pt" height="18pt">
        </td>
    </tr>
    <tr>
        <td>
            e-userlogin
        </td>
        <td>
            <img src="Icons_images\Icons_img81.png" alt="Icons_images81" width="15pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-dataexport
        </td>
        <td>
            <img src="Icons_images\Icons_img82.png" alt="Icons_images82" width="19pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheadright
        </td>
        <td>
            <img src="Icons_images\Icons_img83.png" alt="Icons_images83" width="14pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-arrowheaddown
        </td>
        <td>
            <img src="Icons_images\Icons_img84.png" alt="Icons_images84" width="13pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-undo
        </td>
        <td>
            <img src="Icons_images\Icons_img85.png" alt="Icons_images85" width="13pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-redo
        </td>
        <td>
            <img src="Icons_images\Icons_img86.png" alt="Icons_images86" width="16pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-bold
        </td>
        <td>
            <img src="Icons_images\Icons_img87.png" alt="Icons_images87" width="14pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-italic
        </td>
        <td>
            <img src="Icons_images\Icons_img88.png" alt="Icons_images88" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-underline
        </td>
        <td>
            <img src="Icons_images\Icons_img89.png" alt="Icons_images89" width="17pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-strikethrough
        </td>
        <td>
            <img src="Icons_images\Icons_img90.png" alt="Icons_images90" width="16pt" height="14pt">
        </td>
    </tr>
    <tr>
        <td>
            e-font
        </td>
        <td>
            <img src="Icons_images\Icons_img91.png" alt="Icons_images91" width="15pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-rarrowdown
        </td>
        <td>
            <img src="Icons_images\Icons_img92.png" alt="Icons_images92" width="11pt" height="13pt">
        </td>
    </tr>
    <tr>
        <td>
            e-rarrowleft
        </td>
        <td>
            <img src="Icons_images\Icons_img93.png" alt="Icons_images93" width="16pt" height="15pt">
        </td>
    </tr>
    <tr>
        <td>
            e-rarrowup
        </td>
        <td>
            <img src="Icons_images\Icons_img94.png" alt="Icons_images94" width="14pt" height="11pt">
        </td>
    </tr>
    <tr>
        <td>
            e-rarrowright
        </td>
        <td>
            <img src="Icons_images\Icons_img95.png" alt="Icons_images95" width="14pt" height="16pt">
        </td>
    </tr>
    <tr>
        <td>
            e-calender
        </td>
        <td>
            <img src="Icons_images\Icons_img96.png" alt="Icons_images96" width="14pt" height="17pt">
        </td>
    </tr>
    <tr>
        <td>
            e-save
        </td>
        <td>
            <img src="Icons_images\Icons_img97.png" alt="Icons_images97" width="17pt" height="16pt">
        </td>
    </tr>
</table>