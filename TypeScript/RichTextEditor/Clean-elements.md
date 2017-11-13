---
layout: post
title: Cleanup elements when copy paste from MSWord to RichTextEditor widget
description: Cleanup elements when copy paste from MSWord to RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, cleanup, paste-cleanup
---

# Clean unwanted elements and styles when copy paste from Microsoft Word

While copy pasting content from MSWord document, the content will be processed in the paste action event.[pasteCleanupSettings](https://help.syncfusion.com/api/js/ejrte#members:pasteCleanupSettings) API can be used for removing unwanted elements.
This will convert an unformatted HTML element (MOS XML format) content to a proper HTML element.Table elements also will be converted with proper elements. 
<table>
<tr>
    <th> Options <br/><br/></th>
    <th> Description <br/><br/></th>
</tr>
<tr>
    <td> {{'[listConversion](https://help.syncfusion.com/api/js/ejrte#members:pasteCleanupSettings-listconversion)'| markdownify }} <br/><br/></td>
    <td>List Conversion option convert the list elements into a proper format pasted from MSWord document to editor. <br/><br/></td>
</tr>
<tr>
    <td> {{'[cleanCSS ](https://help.syncfusion.com/api/js/ejrte#members:pasteCleanupSettings-cleanCSS )'| markdownify }} <br/><br/></td>
    <td>Clean CSS is used to clean the unwanted css in the elements pasted from MSWord document to editor <br/><br/></td>
</tr>
<tr>
    <td> {{'[removeStyles  ](https://help.syncfusion.com/api/js/ejrte#members:pasteCleanupSettings-removeStyles  )'| markdownify }} <br/><br/></td>
    <td>Remove styles will remove all styles in the elements pasted from MSWord document to editor. <br/><br/></td>
</tr>
<tr>
    <td> {{'[cleanElements   ](https://help.syncfusion.com/api/js/ejrte#members:pasteCleanupSettings-cleanElements   )'| markdownify }} <br/><br/></td>
    <td>Clean Elements is used to clean the unwanted elements pasted from MSWord document to editor.<br/><br/></td>
</tr>
</table>
 
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
           pasteCleanupSettings:{
               listConversion:true,
               cleanCSS:true,
               removeStyles:true,
               cleanElements:true
           }
    });
 });
}

{% endhighlight %}

Pasted Content before Cleanup:
![](Clean-Elements-images/beforecleanup.png)

![](Clean-Elements-images/Element1.png)

Pasted Content after Cleanup:
![](Clean-Elements-images/Aftercleanup.png)

![](Clean-Elements-images/Element2.png)