---
layout: post
title: File-Size
description: file size 
platform: Typescript
control: Uploadbox
documentation: ug
---

# File Size 

## Maximum File Size for Uploadbox

In the **Uploadbox** control, you can browse files with the size going up to gigabytes. You can restrict the files from being browsed using the **fileSize** property. When you do not use this property, it takes a default size, 31457280B, that is, 31MB.When this size exceeds, you cannot browse the file. 

Add the following code example to the corresponding **HTML** page to render the **Uploadbox** control with the customized file size.



{% highlight html %}

<div class="control">
     <div id="Uploadbox"></div>
</div>

{% endhighlight %}



Initialize the **Uploadbox** using the following code example.



{% highlight js %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module UploadboxComponent {
    $(function () {
        var sample = new ej.Uploadbox($("#Uploadbox"),{
        saveUrl: "save.ashx",
        removeUrl: "removeFiles.ashx",
        error: "error",
        fileSize: 1048576 //bytes
    });
} 
    function error(e, ui) {
        alert(e.error);
    }


{% endhighlight %}



To know about file action, we need to refer link:

<https://help.syncfusion.com/js/uploadbox/file-actions>

The following screenshot displays **Uploadbox** control with customized file size.

When you want to browse the file within the fileSize, you can browse and upload the files.



![](/js/UploadBox/File-Size_images/File-Size_img1.png) 

When you try to browse the file with exceeded fileSize, we cannot browse and upload the files.



![](/js/UploadBox/File-Size_images/File-Size_img2.png) 

## Maximum File Upload Size in IIS

By default, the IIS web server allows for limited file size to be uploaded to the web server. By default, **Machine.config** is configured to accept HTTP Requests up to 4096 KB, that is, 4 MB. 

### How to upload files up to 28.6 MB?

In order to allow larger file size uploads, such as above 4MB, you can override it by modifying the “maxRequestLength” attribute in the web application’s configuration file **web.config**. The property _**maxRequestLength**_ indicates the maximum file upload size of 28.6MB, supported by ASP.NET. You cannot upload the files when the **fileSize** property is below the **maxRequestLength** value.



Property

<table>
<tr>
<th>
Use-Case Description</th><th>
Type</th><th>
Maximum request size</th><th>
Details</th></tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/system.web.configuration.httpruntimesection.maxrequestlength.aspx">maxRequestLength</a></td><td>
Property</td><td>
28.6 MB</td><td>
Maximum request size supported by ASP.NET.</td></tr>
</table>


Add the following code to your **web.config** file. 

{% highlight c# %}

[web.config]
<configuration>
    <system.web>
        <httpruntime maxRequestLength="102400"/> //kilobytes 
    </system.web>
</configuration>


{% endhighlight %}



N> maxRequestLength is measured in kilobytes.


### How to upload the files above 28.6 MB?

The **maxRequestLength** property can be increased by modifying the “maxAllowedContentLength” attribute in the web application's configuration file **web.config**. The default maximum length of the content in a request supported by IIS is around 28.6 MB or 30000000bytes.

Property

<table>
<tr>
<th>
Use-Case Description</th><th>
Type</th><th>
Default value</th><th>
Details</th></tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms689462(v=vs.90).aspx">maxAllowedContentLength</a></td><td>
Property</td><td>
28.6 MB</td><td>
maxAllowedContentLength specifies the maximum length of content in a request supported by IIS.</td></tr>
</table>


You can add the following code to your **web.config** file in order to set that value to 100 MB.

{% highlight c# %}

[web.config]
<system.webServer>
    <security>
        <requestFiltering>
            <requestLimits maxAllowedContentLength="104857600" /> //bytes
        </requestFiltering>
    </security>
</system.webServer>


{% endhighlight %}



N> maxAllowedContentLength is measured in bytes.


![](/js/UploadBox/File-Size_images/File-Size_img4.png) 
                       

N> * When you configure both maxAllowedContentLength, maxRequestLength attributes, then maxAllowedContentLength is considered for execution.
N> * When the upload file’s size exceeds maxAllowedContentLength, you get a 404.13 error page.
N> * When the upload file’s size exceeds maxRequestLength value, you get an exception “System.Web.HttpException: Maximum request length exceeded”.
N> * The ASP.NET method of maxRequestLength is greater than or equal to the IIS method of limiting the request length (maxAllowedContentLength).
