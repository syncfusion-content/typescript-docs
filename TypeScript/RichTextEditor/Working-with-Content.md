---
layout: post
title: Working with content related operation in RichTextEditor widget
description: Working with Content related changes in RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, IFrame Attributes, Editing and Formatting 
---
# Working with Content

The editor creates the iframe element as the content area on control initialization, it is used to display and editing the content. In Content Area, the editor displays only the body tag of a &lt; iframe &gt; document. To set or modify details in the &lt; head &gt; tag, use [Source view](#footer#source-view) of the editor.

## Iframe Attributes

The editor allows you to passing an additional attributes to body tag of a &lt; iframe &gt; element using [iframeAttributes](https://help.syncfusion.com/api/js/ejrte#members:iframeattributes) property. The property contains name/value pairs in string format, it is used to override the default appearance of the content area. 

N> the content area’s font, color, margins, and background can be overridden using iframeAttributes property. You can specifies the editable behavior (content editable) of the content also in this property.

{% highlight html %}

<textarea id="rteSample"></textarea>
 
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            iframeAttributes:{style: "background-color:#e0ffff;color:#6495ed;"}
        });
    });
}

{% endhighlight %}

N> Background image for the RTE control : {{'[Link](http://jsplayground.syncfusion.com/Sync_cpaoqshs)'| markdownify }} <BR>
Set default font for the Iframe : {{'[Link](http://jsplayground.syncfusion.com/Sync_k2uwsibi)'| markdownify }}


## Content Editable

The editor provides option to control the editable behavior using [allowEditing](https://help.syncfusion.com/api/js/ejrte#members:allowediting) property. When the allowEditing property is set to false, the editor disables its editing functionality. 

{% highlight html %}

<textarea id ="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
                allowEditing: false
            });

        });
 }

</script>
{% endhighlight %}

The contentEditable attribute allows you to make any element of HTML content to become editable or non-editable.  

{% highlight html %}

<textarea id ="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "<p>The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,</p>" +
                "<p> it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.</p>",
            });

            var editor = $("#editor").ejRTE("instance");
            var iframeDoc = editor.getDocument();
            var paragraph = $("p", iframeDoc.body);
            $($(paragraph)[1]).attr("contenteditable", "false");
        });
   });
}

{% endhighlight %}

N> Content editable is fully compatible with latest browsers, to know more details, see [here](http://www.w3schools.com/tags/att_global_contenteditable.asp#).

## Submit Content

The editor allows you to process its content before it is being submitted to the server on form submit event. You can use this option to validate content on the client side to prevent invalid data from being submitted to the server.

This example shows how to encode the HTML content before form submit event.

{% highlight html %}

    <form>
        <textarea id ="rteSample"></textarea>
        <button type ="submit">Submit</button>
    </form>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });

        $("form").on("submit", function () {
            var editor = $("#editor").data("ejRTE");
            var encoded = $('<div />').text(editor.model.value).html();
            $("#editor").val(encoded);

        });
   });
}

{% endhighlight %}

## Persistence

The editor is capable to persist its content with HTML format. By default, the persistence support is disabled in the editor. When you set the [enablePersistence](https://help.syncfusion.com/api/js/ejrte#members:enablepersistence) property to true, the persistence will be enabled in the editor.

N>  [local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is not supported below ie9 version, therefore persistence support is fallback to [cookie](http://www.w3schools.com/js/js_cookies.asp#).

{% highlight html %}

    <textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                enablePersistence: true
            });
        });
  }


{% endhighlight %}

## Apply Font color and Background color

If you want to apply font  color or background color for a selected content of RTE you can use font color and background color tools. These tools contains a color palette with basic colors along with an option called **"More colors.."** in order to choose custom colors from color picker dialog.You can apply transparent background color for selected text through **transparent** button available in background color palette.

{% highlight html %}

    <textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
              value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images, it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
              tools: {
                font: ["fontName", "fontSize", "fontColor", "backgroundColor"]
            }
        });
     });
}

{% endhighlight %}

## Insert the content at cursor

If you want to insert/paste the content at the current cursor position (or) to replace the selected content with some formatting, you can use pasteContent method in the editor.

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            value:"The RichTextEditor (RTE) control enables you to edit the contents with insert table and images,"+
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        });
    });
}
    function pasteContent() {
        var selectedHtml = sample.getSelectedHtml();
        sample.pasteContent("<p style ='background-color:yellow;color:skyblue'>" + selectedHtml + "</p>");
    }
{% endhighlight %}
