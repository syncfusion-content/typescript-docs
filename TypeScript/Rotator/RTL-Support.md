---
layout: post
title: RTL-Support
description: rtl support
platform: typescript
control: Rotator
documentation: ug
---

# RTL Support

This feature supports to change the left-to-right alignment of the **Rotator** to right-to-left (RTL). (I.e.) Sets the **Rotator** to do its actions from right to left. The property **enableRTL** sets the **Rotator** from right to left. The value set to this property is **boolean** type.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: 500, 
            enableRTL: true 
        });
    });
}
{% endhighlight %}



