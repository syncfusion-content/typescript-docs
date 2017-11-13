---
layout: post
title: Zoom and Print support in RichTextEditor widget for Syncfusion Essential JS
description: Zoom and Print support for RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Zoom, Print
---
# Zoom

The editor provides zoom tools which enlarges the view of an editor's object enabling you to see more detail. You can continuous zoomIn and zoomOut either using zoom tools or keyboard.

You can assign Increases and decreases of zooming range using [zoomStep](https://help.syncfusion.com/api/js/ejrte#members:zoomStep) property

{% highlight html %}

    <textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                    value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                    " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                    toolsList: ["view"],
                    tools: { view:[“zoomIn”,”zoomOut”]},
                    zoomStep: 0.1 
                });
        });
   }
{% endhighlight %}

![](ZoomandPrint_images/zoom.png)

# Print

The editor provides print tools which use to print the contents of the editor.

{% highlight html %}

    <textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                    value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                    " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                    toolsList: ["print"],
                    tools: { print:[“print”]}
                });

            });
}
{% endhighlight %}

![](ZoomandPrint_images/print.png)

