---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: TypeScript
control: TimePicker
documentation: ug
---

# Keyboard Interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **TimePicker** widget. **TimePicker** widget allows you to perform all kinds of actions using keyboard shortcuts.

List of keyboard shortcuts

<table>
    <tr>
        <th>
            Shortcut Key
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            <a href="http://en.wikipedia.org/wiki/Access_key">Access key</a> + j
        </td>
        <td>
            Focuses into TimePicker widget
        </td>
    </tr>
    <tr>
        <td>
            Alt + Down
        </td>
        <td>
            Opens/Hides the popup
        </td>
    </tr>
    <tr>
        <td>
            Right/Left
        </td>
        <td>
            Moves to adjacent part
        </td>
    </tr>
    <tr>
        <td>
            Up
        </td>
        <td>
            Increments the value
        </td>
    </tr>
    <tr>
        <td>
            Down
        </td>
        <td>
            Decrements the value
        </td>
    </tr>
</table>


List of keyboard shortcuts, When popup is open

<table>
    <tr>
        <th>
            Shortcut Key
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            Up
        </td>
        <td>
            Selects the previous time
        </td>
    </tr>
    <tr>
        <td>
            Down
        </td>
        <td>
            Selects the next time.
        </td>
    </tr>
    <tr>
        <td>
            Home/End
        </td>
        <td>
            Moves to the first / last item
        </td>
    </tr>
    <tr>
        <td>
            Esc
        </td>
        <td>
            Closes the popup
        </td>
    </tr>
</table>

## Configure Keyboard Interaction

The following steps explains you on how to enable keyboard interaction for the **TimePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget and enable keyboard interaction by setting the **access key** property.

{% highlight html %}

<input type="text" id="time" accesskey="j"/>

{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
    // You can render the TimePicker control using the following code.
    $(function () {
         var timeSample = new ej.TimePicker($("#timepick"), {
    });
});
}

{% endhighlight %}

Run the code sample, press **[Access key](http://en.wikipedia.org/wiki/Access_key) + J** to focus in the **TimePicker** widget that enables it and you can navigate using arrow keys and Esc key to close the popup.



![](Keyboard-Interaction_images/Keyboard-Interaction_img1.png) 

