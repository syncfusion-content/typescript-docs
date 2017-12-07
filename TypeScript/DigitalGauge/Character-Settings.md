---
layout: post
title: Character-Settings
description: character settings
platform: typescript
control: Digital Gauge
documentation: ug
---

# Character Settings

## Appearance

You can customize the character using `character settings`The opacity of the character is adjustable with the help of `opacity` property. The space between two characters are adjusted with `spacing` property as like in the segment settings.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module DigitalGaugeComponent {

  $(function () {
        // For Digital Gauge rendering
       var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
            width: 800,
            items: [{
                // For setting text
                value: " Syncfusion ",
                characterSettings: {
                    // For setting character opacity
                    opacity: 0.3,
                    // For setting character spacing
                    spacing: 3
                }
            }]
        })
    });
}

{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](Character-Settings_images/Character-Settings_img1.png)

## Count and Type

The number of text to be displayed can be limited by the attribute called `count`. In **Digital Gauge** five different `types` of characters are supported. They are as follows, 

  * EightCrossEightDotMatrix

  * SevenSegment

  * FourteenSegment

  * SixteenSegment 

  * EightCrossEightSquareMatrix.


{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
       var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
            width: 800,
            items: [{
                // For setting text
                value: "1234567890",
                segmentSettings: {
                    // For setting segment length
                    length: 8,
                    // For setting segment width
                    width: 1
                },
                characterSettings: {
                    // For setting character count
                    count: 10,
                    // For setting segment spacing
                    spacing: 10,

                    // For setting character type
                    type: "sevensegment",
                }
            }]
        })
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](Character-Settings_images/Character-Settings_img2.png)

## Text Positioning

The text in the **Digital****Gauge** is positioned with `position` object. This object contains two attributes such as `x` and `y`. The `x` variable positions the text in the horizontal axis and the `y` variable positions the text in the vertical axis.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
            width: 800,
            height:300,
            frame: {
                backgroundImageUrl: "Board1.jpg"
            },
            items:[{
                // For setting text
                value: "YELLOW",
                // For setting segment color
                segmentSettings: { color: "Yellow" },
                position:{
                    // For setting segment x location
                    x:80,
                    // For setting segment y location
                    y:10
                }
            }]
        });
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.


![](Character-Settings_images/Character-Settings_img3.png)

## Shadow Effects

You can add the shadow effects for text using following properties.

* You can enable/disable the blurring effect for the shadows of the text using `shadow blur` property.

* You can specify the color of the text shadow using `shadow color` property.

* You can set the `x-offset` value for the shadow of the text, indicating the location where it needs to be displayed.

* You can set the `y-offset` value for the shadow of the text, indicating the location where it needs to be displayed.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Digital Gauge rendering
       var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
            width: 800,
            items: [{
                //For setting Text
                value: "WELCOME",
                //For setting segment length and width
                segmentSettings: {
                    length: 3,
                    width: 3
                },
                //For setting shadow color
                shadowColor: "yellow",
                //For setting shadow Blur
                shadowBlur: 20,
                //For setting horizontal offset
                shadowOffsetX: 15,
                //For setting vertical offset
                shadowOffsetY: 15,
            }]
        });
    });

{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](Character-Settings_images/Character-Settings_img4.png)

## Font Customization

You can customize the `font` of the text as per your requirement. To customize the font, you have to set `enableCustomFont`. Following font customization options are available.

* `Font-family`- used to set the font-family of the text.

* `Font-style`- used to set the font-style of the text.

* `Font-size`- used to set the font-size of the text.

{% highlight html %}

<div id="DigitalCore"></div> 

{% endhighlight %}

{% highlight javascript %}
 
$(function () {
  var digitalGaugeSample = new ej.datavisualization.DigitalGauge($("#DigitalCore"),{items: [{enableCustomFont: true ,font: { fontFamily: "Segou", fontStyle: "bold", size: "18px"}}]});
});

{% endhighlight %}
