---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: Typescript
control: Accordion 
documentation: ug
---

# Keyboard Navigation

You can use **Keyboard** shortcut keys as an alternative to the mouse on using Accordion widget using **allowKeyboardNavigation** property. However you will have to focus the control to enable the keyboard navigation. Accordion Widget allows you to perform all kind of actions using keyboard shortcuts.

List of Keyboard shortcut keys

<table>
<tr>
<th>Shortcut Key</th><th>Description</th></tr>
<tr>
<td>
Access key + j	</td><td>
Focuses into the accordion control</td></tr>
<tr>
<td>
Up</td><td>
Moves to previous panel</td></tr>
<tr>
<td>
Down</td><td>
Moves to next panel</td></tr>
<tr>
<td>
Left</td><td>
Moves to previous panel</td></tr>
<tr>
<td>
Right</td><td>
Moves to next panel</td></tr>
<tr>
<td>
Home</td><td>
Moves to the first accordion panel</td></tr>
<tr>
<td>
End</td><td>
Moves to the last accordion panel</td></tr>
</table>

### Configure keyboard interaction

The following steps explains you on how to enable keyboard interaction for an **Accordion** widget.

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

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path=tsfiles/ej.web.all.d.ts" />\

module AccordionComponent {
    $(function () {
        // Configure Keyboard navigation for Accordion by setting allowKeyboardNavigation property to true. Now define the script to focus the Accordion widget on AccessKey + J
        var sample = new ej.Accordion($("#accordion"), {
            allowKeyboardNavigation: true
        });
    
        // Define script to focus into the Accordion control on Alt + J shortcut keys.
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#accordion").focus();
            }
        });
    });
}

{% endhighlight %}


Output for Accordion widget focused and navigated to last item using Keyboard navigation is as follows.

![](Keyboard-Navigation_images/Keyboard-Navigation_img1.png) 


