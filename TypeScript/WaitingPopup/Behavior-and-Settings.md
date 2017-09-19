---
layout: post
title: Behavior-and-Settings
description: behavior and settings
platform: TypeScript
control: WaitingPopup
documentation: ug
---

# Behavior and Settings

## Automatic Initializing WaitingPopup widget

**WaitingPopup** widget contains **showOnInit** property that allows the popup to display over a target on page load automatically. By default, **showOnInit** property is set as false.

The following steps explains you on how to display the **WaitingPopup** on page load.

In an **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}

<div class="control">
    <div id="waitingPopUp"></div>
</div>  

{% endhighlight %}

{% highlight js %}

// Configure the WaitingPopup to display automatically on page load as follows.

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module WaitingPopupComponent {
    $(function () {
        var sample = new ej.WaitingPopup($("#waitingPopUp"),{
            showOnInit: true,
        });
    });
}
{% endhighlight %}

 Add the following styles to render **WaitingPopup** widget.


{% highlight css %}

<style type="text/css" class="cssStyles">

   #waitingPopUp {
       height: 320px;
       width: 600px;
   }
</style>

{% endhighlight %}


The following screenshot illustrates the **WaitingPopup** when **showOnInit** is set to “**true**”.

![](Behavior-and-Settings_images/Behavior-and-Settings_img1.png) 

## Enable / Disable Popup Indicator

You can show or hide the popup indicator of **WaitingPopup** widget using **showImage** property. By default, **showImage** property is set as **true**.

The following steps explains you to enable / disable popup indicator in **WaitingPopup** widget.

 In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}

<div class="control">
    <div id="waitingPopUp"></div>
</div>  

{% endhighlight %}

{% highlight js %}

    // To configure Enable / Disable popup indicator in WaitingPopup, use the following code.
    //Enable popup indicator:
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module WaitingPopupComponent {
 $(function () { 
     var sample = new ej.WaitingPopup($("#waitingPopUp"),{
            showOnInit: true,
            showImage: true,
            text: "Loading... Please wait..."
        });
    });
 }   
    //Disable popup indicator:
 $(function () {
        // declaration
       var sample = new ej.WaitingPopup($("#waitingPopUp"),{
            showOnInit: true,
            showImage: false,
            text: "Loading... Please wait..."
        });
    });
 

{% endhighlight %}

 Add the following styles to render **WaitingPopup** widget.


{% highlight css %}

<style type="text/css" class="cssStyles">
   #waitingPopUp {
       height: 320px;
       width: 600px;
   }
</style>

{% endhighlight %}



Execute the above code to render the following output.

![](Behavior-and-Settings_images/Behavior-and-Settings_img2.png) 

![](Behavior-and-Settings_images/Behavior-and-Settings_img3.png) 

## Show / Hide WaitingPopup

Using **show()** and **hide()** methods, you can display or hide the **WaitingPopup** widget over the target area.

The following steps explains you to show / hide the **WaitingPopup** widget.

In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}

<div class="control">
    <div id="waitingPopUp"></div>
</div>

{% endhighlight %}

{% highlight js %}

    // Use the following code to Show / Hide WaitingPopup.
    //Show WaitingPopup:
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module WaitingPopupComponent {
    $(function () {
        var sample = new ej.WaitingPopup($("#target"),{
        var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");
        popUpObj.show();
    });
}   
    //Hide WaitingPopup:
    $(function () {
        var sample = new ej.WaitingPopup($("#target"),{
        var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");
        popUpObj.hide();
    });

{% endhighlight %}

Add the following styles to render **WaitingPopup** widget.

{% highlight css %}

<style type="text/css" class="cssStyles">
   #waitingPopUp {
       height: 320px;
       width: 600px;
   }
</style>

{% endhighlight %}



The following screenshot illustrates a **WaitingPopup** when **show()** method is invoked.

![](Behavior-and-Settings_images/Behavior-and-Settings_img4.png) 

