---
layout: post
title: Action Buttons in Dialog 
description: How to enable the Interaction button like “Close”, “Minimize” and etc., in Dialog Widget. 
platform: typescript
control: Dialog
documentation: ug
keywords : ejdialog
---

# Action Buttons

The Dialog widget provides the following action buttons.

1. Close

2. Maximize

3. Minimize

4. Pin/Unpin

5. Collapse/Expand

You can display only the necessary buttons in the Dialog widget by configuring the `actionButtons` property.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DialogComponent {
    $(function () {
        var dialogInstance = new ej.Dialog($("#dialog"), {
                showOnInit: false,
                actionButtons: ["close", "maximize", "minimize"]
            });
    });
}           

{% endhighlight %}



![](action-buttons_images\action-buttons_img1.png)


## Customizing Action Buttons

We can customize the action buttons in dialog widget.

You can add new action button in the dialog widget by configuring the `actionButtonClick` event.

{% highlight javascript %}

           //create dialog widget
            var dialogInstance = new ej.Dialog($("#dialog"), {
                showOnInit: false,
                actionButtons: ["close", "collapsible", "maximize", "minimize", "pin", "mediaplay", "search"],
				actionButtonClick: "playMedia"
            });
            function playMedia(args)
		    {
               console.log(args.buttonID);
            }
{% endhighlight %}



![](action-buttons_images\action-buttons_img2.png)
