---
layout: post
title: Enable-or-Disable-the-Uploadbox
description: enable or disable the uploadbox 
platform: Typescript
control: Uploadbox
documentation: ug
---

# Enables or Disables the Uploadbox 

This feature helps set the **enable** or **disable** option for **Uploadbox** by setting **Boolean** type value to **enabled** property. For **enable** or **disable** option, set **enabled** property to ‘**false**’. The data type is **Boolean**.

The following steps explain the configuration of **enabled** property in **Uploadbox**. 

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}

<div id="Uploadbox"></div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript.
/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module UploadboxComponent {
    // Initialize the control in JavaScript.
    $(function () {
        //Declaration.
        var sample = new ej.Uploadbox($("#Uploadbox"),{
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            enabled: false
        });
    });
}
{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



![](Enable-or-Disable_images/Enable-or-Disable_img1.png) 

