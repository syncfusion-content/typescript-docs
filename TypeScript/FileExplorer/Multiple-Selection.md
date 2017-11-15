---
layout: post
title: Multiple Selection
description: FileExplorer allows the user to select multiple files
platform: Typescript
control: File Explorer
documentation: ug
---


# Multiple Selection

The FileExplorer allows the user to select multiple files by enabling the [allowMultiSelection](https://help.syncfusion.com/api/js/ejfileexplorer#members:allowmultiselection) property. The multiple selection can be done by pressing the **Ctrl** key or **Shift** key. You can select all the files in the directory by pressing “**Ctrl + A**”. The multiple selection is useful on copy pasting multiple files, deleting multiple files and downloading multiple files.

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

                allowMultiSelection: false

            });

        });
    }

{% endhighlight %}

