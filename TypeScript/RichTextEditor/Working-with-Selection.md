---
layout: post
title: Working with content selection in RichTextEditor widget
description: Working with content selection in RichTextEditor widget
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, Selection, Select a Range
---
# Working with Selection

The editor control provides option to select all the content and in addition to selection of a particular range of content. 

## Select All 

The [selectAll](https://help.syncfusion.com/api/js/ejrte#methods:selectall) method enables you to select the entire content including images in the editor by programmatically.

N> the selection highlight is invisible if the editor does not have focus. So, if you want to call the selectAll method, focus the editor before.

{% highlight html %}

    <textarea id="rteSample"></textarea>

    <button onclick="selectAll()">Select All</button>

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
        function selectAll() {
            sample.selectAll();
        }

    </script>
{% endhighlight %}

## Select a Range 

You can programmatically select a range of content in the editor using the selectRange method.  To select a range, create a range object with desired offset position and pass it as arguments to selectRange method. The range object is created from createRange method. 

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
                value: "<ul>" + "<li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>" + "<li>Aliquam tincidunt mauris eu risus.</li>" + "<li>Vestibulum auctor dapibus neque.</li>" + "</ul>"
            });
            range = sample.createRange();
            var liTag = $(sample.getDocument().body).find("li");        
            if (!sample._isIE8()) {
                range.setStart(liTag[1], 0);
                range.setEnd(liTag[2], 1);
            }
            else {
                range = sample.getDocument().body.createTextRange()
                range.moveToElementText(liTag[2]);
            }
            sample.selectRange(range);
        });
  }
{% endhighlight %}

## Get Selection

The following public methods helps you to retrieve the selected content from the editor:

* [getText](https://help.syncfusion.com/api/js/ejrte#methods:gettext) method is used to get the currently selected content as raw text.
* [getSelectedHtml](https://help.syncfusion.com/api/js/ejrte#methods:getselectedhtml) method is used to get the HTML source of currently selected content.

{% highlight html %}

    <textarea id="rteSample"></textarea>

    <button onclick="getSelection()">get Selection</button>

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
   function getSelection() {
      var selectedText = sample.getText();
      var selectedHtml = sample.getSelectedHtml();
 }

{% endhighlight %}

