---
layout: post
title: Image and File browser in RichTextEditor widget for Syncfusion Essential JS
description: Configuring and working with Image and File browser in RichTextEditor  
platform: typescript
control: RTE
documentation: ug
keywords: RichTextEditor, File browser, Image, Image Browser
---

# Image and File browser

The editor allows you to manage the images and files using **FileExplorer**. The FileExplorer enables you to insert images from online source as well as local computer where you want to insert the image in your content. The Image and file browser is the ability to upload pictures and link file to the editor. 

## Insert a Image from Online Source

If you want to insert an image from online source like Google, Ping, etc., you need to enable images tool on the editor’s toolbar. By default, the images tool is open a simple dialog which allows you to inserting an image from online source.

{% highlight html %}

<textarea id="rteSample"></textarea>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            toolsList: ["images"],
            tools: {
                images: ["image"]
            }
        });
    });
}
{% endhighlight %}

![](ImageandFilebrowser_images/ImageandFilebrowser_img1.png)


## Insert a Image from Your Computer

Configure the imageBrowser and fileBrowser property to insert an image from your computer. You can specify the settings required by the FileExplorer for create, read, upload, and destroy the files and images from the explorer. 

{% highlight html %}

<textarea id="rteSample"></textarea>

    var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONAction";

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            toolsList: ["images"],
            tools: { images: ["image"] },
            imageBrowser: {
                filePath: "http://mvc.syncfusion.com/OdataServices/FileBrowser/",
                ajaxAction: fileService,
                extensionAllow: "*.png, *.gif, *.jpg, *.jpeg"
            },

            fileBrowser: {
                filePath: "http://mvc.syncfusion.com/OdataServices/FileBrowser/",
                ajaxAction: fileService,
                extensionAllow: "*.txt, *.pdf"
            }
        });

    });
}

{% endhighlight %}

![](ImageandFilebrowser_images/ImageandFilebrowser_img2.png)

N> FileExplorer component has been implemented and integrated with the editor in Volume 1, 2015 release. For more information about FileExplorer component, see [here](https://help.syncfusion.com/js/fileexplorer/overview#).

## Image Properties

You can set or modify properties of an image using the image dialog. It allows you to add links to images, apply border and additional styles. The editor provides option to specify the alternate text for an image, if the image cannot be displayed.

![](ImageandFilebrowser_images/ImageandFilebrowser_img3.png)


## Resize an Image

You can able to resize an image either manually or set the width and height in the image dialog. 

### Resize Manually

You can resize an image by manually select an image, and drag a handle until the image is the desired size. 

![](ImageandFilebrowser_images/ImageandFilebrowser_img4.png)

N> Set the default height and width of the Images which was inserted into the RTE text area in “change” event of RTE - {{'[Link](http://jsplayground.syncfusion.com/Sync_rghpsadi)'| markdownify }}

### Set Width and Height

The editor provides you to set the width and height properties to change the size of an image (rather than forcing you to set in style attributes) using [showDimensions](https://help.syncfusion.com/api/js/ejrte#members:showdimensions) property. By default, the Constrain Proportion checkbox is selected to resize an image to an exact proportion. To apply the exact width and height that you specify into the Height and Width textboxes, uncheck the Constrain Proportions checkbox.

{% highlight html %}

<textarea id="rteSample"></textarea>


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RTEComponent {
    $(function () {
        var sample = new ej.RTE($("#rteSample"),{
            toolsList: ["images"],
            tools: { images: ["image"] },
            showDimensions: true
        });
   });
}

</script>
{% endhighlight %}

![](ImageandFilebrowser_images/ImageandFilebrowser_img5.png)

## Suppression of the Image Browser

The General and Advanced tabs in the RTE Image browser can be removed by setting its corresponding display CSS property to none.

{% highlight CSS %}

    <style type="text/css" class="cssStyles">
        div.e-rte-imageTab.e-tab.e-js.e-widget {
            display: none;
        }
    </style>

 {% endhighlight %}
 
 Can remove the Add `NewFolder` button by using [removeToolbarItem](https://help.syncfusion.com/api/js/ejrte#methods:removetoolbaritem) property of Image Browser in the RTE create event. 

{% highlight html %}

    <textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px">
        Description:
        The Rich Text Editor (RTE) control is an easy to render in
        client side.Customer easy to edit the contents and get the HTML content for
        the displayed content.A rich text editor control provides users with a toolbar
        that helps them to apply rich text formats to the text entered in the text
        area.
    </textarea>
    var sample = new ej.RTE($("#rteSample"),{
            toolsList: ["images"],
            tools: { images: ["image"] },
            width: "100%",
            minWidth: "10px",
            imageBrowser: { filePath: "http://mvc.syncfusion.com/OdataServices/FileBrowser/", ajaxAction: fileService, extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx", ajaxSettings: ajaxSettings },
            fileBrowser: { filePath: "http://mvc.syncfusion.com/OdataServices/FileBrowser/", ajaxAction: fileService, extensionAllow: "*.txt, *.png, *.pdf,*.jpeg", ajaxSettings: ajaxSettings1 },
            create: function (args) {
                this._explorerObj.removeToolbarItem("NewFolder");
            }
   });

{% endhighlight %}