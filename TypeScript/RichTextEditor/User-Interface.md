---
layout: post
title: User Interface for the RichTextEditor widget
description: User Interface for RichTextEditor widget (toolbar, content area, and footer)
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Toolbar Configuration, Custom Tool, Tool items
---

# Toolbar Configuration

The editor’s toolbar contains a collection of tools such as bold, italic and text alignment buttons that are used to format the content.
However, in most integrations, it's desirable to change the toolbar configuration to suit needs. Fortunately, that's quite easy to do too.

<table>
<tr>
    <th> Property <br/><br/></th>
    <th> Description <br/><br/></th>
</tr>
<tr>
    <td> {{'[toolsList](https://help.syncfusion.com/api/js/ejrte#members:toolslist)'| markdownify }} <br/><br/></td>
    <td>  The toolsList option allows you to choose which tools appear on the toolbar, as well as the order and grouping of those items <br/><br/></td>
</tr>
<tr>
    <td> {{'[tools](https://help.syncfusion.com/api/js/ejrte#members:tools)'| markdownify }} <br/><br/></td>
    <td> The toolsList property is used to get the root group order and tools property is used to get the inner order of the corresponding groups displayed.<br/><br/></td>
</tr>
</table>

N> By default, when you tab from the textbox to the RTE, the first tools in the Toolbar of RTE will get focus not in the text area. <BR>
But we can able to focus the RTE text area by setting the tab index attribute as -1 to avoid the focus on RTE toolbar when we tab from textbox to RTE - {{'[Demo](http://jsplayground.syncfusion.com/Sync_1rlmhqbz)'| markdownify }}


## Toolbar Items

The following table lists the available buttons and dropdowns on the toolbar:

<table>
<tr>
<th>
Name<br/><br/></th><th>
Summary<br/><br/></th><th>
Initialization<br/><br/></th><th>
IsDefault?<br/><br/></th></tr>
<tr>
<td>
Font<br/><br/></td><td>
Applies font type, size, and color to the content.<br/><br/></td><td>
tools: { <br/>font: ["fontName", "fontSize", "fontColor", "backgroundColor"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Font style<br/><br/></td><td>
Applies bold, italic, underline, and strikethrough formatting to the content.<br/><br/></td><td>
tools: {<br/>style: ["bold", "italic", "underline", "strikethrough"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Alignment<br/><br/></td><td>
Align the content with left, center, and right margin. <br/><br/></td><td>
tools: {<br/>alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
List<br/><br/></td><td>
Create a new list item (bulleted/numbered).<br/><br/></td><td>
tools: {<br/>lists: ["unorderedList", "orderedList"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Indents<br/><br/></td><td>
Allows to increase/decrease the indent level of the content. <br/><br/></td><td>
tools: {<br/>indenting: ["outdent", "indent"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Undo/Redo Action<br/><br/></td><td>
Allows to undo/redo the actions<br/><br/></td><td>
tools: {<br/>doAction: ["undo", "redo"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Hyperlink<br/><br/></td><td>
Creates a hyperlink to a text or image to a specific location in the content.<br/><br/></td><td>
tools: {<br/>links: ["createLink","removeLink"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Images<br/><br/></td><td>
Inserts an image from an online source or local computer.<br/><br/></td><td>
tools: {<br/>images: ["image"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Media<br/><br/></td><td>
Allows to embed a video into the document.<br/><br/></td><td>
tools: {<br/>media: ["video"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Table<br/><br/></td><td>
Allows to add or modify Tables.<br/><br/></td><td>
tools: {<br/>tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Casing<br/><br/></td><td>
Change the case of selected text in the content<br/><br/></td><td>
tools: {<br/>casing: ["upperCase", "lowerCase"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Scripts<br/><br/></td><td>
Makes the selected text as superscript (higher) or subscript (lower).<br/><br/></td><td>
tools: {<br/>effects: ["superscript", "subscript"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Format<br/><br/></td><td>
Clears the formatting options like bold, italic, underline and more.<br/><br/></td><td>
tools: {<br/>formatStyle: ["format"]<br/>}<br/><br/></td><td>
Yes<br/><br/></td></tr>
<tr>
<td>
Clipboard Actions<br/><br/></td><td>
Controls the clipboard actions by applying specific action on the selected content.<br/><br/></td><td>
tools: {<br/>clipboard: ["cut", "copy", "paste"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
Edit<br/><br/></td><td>
Allows to make find and replace functionalities with the content.<br/><br/></td><td>
tools: {<br/>edit: ["findAndReplace"] <br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
view <br/><br/></td><td>
Allows to change the editor view mode.<br/><br/></td><td>
tools: { <br/>view: ["fullScreen","zoomIn","zoomOut"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
<tr>
<td>
print <br/><br/></td><td>
Allows to print the editor content.<br/><br/></td><td>
tools: { <br/>print: ["print"]<br/>}<br/><br/></td><td>
No<br/><br/></td></tr>
</table>

## Rearrange Group

The toolbar contains groups, which are similar or related functionalities of toolbar items for efficient access. By default, the groups are arranged using the following order

{% highlight javascript %}
toolsList:["formatStyle","font","style","effects","alignment","lists","indenting","clipboard","doAction", 
"clear","links","images","media","tables","casing","customTools","view"]
{% endhighlight %}

The group can be rearranged on customization using the **[toolsList](https://help.syncfusion.com/api/js/ejrte#members:toolslist)** property.

{% highlight html %}

<textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            toolsList:["links","lists","doAction","style","images"],
            tools:{
                style:["bold","italic"],
                lists:["unorderedList","orderedList"],
                doAction:["undo","redo"],
                links:["createLink","removeLink"],
                images:["image"]
            }
        });
    });
}

{% endhighlight %}

N> If you are not specify any group in **toolsList** property, the editor will create the toolbar with default group.


## Undo and Redo

Undo and Redo buttons allow you to editing the text by disregard/cancel the recently made changes and restore it to previous state. It is a useful tool to restore the performed action which got changed by mistake. Up to 50 actions can be undo/redo in the editor by default. 

To undo and redo operations, do one of the following:

* Press the undo/redo button on the toolbar
* Press the **Ctrl** **+** **Z**/**Ctrl** **+** **Y** combination on the keyboard


{% highlight html %}

<textarea id ="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            toolsList: ["doAction"],
            tools: {
                doAction: ["undo", "redo"]
            }
        });
    });
}

{% endhighlight %}

## Clipboard Operations

The editor provides support for the clipboard operations (cut, copy, and paste) in all text and images using the toolbar buttons and the keyboard shortcuts. Toolbar includes buttons through which the clipboard operations, such as Cut, Copy, and Paste can be accessed.

You can use the keyboard shortcuts to perform the clipboard operations.

* Cut - CTRL+X
* Copy - CTRL+C
* Paste - CTRL+V

N> Some browsers block the clipboard access from JavaScript. If you want to use the Cut, Copy, and Paste buttons on the toolbar, you need to allow JavaScript to use the clipboard. If you don’t want to do this configuration, use CTRL+C, CTRL+X, and CTRL+V keyboard commands.

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                toolsList: ["clipboard"],
                tools: {
                    clipboard: ["cut", "copy", "paste"]
                }
            });
      });
  }

{% endhighlight %}

## Types of responsive toolbar

Two types of toolbar modes are available for RTE in responsive mode. This includes "inline" and "popup". Toolbar Type can be set through API [toolbarOverflowMode](https://help.syncfusion.com/api/js/ejrte#members:toolbarOverflowMode)  whose default value is "popup".

{% highlight html %}

     <textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            isResponsive:true,
			toolbarOverflowMode:"inline",
            });
        });
   }


{% endhighlight %}

N> If you are not specifying toolbarOverflowMode, responsive RTE will be rendered with default popup toolbar.