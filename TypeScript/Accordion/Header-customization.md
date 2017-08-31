---
layout: post
title: Header-customization
description: header customization
platform: Typescript
control: Accordion 
documentation: ug
---

# Header customization

## Collapsible

**Accordion** widget allows you to set Collapsible state for an **Accordion** header. Thus you can expand and collapse accordion contents. By default **collapsible** is set to **false**.

### Enable Collapsible settings

The following steps explains to enable Collapsible state for **Accordion**.

In an HTML page, define a div element that is a container for Accordion widget and add the contents correspondingly

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
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module AccordionComponent {
    $(function () {
    // Configure collapsible header for Accordion
 var sample = new ej.Accordion($("#accordion"), {
        collapsible: true
    });
  });
}   

{% endhighlight %}

Output for Accordion control with collapsible headers.


![](Header-customization_images/Header-customization_img1.png) 

## Enable Header expand

**Accordion** widget provides you support to set the event, where the headers should expand and collapse. The **events** properties takes default events like mouseout, mouseover, and click.

### Configure header expand event

The following steps explains you to configure header expand event for **Accordion**.

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

    // Configure header expand event for Accordion
   var sample = new ej.Accordion($("#accordion"), {
        events: "mouseout"
    });

{% endhighlight %}


Output for Accordion control that expands header on mouseout event is as follows.


![](Header-customization_images/Header-customization_img2.png) 

## Set selected header

### Single selection

Using **selectedItemIndex** property you can modify the expanded panel when the control is rendered. By default **selectedItemIndex** is ‘0’ that always activate the first **Accordion** panel.

### Specify the selected item in Accordion panel

The following steps explains you to configure selected item for **Accordion**.

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

    // Configure selected item for Accordion based on the index
    var sample = new ej.Accordion($("#accordion"), {
        selectedItemIndex: 1
    });

{% endhighlight %}

Output for Accordion control with the selected item by index is as follows.

![](Header-customization_images/Header-customization_img3.png) 

## Multiple selection

In **Accordion** widget you can select multiple panel items using **selectedItems** property. It takes array of indices that needs to be selected on rendering the control. As you need to select multiple items, you can set **enableMultipleOpen** to **true**.

### Configure multiple selection in Accordion panel

The following steps explains to configure selected items for **Accordion**.

In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

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

    // Configure multiple item selection for Accordion
   var sample = new ej.Accordion($("#accordion"), {
        selectedItems: [0, 2],
        enableMultipleOpen: true
    });

{% endhighlight %}

Output for Accordion control with the multiple selected items is as follows.


![](Header-customization_images/Header-customization_img4.png) 

