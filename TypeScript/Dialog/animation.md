---
layout: post
title: Animation in Dialog 
description: How to apply animation effects.
platform: typescript
control: Dialog
documentation: ug
keywords : ejdialog
---

# Animation

The Dialog widget can be animated while opening and closing the dialog.

We can specify the effect and the duration for the animation. There are two types of effects. They are slide and fade. We can configure these settings separately for open and close dialog actions.

{% highlight javascript %}

            //create dialog widget
/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module DialogComponent {
    $(function () {
        var dialogInstance = new ej.Dialog($("#dialog"), {
                showOnInit: false,
                actionButtons: ["close", "maximize", "minimize", "collapsible"],
                enableAnimation: true,
                animation: {
                    //animation settings while opening the dialog
                    show: {
                        effect: "slide",
                        duration: 500
                    },
                    //animation settings while closing the dialog
                    hide: {
                        effect: "fade",
                        duration: 500
                    }
                }
            });
    });
}    

{% endhighlight %}

![](animation_images\animation_img1.png)

