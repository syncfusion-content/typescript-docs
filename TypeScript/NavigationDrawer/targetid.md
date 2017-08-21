---
layout: post
title: targetid
description: targetid
platform: typescript
control: Navigation Drawer
documentation: ug
---

## TargetId

This property is used to define the target Id for **Navigation Drawer**. The drawer opens while you click on the specified target element.

{% highlight html %}

        <button id="drawerTarget" style="top:200px;left:600px;position:absolute"></button>
        
        <div id="navpane">
                <ul>
                    <li>Settings</li>
                    <li>Read</li>
                    <li>Help</li>
                    <li>About</li>
                </ul>
        </div>
        
{% endhighlight %}

Add the following code in the **script** tag.

{% highlight javascript %}
    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module NavigationDrawerComponent {
    $(function () {
        var navigationdrawerInstance = new ej.NavigationDrawer($("#navpane"), {
                position: "fixed",
                targetId: "drawerTarget",
                enableListView: true,
                listViewSettings: { width: 300 }
        });
         var buttonInstance = new ej.ejButton($("#drawerTarget),{
              text:"Open Drawer"
         }) ;
    });
  }
 
{% endhighlight %}

The following screenshots illustrates the output.

![](targetid_images\targetid_img1.png)

Before target click
{:.caption}



![](targetid_images\targetid_img2.png)

After target click
{:.caption}

