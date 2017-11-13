---
layout: post
title: Context Menu in RichTextEditor widget
description: Context Menu related changes in RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Context Menu, Adding Items, Removing Items
---

# Context Menu 

Editor provides custom context menu support, which enables more interaction on the content modification and also it can be enabled dynamically. The showContextMenu property helps to enable custom context menu within editor area.
Based on the target content type context menu provides different actions. Refer the details with below table.

{% highlight html %}

<textarea id="rteSample">
 <p><b>Description:</b></p>
        <p>The Rich Text Editor (RTE) control is easy to render in the
        client side. Customers can easily edit the contents and get the HTML content for
        the displayed content. A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area. </p></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
        showContextMenu: true
        });
    });
}

{% endhighlight %}

* Based on the target content type context menu provides different actions- refer the details with below table.

<table>
<tr>
<td>
Content-Type
</td>
<td>
Supported Actions 
</td>
</tr>
<tr>
<td>
Text content
</td>
<td>
cut, copy, paste, add/edit/open/remove hyperlink.
</td>
</tr>
<tr>
<td>
Image content
</td>
<td>
cut, copy, paste, image properties.
</td>
</tr>
<tr>
<td>
Table content
</td>
<td>
cut, copy, paste, insert row/column, remove row/column/table, edit table properties, add/edit/open/remove hyperlink.
</td>
</tr>
</table>

N> We have given support to own context menu by restricting the default browser context menu, which provides you the options for quick access but, with that clipboard action are restricted based on browser behavior. <BR>

However we can disable the context menu by using ShowContextMenu API and it needs to be set as false, if you wish to continue with default browser context menu.

