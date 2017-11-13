---
layout: post
title: Working with Lists operation in RichTextEditor widget
description: Working with Lists customization for RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Lists, Custom Lists

---
# Working with Lists

The editor provides tools to makes your content as list such as an ordered and unordered list.

## Create a Lists

By default, [Insert Lists](https://help.syncfusion.com/api/js/ejrte#members:tools-lists) tool is enabled in the editor’s toolbar.The editor’s have ordered and unordered list types.

{% highlight html %}

    <textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                    value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                    " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                    toolsList: ["lists"],
                    tools: {
                        lists: ["unorderedList", "orderedList"]
                    }
            });
     });
}
{% endhighlight %}

## Custom Lists

You can use [custom lists](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList) tools to insert lists with custom behaviors.You can create a list with related attributes (such as listImage, listStyle, title, name, and text) using the custom list tool.Ordered and Unordered list having own customize ways to insert a list into the editor’s content.

* [Insert a customOrderedList](#insert-a-customOrderedList)
* [Insert a customUnorderedList](#insert-a-customUnorderedList)  


### Insert a customOrderedList

you need to enable [customOrderedList](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList) tool on the editor’s toolbar.

The customOrderedList having below options for an ordered list customization.
<table>
<tr>
<th>
Option<br/><br/></th><th>
Summary<br/><br/></th></tr>
<tr><td>{{'[name](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-name)'| markdownify }} </td><td>Specifies the name for customOrderedList item.</td></tr>
<tr><td>{{'[tooltip](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-tooltip)'| markdownify }} </td><td>Specifies the title for customOrderedList item.</td></tr>
<tr><td>{{'[css](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-css)'| markdownify }} </td><td>Specifies the styles for customOrderedList item.</td></tr>
<tr><td>{{'[text](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-text)'| markdownify }} </td><td>Specifies the text for customOrderedList item.</td></tr>
<tr><td>{{'[listStyle](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-listStyle)'| markdownify }} </td><td>Specifies the list style for customOrderedList item.</td></tr>
<tr><td>{{'[listImage](https://help.syncfusion.com/api/js/ejrte#members:tools-customOrderedList-listImage)'| markdownify }} </td><td>Specifies the image for customOrderedList item.</td></tr>
</table>


{% highlight html %}

    <textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                toolsList: ["lists"],
                tools: {
                    lists: ["orderedList"],
                    customOrderedList: [{
                        name: "orderedInsert",
                        tooltip: "Custom OrderedList",
                        css: "e-rte-toolbar-icon e-rte-listitems customOrdered",	 
                        text: "Lower-Greek",
                        listStyle:"lower-greek"
                    }]
                }
           });
      });
   }
{% endhighlight %}

![](WorkingwithLists_images/ordered.png)

### Insert a customUnorderedList

you need to enable [customUnorderedList](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList) tool on the editor’s toolbar.

The customUnorderedList having below options for an unordered list customization.

<table>
<tr>
<th>
Option<br/><br/></th><th>
Summary<br/><br/></th></tr>
<tr>
<td>
{{'[name](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-name)'| markdownify }} 
</td><td>Specifies the name for customUnorderedList item.</td></tr>
<tr><td> {{'[tooltip](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-tooltip)'| markdownify }} </td><td>Specifies the title for customUnorderedList item.</td></tr>
<tr><td> {{'[css](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-css) '| markdownify }} </td><td>Specifies the styles for customUnorderedList item.</td></tr>
<tr><td> {{'[text](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-text) '| markdownify }} </td><td>Specifies the text for customUnorderedList item.</td></tr>
<tr><td> {{'[listStyle](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-listStyle) '| markdownify }} </td><td>Specifies the list style for customUnorderedList item.</td></tr>
<tr><td> {{'[listImage](https://help.syncfusion.com/api/js/ejrte#members:tools-customUnorderedList-listImage) '| markdownify }} </td><td>Specifies the image for customUnorderedList item.</td></tr>
</table>

{% highlight html %}

    <textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                toolsList: ["lists"],
                tools: {
                    lists: ["unorderedList"],
                    customUnorderedList: [{
                        name: "UnorderedInsert",
                        tooltip: "Custom UnorderedList",
                        css: "e-rte-toolbar-icon e-rte-unlistitems customUnOrdered",
	                    text: "Smiley",
                        listImage:"url('../content/images/rte/Smiley-GIF.gif')"                   
                   }]
                }
            });
        });
    }

{% endhighlight %}

![](WorkingwithLists_images/unordered.png)

