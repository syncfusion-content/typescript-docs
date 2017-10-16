---
layout: post
title: RTL-support
description: rtl support
platform: TypeScript
control: Toggle Button
documentation: ug
---

# RTL support

In some cases, it is necessary to use right to left alignment. You can render **RTL** support by using **enableRTL** property. In **RTL** mode, when there is more than one content (image/text, image/image) in button, then the content is aligned in right to left format. For example, when text is in left and image is in right position, after applying right to left alignment these positions are interchanged.

The following steps explains you the details about rendering the **Toggle Button** with Right to left alignment support.

In the **HTML** page, add the following button elements to configure **Toggle Button** widget.

{% highlight html %}

<input type="checkbox" id="toggle_rtl" />

{% endhighlight %}

{% highlight html %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ToggleButtonComponent {
    $(function () {
        var button = new ej.ToggleButton($("#toggle_rtl"), {
                size: "small",
                imagePosition: "imageleft",
                contentType: "textandimage",
                showRoundedCorner: true,
                defaultText: "Play",
                activeText: "Next",
                defaultPrefixIcon: " e-icon e-mediaplay",
                activePrefixIcon: " e-icon e-mediapause",
                //used to enable or disable RTL support for toggle button
                enableRTL: true
            });
        });
}

{% endhighlight %}

In above mentioned code example **prefixIcon** property is used and the icon that is to be on left side, (before text) is rendered on right side as **enableRTL** property is used with **prefixIcon.**  Consequently, the alignment is changed in right to left order.

Output of above steps



![](RTL-support_images/RTL-support_img1.png) 


