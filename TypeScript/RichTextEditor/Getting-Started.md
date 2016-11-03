---
layout: post
title: Getting Started for Typescript RichTextEditor
description: Getting started with RichTextEditor and configure the toolbar and other functionalities.
platform: Typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Control Initialization, Setting and Getting Content
---
# Getting Started

This section helps to understand the getting started of RTE control with the step-by-step instruction.

## Script and CSS reference

Create a new HTML file and include the below code

Add link to the CSS file from the specific theme folder to your HTML file within the head section. Refer the built-in available themes from [here](http://helpjs.syncfusion.com/js/theming-in-essential-javascript-components#). 
Also add links to the [CDN](http://helpjs.syncfusion.com/js/cdn#) Script files along with the other external dependencies as depicted below,

{% highlight html %}
<head>
   <meta charset="utf-8" />
   <title>Getting Started - RichTextEditor</title>
   <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
   <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>  
   <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
{% endhighlight %}

N> Uncompressed version of the required library files are available for the development or debugging purpose which can be generated from the custom script [here](http://csg.syncfusion.com/#). Also to reduce the file size further please use [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) compression in your server.

## Control Initialization

Create a **TextArea** element within the body of the HTML document where the widget needs to be rendered.

{% highlight html %}
<body>
   <textarea id ="texteditor"></textarea>
</body>
{% endhighlight %}
 
Initialize the editor in ts file by using the `ej.RTE` method.

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{});
    });
}

{% endhighlight %}

## Toolbar–Configuration

You can configure a toolbar with the tools as your application requires.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            toolsList: ["style", "lists", "doAction", "links", "images"],
            tools: {
                style: ["bold", "italic"],
                lists: ["unorderedList", "orderedList"],
                doAction: ["undo", "redo"],
                links: ["createLink"],
                images: ["image"]
            }
        });
    }); 
}
{% endhighlight %}

## Setting and Getting Content

You can set the content of the editor as follows.

{% highlight javascript %}

<textarea id="texteditor"></textarea>
   
<script type="text/javascript">
    $("#texteditor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
        " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
    });
</script>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
            " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        });
    }); 
}

{% endhighlight %}

To retrieve the editor contents,

{% highlight javascript %}
var currentValue = $("#texteditor").ejRTE("model.value");
{% endhighlight %}

You can find sample to quick start with the editor [here](http://jsplayground.syncfusion.com/Sync_nenmojvz#).

