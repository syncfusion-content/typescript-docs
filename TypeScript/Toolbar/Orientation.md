---
layout: post
title: Orientation
description: orientation
platform: TypeScript
control: Toolbar
documentation: ug
---

# Orientation

The **Toolbar** control supports both vertical and horizontal orientations, allowing it to fit into any scenario. The **orientation** property **of Toolbar** defines the orientation in which the control is rendered. Set the value to this property as **enum or string** type. It accepts the following values.

* ej.Orientation.Horizontal or “Horizontal”
* ej.Orientation.Vertical  or “Vertical”

The following section explains you on how to set orientation for the toolbar.

## Horizontal

This property sets the **Toolbar** in **horizontal** orientation. You can refer the following steps to set horizontal orientation for **Toolbar** control.

In View, create UL-LI list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ToolbarComponent {
    
    $(function () {
        var sample = new ej.Toolbar($("#toolbar"),{ 
            width: "290px", 
            orientation: ej.Orientation.Horizontal
         });
    });
}
{% endhighlight %}

OR

{% highlight js %}

    $(function () {
        // declaration            
          var sample = new ej.Toolbar($("#toolbar"),{ 
             width: "290px",
             orientation: "Horizontal" 
              });
    });

{% endhighlight %}

Build and run the application.

The following screenshot illustrates a **Toolbar** with horizontal orientation.

![](Orientation_images/Orientation_img1.png)

## Vertical

This property sets the **Toolbar** in **vertical** orientation. You can refer the following steps to set vertical orientation for **Toolbar** control.

Create UL-LI list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.


{% highlight js %}

    $(function () {
        // declaration
        var sample = new ej.Toolbar($("#toolbar"),{ 
            orientation: ej.Orientation.Vertical 
        });
    });

{% endhighlight %}

OR

{% highlight js %}

    $(function () {
        // declaration
        var sample = new ej.Toolbar($("#toolbar"),{ 
             orientation: "Vertical" 
        });
    });

{% endhighlight %}


Build and run the application.

The following screenshot illustrates a **Toolbar** with vertical orientation.

![](Orientation_images/Orientation_img2.png)
