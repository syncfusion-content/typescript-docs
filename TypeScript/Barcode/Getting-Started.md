---
layout: post
title: Getting started with Syncfusion Essential Barcode for TypeScript
description: Getting started walk through to create your first Barcode.
platform: TypeScript
control: ejBarcode
keywords: Barcode, typescript ejBarcode
---

# Overview

The Syncfusion Essential JS Barcode widget enables rendering of one dimension and two dimension barcodes in web page. Barcode provides you a simple and inexpensive method of encoding text information that can be easily read by electronic readers.

**Key Features**

* Supports 10 one-dimensional barcodes including Code 39 and Code 32 barcodes.
* Supports 2 two-dimensional barcodes such as QR and Data Matrix barcodes.

# Getting Started

**Essential JavaScript Barcode** widget provides support to create Barcode within your web page. This section explains briefly about how to create an **Barcode** in your application with **Typescript.** 

## Create Barcode in Typescript

Create an HTML page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

      <!DOCTYPE html>
      <html>
      <head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
      </head>
      <body>
      </body>
      </html>

{% endhighlight %}

Create a **Barcode** element within the body of the HTML document where the widget needs to be rendered.

{% highlight html %}

    <div id="targetElement">
        <div id="Barcode"></div>
    </div>

{% endhighlight %}

Initialize the Barcode in ts file by using the `ej.datavisualization.Barcode` method.

{% highlight html %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module Barcodecomponent {
    $(function () {
        var barcodesample = new ej.datavisualization.Barcode($("#Barcode"), {
            text:"http://www.syncfusion.com"
        });
    });
}

{% endhighlight %}

The following screenshot illustrates the output of the above code example.

![](getting-started-images/default.png)
