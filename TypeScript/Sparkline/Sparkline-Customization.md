---
layout: post
title: Customization for Essential Javascript Sparkline
description: Learn how to customize the Sparkline .
platform: ts
control: Sparkline
documentation: ug
---

# Sparkline Customization

This section explains you the customization options available to make changes in the Sparkline for getting better appearance.

## Sparkline background

You can specify the background color for the Sparkline using **background** property. When you don't specify the **background**, it takes "transparent" as background color. 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
           // ...
            //Specifies background color for sparkline
            background : "gray"
            // ...
            
       });
    });
}

{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img1)

## Stroke color and width

You can customize the series border color and width using **stroke** and **width**. This is applicable for Sparkline types line and area.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            //Specifies border color and width for line and area series
            stroke: "green",
            width: 3
            // ...
       });
    });

{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img2)

## Sparkline border

You can customize the **border** width and height of the Sparkline using **border width** and **border height** properties. This is applicable for column, win-loss and pie series.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            //Specifies border width and color for column, winLoss and pie series
            border: { color: "green", width: 2 },
            // ...
       });
    });
           
{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img3)

## Opacity

By default **opacity** of the Sparkline is 1. You can specify the opacity value from 0 to 1. This is applicable for all types of series. 

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            //..
             //Specifies the opacity of the sparkline
            opacity: 0.5
            // ...
       });
    });
        
{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img4)

## Localization

Sparkline is having support for localization as well. Default culture is "en-US". You can modify the culture using the property **locale**.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
            // ...
            //Culture for the sparkline
            culture: "fr-FR"
            // ...
       });
    });

{% endhighlight %} 

## Padding for Sparkline

**Padding** is used to specify the padding value between the container and Sparkline. By default padding value of the Sparkline is 5. 

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
             // ...
            //Padding for the sparkline
            padding: 20,
            // ...
       });
    });

{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img5)

## Canvas support

You can control whether Sparkline has to be rendered as SVG or **Canvas**. Canvas rendering supports all the functionalities supported in SVG rendering.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
              // ...
            //enables canvas rendering
            enableCanvasRendering : true
            // ...
       });
    });

{% endhighlight %} 

## Themes

You can specify different **themes** for Sparkline control.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
             // ...
            //theme for sparkline
            theme:"flatdark",
            // ...
       });
    });

{% endhighlight %} 

![](Sparkline-Customization_images/Sparkline-Customization_img6)
