---
layout: post
title:  how to
description:  how to
platform: Typescript
control: Signature
documentation: ug
---

##  How To

### Save signature image with user defined format

By default, the downloaded image from the signature canvas will be in **png** format. We can define our own format to download the image with **saveImageFormat** property. And we can also save the image along with the background by using the **saveWithBackground** property.

The following code example is used to download drawn image on the Signature control.

{% highlight html %}

<div id="signature"></div>

<input id="save" type="button" value="save" />

{% endhighlight %}

Add the following script to define the download format for the canvas

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
                height: "500px",
                saveWithBackground: true,
                strokeWidth: 3,
                saveImageFormat :"jpg",
                backgroundImage: "../content/images/progressbar/water.png",

            });
          var button = new ej.Button($("#signSave"), {
                size: "normal", width: "70px",
                showRoundedCorner: true,
                click: onSave
            });
        });
  }
      function onSave(args) {
            var signature = $("#signature").ejSignature("instance");
            signature.save("MySignature");
        }


{% endhighlight %}

The following screenshot illustrates the Signature with saving (downloading) the drawn image.

![](How_To_images\savesignatureimagewithuserdefinedformat_img1.png)

### To clear the Signature

To clear the signature, you can simply use the **clear()** method. This method will clear all the drawn strokes in the signature canvas and leaves it empty.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
                height: "500px",
                strokeWidth: 3

            });
       var button = new ej.Button($("#signatureClear"), {
                size: "normal", width: "70px",
                showRoundedCorner: true,
                click: "onClear"
            });
        });
   }
      function onClear(args) {
            var signature = $("#signature").ejSignature("instance");
            signature.clear();
        }

{% endhighlight %}

### Make signature as responsive

When the signature control is resized or even the window is resized the strokes drawn in the signature will be disappeared. To make the strokes visible even after resizing the window, we must set the **isResponsive**property as true.

The following code example is used to render the Signature control with responsive support.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
            isResponsive: true
        });
    });
}  

{% endhighlight %}

The following screenshot illustrates the Signature with responsiveness.

Before Responsiveness:

![](How_To_images\makesignatureasresponsive_img1.png)


After giving the Responsiveness:

![](How_To_images\makesignatureasresponsive_img2.png)


### To check whether any input to the signature control since render

We can detect whether not there has been any input to the signature control since render. To detect we can use the storeSnap public variable, which is an array that stores all the canvas inputs. At initial rendering this array is empty and we can use this variable to check for the drawn strokes.


{% highlight js %}

      var signature  = new ej.Signature($("#signature"), { });

            if (ej.isNullOrUndefined(signature.storeSnap)) {

                //Something

            }

{% endhighlight %}