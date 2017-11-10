---
layout: post
title: Customization of RichTextEditor widget for Syncfusion Essential JS
description: Customization in RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Context Menu, Adding Items, Removing Items
---

# How To

## Add Google web fonts to editor 

To use web fonts in EJ RTE, it is not needed for the web fonts to be present in local machine. To add the web fonts to EJ RTE, we need to append the web font link to the RTE Iframe <head> tag. We can achieve this in the “create” event of the RTE as shown below. 

{% highlight html %}

    <textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px">
        Description:
        The Rich Text Editor (RTE) control is an easy to render in
        client side.Customer easy to edit the contents and get the HTML content for
        the displayed content.A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area.
    </textarea>


         var fonts = [
                { text: "Segoe UI", value: "Segoe UI" },
                //Added from Google web fonts
                { text: "Noto Sans", value: "Noto Sans" },
                { text: "Roboto", value: "Roboto" },
                { text: "Great vibes", value: "Great Vibes,cursive" }
         ];

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                width: "550px",
                showFooter: true,
                fontName:fonts,
                tools: {
                    font: ["fontName", "fontSize", "fontColor", "backgroundColor"],
                    style: ["bold", "italic", "underline", "strikethrough"],
                    alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
                    lists: ["unorderedList", "orderedList"],
                    copyPaste: ["cut", "copy", "paste"],
                    doAction: ["undo", "redo"],
                    clear: ["clearFormat", "clearAll"]
                        
                },
                create: function () {
                    var $head = this._rteIframe.contents().find("head");
                    var url = "Styles/styles.css";
                        //Added two Google web fonts (“Roboto” and “Great vibes”)
                    $head.append($("<link/>", { rel: "stylesheet", href: 'http://fonts.googleapis.com/css?family=Roboto', type: "text/css" }));
                    $head.append($("<link/>", { rel: "stylesheet", href: 'http://fonts.googleapis.com/css?family=Great+Vibes', type: "text/css" }));
                }
            });
        });
 }

{% endhighlight %}

In the above sample, you can see that we have added two Google web fonts (“Roboto” and “Great vibes”) to ejRTE. [Demo Link](http://jsplayground.syncfusion.com/Sync_ce43lcpy)

## Increase RTE max word count 

To increase the RTE content maximum word count, we suggest you to set the [maxLength](https://help.syncfusion.com/api/js/ejrte#members:maxlength) property for it. By default, maxLength value is 7000, assign it with a value based on your requirement. 

Refer the following API reference link: [Link](https://help.syncfusion.com/api/js/ejrte#members:maxlength) 

## Add multiple editor instances to a single page 

This is in fact a common use case, especially when you may wish to break your content into sections (e.g. titles, paragraphs) that the user can edit individually. 

### Multiple editor instances sharing same RTE properties 

In the following example, the page is broken into two separate editable areas, each sharing the same RTE configuration. Each individual `textarea` is provided the same class of 'myEdit'. 

{% highlight html %}

        <textarea class="myEdit" rows="10" cols="30" style="width: 740px; height: 440px">
            Title
        </textarea>
        <br>
        <textarea class="myEdit" rows="10" cols="30" style="width: 740px; height: 440px">
            Description
        </textarea>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($(".myEdit"),{
                width: "100%",
                minWidth: "100px",
                isResponsive: true,
                showToolbar: false,
                height: "50px"
            });
        });
}

{% endhighlight %}

### Multiple editor instances sharing a unique RTE properties

In this next example each editable area will be loaded with an instance of RTE with a unique configuration. This is especially helpful when different content areas have different needs. For example, you may want to provide a very simple configuration for editing titles and a more complete configuration for editing body content. This is accomplished by defining a RTE property for each desired configuration.

{% highlight html %}

        <textarea class="myEdit1" rows="10" cols="30" style="width: 740px; height: 440px">
            Title
        </textarea>
        <br>
        <textarea class="myEdit2" rows="10" cols="30" style="width: 740px; height: 440px">
            Description
        </textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($(".myEdit1"),{
                width: "100%",
                minWidth: "100px",
                isResponsive: true,
                showToolbar: false,
                height: "50px"
            });
        var sample1 = new ej.RTE($(".myEdit2"),{
                width: "100%",
                minWidth: "100px",
                isResponsive: true
            });
        });
   }
    
{% endhighlight %}

## Set the horizontal scroller rather than text wrapping in the RTE? 

This can be achieved by setting the CSS “whitespace” as nowrap in RTE body element in the create event of RTE as shown below code: 

{% highlight html %}

    <textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px">
        The RichTextEditor (RTE) control enables you to edit the contents with insert table and images
        It also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.
    </textarea>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                width: "100%",
                minWidth: "100px",
                create: "onCreate"

            });
        });
    }
     function onCreate() {
            //Access the content of the RTE within IFrame and set the style
            $('#rteSample_Iframe').contents().find('body').attr("style", "white-space: nowrap");
        }

{% endhighlight %}


## Set Toolbar Height

We do not have any property for adjusting the height of the RTE Toolbar. But it is possible to adjust the height by overriding the class of the RTE toolbar. Override the class as below,

{% highlight CSS %}

    <style>
        .e-rte .e-js.e-toolbar{
                height: 100px;
            }
    </style>
    
{% endhighlight %}

## Add Separator in the Toolbar

we can add separator in the RTE toolbar list. We have a property [“enableSeparator”](https://help.syncfusion.com/api/js/ejtoolbar#members:enableseparator) in the toolbar control. So we need to set this property as true by creating the object of toolbar in the “preRender” event of RTE as shown below code:

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                     enableSeparator: true
        });
    }
 }    

{% endhighlight %}

## Custom image for the Tools

This requirement can have achieved by using [“cssClass”](https://help.syncfusion.com/api/js/ejrte#members:cssclass) API of RichTextEditor component. It is used to customize the default “CSS” styles of the control. Using this API to define our own custom “CSS” and images to overwrite the default “CSS” styles of the control. 

{% highlight html %}

    <textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px">
        The RichTextEditor (RTE) control enables you to edit the contents with insert table and images
        It also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.
    </textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                cssClass: "dark"
             });
        });
   } 

{% endhighlight %}

Apply the following style and In the below sample, the sprite image has been used for the icons

{% highlight html %}

    <style type="text/css">
        .dark .e-rte-toolbar-icon {
            background: url(themes/icons/ui-icons-default.png);
        }
        .dark .e-active .e-rte-toolbar-icon, .dark .e-rte-toolbar-icon:hover {
            background: url(themes/icons/ui-icons-active.png);
        }
        .e-rte-toolbar-icon.bold:before, .e-rte-toolbar-icon.italic:before, .e-rte-toolbar-icon.underline:before, .e-rte-toolbar-icon.strikethrough:before, .e-rte-toolbar-icon.justifyLeft:before, .e-rte-toolbar-icon.justifyCenter:before, .e-rte-toolbar-icon.justifyRight:before, .e-rte-toolbar-icon.justifyFull:before, .e-rte-toolbar-icon.unorderedList:before, .e-rte-toolbar-icon.orderedList:before, .e-rte-toolbar-icon.undo:before, .e-rte-toolbar-icon.redo:before, .e-rte-toolbar-icon.createLink:before, .e-rte-toolbar-icon.image:before, .e-rte-toolbar-icon.video:before, .e-rte-toolbar-icon.createTable:before {
            content: none;
        }
        .dark .e-rte-toolbar-icon.outdent, .dark .e-rte-toolbar-icon.indent {
            background: none;
        }
        .dark .e-rte-toolbar-icon.bold, .dark .e-active .e-rte-toolbar-icon.bold {
            background-position: -288px 49px;
        }
        .dark .e-rte-toolbar-icon.italic, .dark .e-active .e-rte-toolbar-icon.italic {
            background-position: -313px 49px;
        }
        .dark .e-rte-toolbar-icon.underline, .dark .e-active .e-rte-toolbar-icon.underline {
            background-position: -338px 49px;
        }
        .dark .e-rte-toolbar-icon.strikethrough, .dark .e-active .e-rte-toolbar-icon.strikethrough {
            background-position: -364px 49px;
        }
        .dark .e-rte-toolbar-icon.justifyLeft, .dark .e-active .e-rte-toolbar-icon.justifyLeft {
            background-position: -389px 112px;
        }
        .dark .e-rte-toolbar-icon.justifyCenter, .dark .e-active .e-rte-toolbar-icon.justifyCenter {
            background-position: -338px 112px;
        }
        .dark .e-rte-toolbar-icon.justifyRight, .dark .e-active .e-rte-toolbar-icon.justifyRight {
            background-position: -416px 112px;
        }
        .dark .e-rte-toolbar-icon.justifyFull, .dark .e-active .e-rte-toolbar-icon.justifyFull {
            background-position: -364px 112px;
        }
        .dark .e-rte-toolbar-icon.unorderedList, .dark .e-active .e-rte-toolbar-icon.unorderedList {
            background-position: -131px 89px;
        }
        .dark .e-rte-toolbar-icon.orderedList, .dark .e-active .e-rte-toolbar-icon.orderedList {
            background-position: -104px 89px;
        }
        .dark .e-rte-toolbar-icon.undo, .dark .e-active .e-rte-toolbar-icon.undo {
            background-position: -262px 49px;
        }
        .dark .e-rte-toolbar-icon.redo, .dark .e-active .e-rte-toolbar-icon.redo {
            background-position: -234px 49px;
        }
        .dark .e-rte-toolbar-icon.createLink, .dark .e-active .e-rte-toolbar-icon.createLink {
            background-position: -470px 69px;
        }
        .dark .e-rte-toolbar-icon.image, .dark .e-active .e-rte-toolbar-icon.image {
            background-position: -287px 113px;
        }
        .dark .e-rte-toolbar-icon.video, .dark .e-active .e-rte-toolbar-icon.video {
            background-position: -311px 70px;
        }
        .dark .e-rte-toolbar-icon.createTable, .dark .e-active .e-rte-toolbar-icon.createTable {
            background-position: -1px 27px;
        }
    </style>
    
{% endhighlight %}

