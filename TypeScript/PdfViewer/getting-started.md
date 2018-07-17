---
title: Getting Started for Typescript PDF viewer
description: PDF viewer 
platform: Typescript
control: PDF viewer
documentation: ug
keywords: ejPdfViewer, PDF viewer, js pdfviewer
---

# Getting Started

This section explains briefly about how to integrate a PDF viewer control in your TypeScript web application.

For common steps to create a project in typescript, you can refer [here](https://help.syncfusion.com/js/typescript).

The default type definition file ej.web.all.d.ts needs to be included the support for type-checking while initializing any of the Syncfusion widgets. 

The important step you need to do is to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (app.ts file), so that you will get the intelliSense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the jquery.d.ts file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

## Script and CSS Reference

Add the scripts and CSS references to the “index.html” page in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
    <script src="https://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    <script src="app.js"></script>
</head>
<body>
</body>
</html>

{% endhighlight %}

N> 1. In production, we highly recommend you to use our [`custom script generator`](http://help.syncfusion.com/js/custom-script-generator) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [`GZip compression`](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server.

N> 2. For themes, you can use the `ej.web.all.min.css` CDN link from the code snippet given. To add the themes in your application, please refer to [`this link`](http://help.syncfusion.com/js/theming-in-essential-javascript-components).


### Control Initialization

Add a `div` container to render the PDF viewer control.

{% highlight html %}

<!DOCTYPE html>
<html>    
     <body>
         <div id="pdfviewer1"></div>
     </body>
</html>

{% endhighlight %}

Initialize the PDF viewer in app.ts file by using the `ej.PdfViewer` method.

{% highlight html %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module PdfViewerComponent {
    $(function () {
        var viewer = new ej.PdfViewer($("#pdfviewer1"), {
            serviceUrl: "http://js.syncfusion.com/ejservices/api/PdfViewer",
            isResponsive: true
        });
    });
}

{% endhighlight %}


N> Default PDF document will be rendered in the PDF viewer control, which is used in the online service.

![](getting-started_images/pdfviewer.png)

