---
layout: post
title: RTL-Support
description: rtl support
platform: TypeScript
control: Button
documentation: ug
---

# RTL Support

In some cases you can use right to left alignment. Here, RTL support is provided using **enableRTL** property. In RTL mode when you have more than one content (image/text, image/image) in button, then these content are aligned in right to left format. For example, when text is in left and image is in right position, after applying right to left alignment these position are interchanged.

The following steps explains the details about rendering the button with Right to left alignment support.

In the **HTML** page, add the following button elements to configure button widget.

{% highlight html %}

   <button id="button_rtl">button</button>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        $("#button_rtl").ejButton({
            size: "large", contentType: ej.ContentType.TextAndImage,
            showRoundedCorner: true,
            prefixIcon: "e-icon e-login",
            //used to enable or disable RTL support for button
            enableRTL: true
        });
    });

{% endhighlight %}

In above mentioned code example prefixIcon property is used and the icon that is to be on left side, (before text) is rendered on right side as enableRTL property is used with prefixIcon.  Consequently, the alignment is changed in right to left order.

Execute the above code to render the following output.

![](RTL-Support_images/RTL-Support_img1.png) 

