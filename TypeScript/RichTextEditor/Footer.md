---
layout: post
title: Footer in RichTextEditor widget for Syncfusion Essential JS
description: Footer related changes in RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Footer, Clear Format, Re-sizer, HTML Tag info, Characters Count, Word Count
---

# Footer

This option allows you to specify which footer elements should display at the bottom of the editor. The available footer elements are listed below:

1. HTML View
2. HTML Tag Info
3. Characters Count / Word Count
4. Clear Format
5. Resizer

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{ 
        showFooter: true
    });
 });
}


{% endhighlight %}

## Source View

RichTextBox includes the ability for users to directly edit HTML code via “Source View” in a separate dialog. If you made any modification in Source view directly, click Update button to synchronize with Design view. This provides power users with more flexibility over the content they create.

You can paste HTML text into Source view. If you cut or copy from HTML source such as page source of Browser, paste as HTML (without escape characters) into Source view.

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{ 
        showFooter:true,
        showHtmlSource:true
    });
  });
 } 



{% endhighlight %}

N> Source view is useful for working directly with raw HTML text, so this tool is mainly used for advanced users who would like to have more control over the source of their content. 

## HTML Tag Info

The HTML tag info tool that shows the path of currently selected tag along with hierarchy of parent tags to which it belongs. The tag information is displayed at the bottom of the editor. It is used to determine which element has the focus in the editor’s content. 

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
        showFooter:true,
        showHtmlTagInfo:true
    });
  });
}

{% endhighlight %}

N> The outermost tag is the body tag of &lt; iframe &gt; element in design view, so it shows the path from currently selected path to the body tag.

## Characters Count/Word Count

The editor automatically counts the number of characters and words in the content while you type. The characters and words count displayed at the bottom of the editor. You can limit the number of characters in your content using [maxLength](https://help.syncfusion.com/api/js/ejrte#members:maxlength) property. By default, the editor sets the characters limit value as 7000 characters.

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            showFooter: true,
            showWordCount: true,
            showCharCount: true,
            maxLength: 500
        });
    });
}  


{% endhighlight %}

N> The editor counts the characters by including the space, and this validation occurs while pasting the content into the editor also.

## Clear Format

The clear format tool is useful to remove all formatting styles (such as bold, italic, underline, color, superscript, subscript, and more) from currently selected text. As a result, all the text formatting will be cleared and return to its default formatting styles. When you set the [showClearFormat](https://help.syncfusion.com/api/js/ejrte#members:showclearformat) property to true, the clear format tool will be displayed at bottom of the editor.

{% highlight javascript %}

<textarea id="rteSample"></textarea>


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
        showFooter:true,
        showClearFormat:true
    });
 });
}
{% endhighlight %}

## Resize Handle

When you set the [enableResize](https://help.syncfusion.com/api/js/ejrte#members:enableresize) property to true, resize handle will be displayed at bottom-right corner of the editor. You can drag the handle to change its size. On resizing, the editor will automatically adjust the toolbar, content area, and footer within it accordingly. Resize limits can be defined via [minHeight](https://help.syncfusion.com/api/js/ejrte#members:minheight), [maxHeight](https://help.syncfusion.com/api/js/ejrte#members:maxheight), [minWidth](https://help.syncfusion.com/api/js/ejrte#members:minwidth), and [maxWidth](https://help.syncfusion.com/api/js/ejrte#members:maxwidth) properties. You can specify the size of the editor programmatically through the [height](https://help.syncfusion.com/api/js/ejrte#members:height) and [width](https://help.syncfusion.com/api/js/ejrte#members:width) properties. 

{% highlight html %}

<textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
        showFooter:true,
        enableResize:true,
        width:600,minWidth:250,maxWidth:750,
        height:300,minHeight:250,maxHeight:500
    });
  });
}

{% endhighlight %}

N>  1.	As resizable option will be added in the footer of RTE, so set the showFooter property also as “true”.   <BR>
2.	In order to showcase only the resizer, disable the other properties in the Footer such as showClearFormat,  showClearFormat,  showCharCount, showWordCount <BR> 
3.	When you set the enableRTL property to true, the resize handle will automatically positioned to the bottom-left corner of the editor. <BR>

## Characters Count/Word Count

The editor automatically counts the number of characters and words in the content while you type. The characters and words count displayed at the bottom of the editor. You can limit the number of characters in your content using [maxLength](https://help.syncfusion.com/api/js/ejrte#members:maxlength) property. By default, the editor sets the characters limit value as 7000 characters.

{% highlight html %}

    <textarea id="editor"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                showFooter: true,
                showWordCount: true,
                showCharCount: true,
                maxLength: 500
            });
     });
 }

{% endhighlight %}

By clicking the Characters Count/Word Count labels in footer , The word and character count information dialog is opened. It contains the details of the number of words and characters with and without spacing.  

![](UserInterface_images/wordchar.png)

N> The editor counts the characters by including the space, and this validation occurs while pasting the content into the editor also.