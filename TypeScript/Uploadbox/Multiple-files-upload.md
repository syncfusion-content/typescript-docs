---
layout: post
title: Multiple-files-upload
description: multiple files upload
platform: Typescript
control: Uploadbox
documentation: ug
---

# Multiple files upload

The **Uploadbox** widget provides support to upload multiple files spontaneously. The **multipleFilesSelection** property enables you to select multiple files while browsing.  To achieve this, set the **multipleFilesSelection** property to ‘**true**’. The data type is **Boolean**.

N> The Multiple file selection supports all the latest versions of browser except Internet Explorer 9 and its previous versions.



The following steps explain the configuration of **multipleFilesSelection** property in **Uploadbox**. 

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.


{% highlight html %}

<div class="control">
    <div id="Uploadbox"></div>
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module UploadboxComponent {
    $(function () {
        var sample = new ej.Uploadbox($("#Uploadbox"),{
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            multipleFilesSelection: true
        });
    });
}
{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



![](Multiple-files-upload_images/Multiple-files-upload_img1.png)



![](Multiple-files-upload_images/Multiple-files-upload_img2.png)

