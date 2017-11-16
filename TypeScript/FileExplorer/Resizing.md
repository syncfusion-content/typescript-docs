---
layout: post
title: Resizing
description: resize support
platform: Typescript
control: File Explorer
documentation: ug
---

# Resizing 

The FileExplorer has the resize support through the resize handle which appears at right-bottom corner of footer. By clicking the resize handle the user can resize the FileExplorer through the UI. While resizing the dimension of the FileExplorer is automatically adjusted.

The resize behavior can be enabled through the [enableResize](https://help.syncfusion.com/api/js/ejfileexplorer#members:enableresize) property. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ExplorerComponent {
    $(function () {
            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            var file = new ej.FileExplorer($("#fileExplorer"), {

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // it enables the resize functionality

                // and a resize handle added in the Footer element

                enableResize: true

            });
       });
    }

{% endhighlight %}

## Responsiveness

By enabling the [isResponsive](https://help.syncfusion.com/api/js/ejfileexplorer#members:isresponsive) property, you can make the FileExplorer as responsive. While resizing the FileExplorer component, the inner content and toolbar items are automatically adjusted to equalize the size. The toolbar items are displayed within Dropdown on enabling the responsive. Otherwise it floated to the next line to equalize the space. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ExplorerComponent {
    $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            var file = new ej.FileExplorer($("#fileExplorer"), {

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // it enables the resize functionality

                enableResize: true,

                // it enables the control responsiveness

                isResponsive: true

            });

        });
  }

{% endhighlight %}

## Restriction on Resize

You can restrict the dimension of the FileExplorer by setting the [minHeight](https://help.syncfusion.com/api/js/ejfileexplorer#members:minheight), [maxHeight](https://help.syncfusion.com/api/js/ejfileexplorer#members:maxheight) and [minWidth](https://help.syncfusion.com/api/js/ejfileexplorer#members:minwidth),[maxWidth](https://help.syncfusion.com/api/js/ejfileexplorer#members:maxwidth) properties while resizing the FileExplorer. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ExplorerComponent {

    $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

             var file = new ej.FileExplorer($("#fileExplorer"), {

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                enableResize: true,

                isResponsive: true,

                // restricts the dimensions for height and width

                minHeight: "200px",

                maxHeight: "400px",

                minWidth: "300px",

                maxWidth: "1200px"

            });

        });
   }

{% endhighlight %}

