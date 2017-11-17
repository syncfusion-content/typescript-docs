---
title: Thumbnail Compression | FileExplorer | JavaScript | Syncfusion
description: Thumbnail image size reduction option in FileExplorer
platform: Typescript
control: FileExplorer
documentation: UG
keywords: Thumbnail compression, image compression, reduce image size
---

# Thumbnail Compression

The “FileExplorer” allows thumbnail images to be compressed on the server side and loaded into the “FileExplorer” layout to improve performance when working with large size images.

You can enable this option using “**enableThumbnailCompress**” API of FileExplorer. Refer following code block that will be helpful to you.

  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ExplorerComponent {
    $(function () {
        var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/webapi/FileExplorer/FileBrowser/";
        var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/fileoperation/doJSONAction";
        var file = new ej.FileExplorer($("#fileExplorer"), {
            path: fileSystemPath,
            ajaxAction: ajaxActionHandler,
            width: "100%",
            layout: "tile",
            enableThumbnailCompress: true
        });
    });
 }

 {% endhighlight %}



N> In server side, don’t forget to add “[GetImage](https://help.syncfusion.com/cr/cref_files/aspnetmvc/ejmvc/Syncfusion.EJ~Syncfusion.JavaScript.FileExplorerOperations~GetImage.html)” handling operation that helps to reduce the image size before loading.
