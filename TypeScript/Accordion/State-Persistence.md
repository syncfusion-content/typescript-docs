---
layout: post
title: State-Persistence
description: state persistence
platform: Typescript
control: Accordion 
documentation: ug
---

# State Persistence

**Accordion** widget can store the model value in the browser cookies and on every time after initial rendering, the control get the model from the cookie only. Using **enablePersistence** property you can store the model value in cookies. Thus when any changes are made dynamically then those values are updated in cookie. On refreshing the page the past state of the **Accordion** control is maintained in cookie and control is rendered from it.

## Configure state persistence of Accordion panel

The following steps explains to enable state maintenance for **Accordion**.

In an HTML page, define a div element that is a container for  Accordion widget and add the contents correspondingly

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

 // Configure enablePersistence for Accordion

 /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module AccordionComponent {
    $(function () {
        var sample = new ej.Accordion($("#accordion"), {
        enablePersistence: true
    });
 });
} 

{% endhighlight %}


Output after page refresh maintaining the previous state of Accordion widget is as follows.


![](State-Persistence_images/State-Persistence_img1.png)

