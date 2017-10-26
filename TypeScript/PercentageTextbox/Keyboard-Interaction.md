---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: typescript
control: PercentageTextBox 
documentation: ug
---

# Keyboard Interaction

With the keyboard navigation enabled in the **PercentageTextBox** control, it is possible to control the actions of the **PercentageTextBox** with the provided shortcut keys. Almost all the **PercentageTextBox** actions that are done through mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **PercentageTextBox** control are discussed in the following table. 

Keyboard Shortcuts

<table>
<tr>
<th>
Shortcut Key</th><th>
Description</th></tr>
<tr>
<td>
<a href="http://en.wikipedia.org/wiki/Access_key">Access key</a><b> + j</b></td><td>
Focuses the PercentageTextBox<b> </b>control</td></tr>
<tr>
<td>
Up</td><td>
Increments the value</td></tr>
<tr>
<td>
Down</td><td>
Decrements the value</td></tr>
</table>

## Configuring Keyboard Navigation

The following steps explain the implementation of keyboard interaction in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. Set the **access key** property to the **PercentageTextBox** control for focusing the control while key is pressed.



{% highlight html %}

<table cellpadding="10">
    <tbody>
        <tr>
            <td>
                <label for="percent">Percent</label>
            </td>
            <td>
                <input id="percent" type="text" accesskey="j" />
            </td>
        </tr>
    </tbody>
</table>

{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module EditorComponent {
    $(function () {
        var number = new ej.PercentageTextbox($("#percent"), {
            value: 22            
        });
    });
}  


{% endhighlight %}

Run the above example and press [Access key](http://en.wikipedia.org/wiki/Access_key) **+ j** key to focus the **PercentageTextBox** widget. Perform provided functionality by using keyboard shortcuts.



![](Keyboard-Interaction_images/Keyboard-Interaction_img1.png)