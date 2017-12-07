---
layout: post
title: Bullet-Graph-Caption
description: bullet graph caption
platform: js
control: BulletGraph	
documentation: ug
---

# Bullet Graph Caption

**Bullet Graph** supports title and **subtitle** to convey what is represented in **Bullet Graph**. They are customized using **caption settings** property.

## Title

**Title** is set to **Bullet Graph** using **text** property in **caption settings**. Caption settings also include properties like **location**, **font**, **text alignment**, **text anchor**, **text position**, **text angle** and **padding** for customizing the caption of **Bullet Graph**.

### Location

Using **location**option, you can set the **X** and **Y** position of caption text.

### Font

Using **font** property, you can customize **font color**, **font family**, **font style**, **font weight**, **opacity**, **size** options.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
         quantitativeScaleSettings: {
                        location: { x: 100, y: 200 },                   
                        minimum: 0,
                        maximum: 5,
                        interval: 0.5,
                        featureMeasures: [{ value: 4, comparativeMeasureValue: 3.5, category: "" }]
                    },
                    height: 700, width: 600,
                    captionSettings: {
                        text: "Revenue YTD",
                        textAngle: 0,
                        location: {
                            x: 10, y: 220
                        },
                        font: {
                            color: 'gray',
                            fontFamily: 'Segoe UI',
                            fontStyle: 'bold',
                            size: '14px',
                            fontWeight: 'regular',
                            opacity: 1
                        }                        
                    }
        });
    });
}

{% endhighlight %}

The following screenshot displays a **Bullet Graph** with customized caption using the above code.

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img1.png)

## Subtitle

**Subtitle** is added to **Bullet Graph** using **text**property of **subtitle** in **captionSettings**. **Subtitle** also provides properties like **location**, **font**,**text alignment**, **text anchor**, **text angle** and **padding** to customize subtitle similar to caption.

### Location

Using **location** option, you can set the **X** and **Y** position of the subtitle text in the caption settings.

### Font

Using **font** property, you can customize **font color**, **font family**, **font style**, **font weight**, **opacity**, **size** options of the subtitle text.

{% highlight javascript %}

 $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
         quantitativeScaleSettings: {
                        location: { x: 100, y: 200 },                   
                        minimum: 0,
                        maximum: 5,
                        interval: 0.5,
                        featureMeasures: [{ value: 4, comparativeMeasureValue: 3.5, category: "" }]
                    },
                    height: 700, width: 600,
                    captionSettings: {
                        text: "Revenue YTD",
                        textAngle: 0,
                        location: {
                            x: 10, y: 220
                        },
                        font: {
                            color: 'gray',
                            fontFamily: 'Segoe UI',
                            fontStyle: 'bold',
                            size: '14px',
                            fontWeight: 'regular',
                            opacity: 1
                        }                        
        });
    });

{% endhighlight %}

The following screenshot displays **Bullet Graph** with a subtitle

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img2.png)

## Indicator

You can add **Indicator** to bullet graph by enabling **visible** and setting **text** properties of **indicator** in **captionSettings**. Indicator is used to represent whether target is achieved or not with text and symbol by comparing current and target values in bullet graph. 

Indicator displays a **symbol** along with text which is different from caption and subtitle. Images like logos can be used in indicator instead of symbols. Indicator has properties such as **symbol**, **text**, **text spacing**, **text angle**, **text alignment**, **text anchor**, **text position**, **location**, **padding** and **font**.

### Location

Using **location**option, you can set the **X** and **Y** position of indicator text.

### Font

Using **font** property, you can customize **font color**, **font family**, **font style**, **font weight**, **opacity**, **size** font properties of the indicator text.

### Symbol

Using **symbol** settings, you can customize the following **symbol** properties.

* You can customize the symbol border properties **border color** and **border width** using **border** settings.

* You can specify the color of the symbol using **color** property.

* You can set the shape of the symbol using **shape** property.

* Instead of setting shape for symbol, you can use image also. To use image as symbol, you need to set **image url** for symbol.

* You can customize the **size** of the indicator symbol using **width** and **height** properties of indicator's symbol size settings. 

* To customize the opacity of the indicator symbol, you can use the **opacity**property of the symbol.

{% highlight javascript %}


$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                    captionSettings: {
                        indicator: {
                            visible: true,
                            textAngle: 0,
                            location: { x: 15, y: 240 },
                            text: "+ $0.5 K",
                            textSpacing: 5,
                            symbol: {
                                color: 'green',
                                shape: 'triangle',
                                imageURL: "Column.png",
                                size: {
                                    width: 10,
                                    height: 10
                                },
                                border: {
                                    width: 1,
                                    color: 'green'
                                }
                            },
                            font: {
                                color: 'green',
                                fontFamily: 'Segoe UI',
                                fontStyle: 'Normal ',
                                size: '12px',
                                fontWeight: 'regular',
                                opacity: 1
                            },
                        }
                    }
                });
            });    


{% endhighlight %}



The following screenshot displays a bullet graph with indicator.

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img3.png)

## Trim

The title, subtitle and indicator text can be overlapped to the scale group. You can avoid the overlapped text by using the **enable trim** property of the captionSettings. The default value of the enableTrim is true. 

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
         captionSettings: {
          text: 'Bullet Graph Title',
          enableTrim : true,
      }
});
});


{% endhighlight %}



The following screenshot displays the BulletGraph with Trim.

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img4.png)

## Text Placement

All the caption group elements (caption, subtitle, and indicator) in the **Bullet Graph** support text positioning by using the property **textPosition** available in all caption group elements. The properties, **textAlignment** and **textAnchor** are used to customize text placement further.

**Text Position**

The property, textPosition, is used to position the text at the top, bottom, left, and right side of the quantitative scale. The default value of this property is float. By default, text can be placed at any desired location by using the location property.

{% highlight javascript %}


$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Bullet Graph Title',
                    textPosition: 'top',
                    font:{
                        size: '20px',
                        fontWeight: 'bold',

                    }
                }
            });
        });

{% endhighlight %}

The following screenshot displays the Bullet Graph with the title positioned above.

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img5.png)

### Text Alignment

Alignment of text at different positions with respect to scale can be customized by using the **textAlignment** property. Text can be aligned in the **near**, **center,** and **far** locations of the scale. Text alignment depends upon **textPosition** property and is not applicable when the value of the **textPosition** property is **float**. The default value of the **textAlignment** property is **near**.

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Revenue',
                    textPosition: 'left',
                    textAnchor: 'middle',
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    },
                    subTitle: {
                        text: '$ in thousands',
                        textPosition: 'left',
                        textAlignment: 'center',
                        font: {
                            size: '12px',
                            fontWeight: 'bold',

                        }
                    }
                }
            });
        });  


{% endhighlight %}



The following screenshot displays the Bullet Graph with the title and subtitle at different alignments.

![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img6.png)

### Text Anchor

Text elements aligned at the same position are anchored by using the textAnchor property. These can be anchored at the start, middle, and end. The default value of this property is start and applicable only when two or more text elements are aligned at the same position. 

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                 value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Revenue',
                    textPosition: 'left',
                    textAnchor: 'middle',
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    },
                    subTitle: {
                        text: '$ in thousands',
                        textPosition: 'left',
                        textAlignment: 'center',
                        font: {
                            size: '12px',
                            fontWeight: 'bold',

                        }
                    }
                }
        });
    });

         
{% endhighlight %}



![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img7.png)

### Padding

The space required between text and quantitative scale is customized by using the padding property. The default value of this property is 5 and not applicable when the value of the textPosition property is float.

{% highlight javascript %}

$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Profit in %',
                    textPosition: 'left',
                    textAlignment: 'center',
                    padding: 10,
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    }
                }         
        });
    });


{% endhighlight %}


![](Bullet-Graph-Caption_images/Bullet-Graph-Caption_img8.png)

