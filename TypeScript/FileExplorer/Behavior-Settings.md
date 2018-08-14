---
layout: post
title: Behavior Settings
description: Customize the behavior of FileExplorer.
platform: Typescript
control: FileExplorer
documentation: ug
---

# Behavior Settings

Here are the some properties to customize the behavior of FileExplorer.

## File type restriction

FileExplorer control showcase all the files from the filesystem, here you can customize the file types that what you want to show by using [fileTypes](https://help.syncfusion.com/api/js/ejfileexplorer#members:filetypes) property. It filter the files based on the files extensions.

By default it having the value “*.*”, so it allows all the file types. In case of image browser you can allow the image files only by setting "*.png, *.gif, *.jpg, *.jpeg", so it doesn’t allow the other type of files.

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

            fileTypes: "*.png, *.gif, *.jpg, *.jpeg"

        });
    });
 }

{% endhighlight %}

## Customize the AJAX request settings

As you already know FileExplorer is a client – server based control and each action performed in the client sends an AJAX request to the server to perform the server side operations. While the AJAX request, the AJAX configurations can be customized through [ajaxSettings](https://help.syncfusion.com/api/js/ejfileexplorer#members:ajaxsettings) property.

The [beforeAjaxRequest](https://help.syncfusion.com/api/js/ejfileexplorer#events:beforeajaxrequest) event will be triggered before the AJAX request is performed. You can modify the ajax request in this event.

You can see the following requests passed during the **client – server actions**:

* Read, 
* Create folder
* Remove
* Rename
* Paste
* Get details
* Upload
* Download 
* Get Image

The following is the syntax for ajaxSettings property.

{% highlight javascript %}

       ajaxSettings: { read: {}, createFolder: {}, remove: {}, rename: {}, paste: {}, getDetails: {}, upload: {}, download: {}, getImage: {} }
                
{% endhighlight %}

The actions “read, createFolder, remove, rename, paste, getDetails” are supported all the jQuery AJAX configurations. The remaining actions “upload, download, getImage” are accepted the URL only.

If you want to customize read action alone, the AJAX **url** and **dataType** are changed for the read action, refer the below code example.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ExplorerComponent {
    $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            var ajaxJSONPActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperationsCors";

            var file = new ej.FileExplorer($("#fileExplorer"), {

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                ajaxSettings: {

                    read: {

                        url: ajaxJSONPActionHandler,

                        dataType: "jsonp"

                    }

                }

            });

        });
    }
{% endhighlight %}


For following file actions, you have to make the custom request in URL format only, not able to use jQuery AJAX configurations as like "dataType", "contentType", "async", etc..

* upload
* download
* getImage

Also its compulsory to add "{0}" in the end of "upload, download and getImage" URL's. That helps to pass the internal parameters with the action request.

{% highlight javascript %}

       ajaxSettings: {
            upload: {
                url: ajaxActionHandler + "/upload{0}"
            },
            download: {
                url: ajaxActionHandler + "/download{0}"
            },
            getImage: {
                url: ajaxActionHandler + "/getImage{0}"
            }
      }

{% endhighlight %}

N> **ajaxActionHandler** - prefix URL of AJAX handling method
