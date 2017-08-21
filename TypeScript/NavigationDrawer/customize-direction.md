---
layout: post
title: customize-direction
description: customize direction
platform: typescript
control: Navigation Drawer
documentation: ug
---

## Customize Direction

By using this property you can set the drawer to be open from right to left direction or left to right direction. The possible direction values are Right, Left and the default value is Left. Refer to the following code example.

{% highlight html %}

    <div id="main" style="height:700px;">
        <div id="navpane">
            <ul>
                <li>Settings</li>
                <li>Read</li>
                <li>Help</li>
                <li>About</li>
            </ul>
        </div>
    </div>

{% endhighlight %}

Add the following code in the **script** tag.

{% highlight javascript %}
    
 ///  <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module NavigationDrawerComponent {
    $(function () {
        var navigationdrawerInstance = new ej.NavigationDrawer($("#navpane"), {
             direction: "right",
             position: "fixed", 
             enableListView: true,
             listViewSettings: { width: 300 } 
        });
    });
}

{% endhighlight %}


The following screenshot displays the output by swiping from right to left at the right side end of the screen.

![](customize-direction_images\customize-direction_img1.png)

