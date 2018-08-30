---
title: Drag and Drop Support | FileExplorer | JavaScript | Syncfusion
description: Drag and Drop option in FileExplorer
platform: Typescript
control: FileExplorer
documentation: UG
keywords: Drag and drop option
---

# Drag and Drop Support

The FileExplorer allows files to be moved from one folder to another by using drag and drop. It also supports uploading a file by dragging it from Windows Explorer to a folder in the FileExplorer control.

You can enable or disable this support by using “**allowDragAndDrop**” API of FileExplorer.

The [dragStart](https://help.syncfusion.com/api/js/ejfileexplorer#events:dragstart), [drag](https://help.syncfusion.com/api/js/ejfileexplorer#events:drag), [dragStop](https://help.syncfusion.com/api/js/ejfileexplorer#events:dragstop) and [drop](https://help.syncfusion.com/api/js/ejfileexplorer#events:drop) events occur in the mentioned order when a drag and drop operation is performed.

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

                allowDragAndDrop: false

            });

        });
  }

{% endhighlight %}

