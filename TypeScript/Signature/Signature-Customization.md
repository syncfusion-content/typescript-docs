---
layout: post
title:  signature customization
description:  signature customization
platform: Typescript
control: Signature
documentation: ug
---

# Signature Customization

## Background color

Signature widget allows you to set the background Color for the control using the **backgroundColor** property. When we set our required background, then the signature’s background color will be changed automatically.

The following code example is used to render the Signature control with background color

Add the following script to render signature with customized background color.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
                 backgroundColor:"#808080"
                  });
        });
  }
{% endhighlight %}

The following screenshot illustrates the Signature with custom defined background color.

![](Signature_Customization_images\backgroundcolor_img1.png)

## Background Image

Signature widget allows you to set the background image for the control using the **backgroundImage** property. When we set our required background image, then the signature’s canvas will be changed with the given image.

The following code example is used to render the Signature control with customized background image.

Add the following script to render signature with customized value.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
                backgroundImage: "image.jpg"
                 });
        });
}


{% endhighlight %}

The following screenshot illustrates the Signature with custom defined background image.

![](Signature_Customization_images\backgroundimage_img1.png)


## Stroke color

Signature widget allows you to set the stroke color for the signature stroke using the **strokeColor** property. When we set our required color, then the signature’s stroke color will be changed.

The following code example is used to render the Signature control with stroke color.

Add the following script to render signature with customized stroke color.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), { 
                strokeColor: "red"
             });
        });
 }

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined stroke color.

![](Signature_Customization_images\strokecolor_img1.png)

## Stroke Width

Signature widget allows you to set the stroke width for the control using the **strokeWidth** property. When we set our required width, then the signature’s stroke width will be changed.

The following code example is used to render the Signature control with maximum stroke value.

Add the following script to render signature with customized stroke width.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SignatureComponent {
    $(function () {
        var basicSignature = new ej.Signature($("#signature"), {
                 strokeWidth: 4
            });
        });
   }

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined stroke maximum value.

![](Signature_Customization_images\strokewidth_img1.png)