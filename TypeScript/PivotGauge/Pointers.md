---
layout: post
title: Pointers
description: pointers
platform: Typescript
control: PivotGauge
documentation: ug
---

# Pointers

## Pointer Types

PivotGauge pointers has two types such as,

* Needle
* Marker

Needle type pointers are the default pointers which is always located at the center of the Gauge. Following shapes that are supported for the needle pointers are:

* Rectangle
* Triangle
* Trapezoid
* Arrow
* Image.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [{
                        type: "needle",
                        needleType: "trapezoid"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/NeedlePointer.png) 

For marker pointer, the available shapes are Rectangle, Triangle, Ellipse, Diamond, Pentagon, Circle, Slider, Pointer, Wedge, Trapezoid, RoundedRectangle and Image.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [{
                        type: "marker",
                        markerType: "diamond"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/MarkerPointer.png) 

## Adding Pointer Collection

Pointer collection can be directly added to the scales option within the PivotGauge control. 

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [{
                        type: "needle",
                        needleType: "triangle"
                    },
                    {
                        type: "marker",
                        markerType: "diamond"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/PointerCollection.png) 

## Appearance Customization

The appearance of the pointer can be customized through the following properties.

* **border** – sets the "Color" and "Width" of the pointer border.
* **backgroundColor** – sets the background color of the pointer.
* **length** – sets the length of the pointer.
* **width** – sets the width of the pointer.
* **opacity** – sets the opacity of the pointer.  By default, the value is 1.
* **type** – sets the type of the pointer.  By default, the type is "Needle".

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [{
                        border:{
                            color: "green",
                            width:2
                        },
                        backgroundColor: "yellow",
                        length:120,
                        width:7,
                        opacity:0.6,
                        type: "needle",
                        needleType: "triangle"
                    },
                    {
                        border:{
                            color: "green",
                            width:2
                        },
                        backgroundColor: "yellow",
                        length:25,
                        width:15,
                        opacity:0.8,
                        type: "marker",
                        markerType: "diamond"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/AppearanceCustomization.png) 

## Pointer Position

Pointer can be positioned with the help of below two properties.

* **distanceFromScale** -  defines the distance between scale and pointer. By default, the value is 0.
* **placement** -  defines the location of the pointer. By default, the value is "Center".

N> Both the properties can be applied only if the pointer type is set to “Marker”. Needle pointer type appears only at the center of the control, which is its default position.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [
                    {
                        type: "marker",
                        distanceFromScale: 2,
                        placement: "far"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/PointerPosition.png) 

## Pointer Image

It is possible to replace the pointers with image. To view the pointers as image, we need to set the appropriate location in the `imageUrl` property.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [
                    {
                        type: "needle",
                        needleType: "image",
                        imageUrl:"../image.png"
                    },
                    {
                        type: "marker",
                        markerType: "image",
                        imageUrl:"../image.png"
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/MarkerPointerWithImage.png)

## Pointer Value Text

To display the current value of the pointers in PivotGauge control, **"pointerValueText"** option inside pointers is used.  Following are the properties used to enable and customize the pointer value text.
 
* **showValue** – enables the pointer value text by setting the property to "true". By default, its value is "true".
* **distance** – sets the distance between pointer and text.
* **color** – sets the color of the text.
* **opacity** – sets the opacity of the text. By default, its value is 1.
* **angle** – sets the rotation angle of the text. By default, its value is 0.
* **font** – sets the font size, font style and font family of the text.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotGauge($("#PivotGauge1"), {
        scales: [{
            pointers: [
                    {
                        type: "needle",
                        pointerValueText:{
                            showValue: true,
                            distance: 10,
                            color: "red",
                            opacity: 70,
                            angle: 20,
                            font:{
                                fontFamily: "Arial",
                                fontStyle: "Normal",
                                size: "15px"
                            }
                        }
                    },
                    {
                        type: "marker",
                        pointerValueText:{
                            showValue: true,
                            distance: 40,
                            color: "red",
                            opacity: 70,
                            angle: -40,
                            font:{
                                fontFamily: "Arial",
                                fontStyle: "Normal",
                                size: "15px"
                            }
                        }
                    }]
        }]
    });
});	

{% endhighlight %}

![](Pointers_images/PointerValueText.png) 
