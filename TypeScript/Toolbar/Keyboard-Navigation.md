---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: TypeScript
control: Toolbar
documentation: ug
---

# Keyboard Navigation

The entire **Toolbar** commands can be accessed through the keyboard by specifying the **Keyboard Shortcut** listed in the following table.

List of keyboard shortcuts

<table>
<tr>
<th>
Keyboard Shortcut</th><th>
Function</th></tr>
<tr>
<td>
Alt + j</td><td>
Focuses the control</td></tr>
<tr>
<td>
UP</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Left</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Right</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item.</td></tr>
<tr>
<td>
End</td><td>
Navigates to the ending item.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
</table>


The following code example illustrates shortcuts associated with the **Toolbar** items.



{% highlight html %}

<!-- Refer Local Data section for style and data bound for toolbar item -->

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module ToolbarComponent {
    $(function () {
        // declaration
        var sample = new ej.Toolbar($("#toolbar"),{
             width: "290px"
              });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#toolbar").focus();
            }
        });
    });
}  

{% endhighlight %}

![](Keyboard-Navigation_images/Keyboard-Navigation_img1.png) 

