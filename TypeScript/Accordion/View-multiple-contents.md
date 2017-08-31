---
layout: post
title: View-multiple-contents
description: view multiple contents
platform: Typescript
control: Accordion 
documentation: ug
---

# View multiple contents

By default **Accordion** allows only one panel to be in expanded state. You can enable multiple panels in expand state by setting **enableMultipleOpen** to **true.**

## Enabling multiple panel open

The following steps explains you to enable multiple panel for **Accordion**.

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

    // Enable multiple open for Accordion
    $("#accordion").ejAccordion({
        enableMultipleOpen: true
    });
    
{% endhighlight %}


Following screenshot is the output for Accordion control on enableMultipleOpen set to true.


![](/js/Accordion/View-multiple-contents_images/View-multiple-contents_img1.png)

