---
layout: post
title: RTL-Support
description: rtl support
platform: Typescript
control: Accordion 
documentation: ug
---

# RTL Support

This feature supports to change the left-to-right alignment of the **Accordion** widget to right-to-left (**RTL**). 

## Enabling RTL Support

The following steps explains you in enabling the right-to-left property for an **Accordion**.

In an HTML page, define a div element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}

<div id="accordion" style="width: 500px">
    <h3>
        <a href="#">Orubase</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Orubase is the only mobile application development Framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible time frame.
    </div>
    <h3>
        <a href="#">WinRTXAML</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
    </div>
    <h3>
        <a href="#">Metro Studio</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
    </div>
</div>

{% endhighlight %}


{% highlight javascript %}

    // Enable RTL for accordion control

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module AccordionComponent {
    $(function () {
        var sample = new ej.Accordion($("#accordion"), {
        enableRTL: true
    });
 });
}
	
{% endhighlight %}


Output for accordion when “enableRTL” is set to “true” is as follows,

![](RTL-Support_images/RTL-Support_img1.png) 

