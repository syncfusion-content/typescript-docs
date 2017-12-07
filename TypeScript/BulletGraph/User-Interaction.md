---
layout: post
title: User-Interaction
description: user interaction
platform: typescript
control: BulletGraph	
documentation: ug

---

# User Interaction

## Animation

**Bullet Graph** supports animation that makes the performance measure bar to animate when rendering the Bullet Graph. **Animation** is enabled or disabled using **enable animation** property. By default, **Animation** is enabled in Bullet Graph.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
         enableAnimation: true,
                    value: 8,
                    comparativeMeasureValue: 5,     
        });
    });
}

{% endhighlight %}

## Responsiveness during browser resize

**Bullet Graph** is made responsive when resizing the browser by using **isResponsive** property. By default the value of this property is **true** in Bullet Graph.

{% highlight javascript %}


 $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                    isResponsive: true,
                    value: 8,
                    comparativeMeasureValue: 5,                    
                });
            });
                


{% endhighlight %}



## Applying same color to all ticks and labels in a range

Background color for qualitative range is applied to major ticks and minor ticks of the **Bullet Graph** using **applyRangeStrokeToTicks** property. The range colors are applied to labels using **applyRangeStrokeToLabels** property. By default same colors are not applied to a qualitative range and its corresponding ticks or labels.

{% highlight javascript %}


$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
                    applyRangeStrokeToTicks: true,
                    applyRangeStrokeToLabels: true,

                    qualitativeRanges: [
                        { rangeEnd: 3.5, rangeStroke: 'darkred', rangeOpacity: 0.5 },
                        { rangeEnd: 5.0, rangeStroke: 'red', rangeOpacity: 1 },
                        { rangeEnd: 7.5, rangeStroke: 'blue', rangeOpacity: 0.7 },
                        { rangeEnd: 9.0, rangeStroke: 'lightgreen', rangeOpacity: 1 },
                        { rangeEnd: 10.0, rangeStroke: 'green', rangeOpacity: 1 }
                    ],
                    value: 8,
                    comparativeMeasureValue: 5,                    
                });
            });



{% endhighlight %}

![](User-Interaction_images/User-Interaction_img1.png) 

## Tooltip

By default **Bullet Graph** displays **Tooltip** when mouse is hovered over feature measure bar. **Tooltip** is enabled or disabled using **visible**property in **tooltipSettings**.

![](User-Interaction_images/User-Interaction_img2.png) 

Bullet Graph supports Tooltip template instead of default Tooltip to customize the appearance and contents of Tooltip. The Tooltip template should be a &lt;div&gt; element with display set to ‘none’, so it is displayed only when mouse is placed on feature measure bar. The id value of the &lt;div&gt; element should be provided as value to the **template** property in tooltipSettings of Bullet Graph to display the customized &lt;div&gt; element as Tooltip instead of default Tooltip. The values displayed in default Tooltip such as current value, target value and category are accessed in template &lt;div&gt; element by using {{currentValue}}, {{targetValue}} and {{category}} respectively.

{% highlight html %}

<div id="BulletGraphTooltip" style="display:none; width:125px; padding-top: 10px; padding-bottom:10px; color: blue"> 
    <div align="center" style="color:blue; font-weight:bold"> Sales </div> 
    <table style="color:green"> <tr> <td> Current </td> <td> : </td> </tr> <tr> <td> Target </td> <td> : </td> </tr> </table> 
</div>

{% endhighlight %}

{% highlight javascript %}

   $(function () {
    var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
         value: 8,
         comparativeMeasureValue: 6,
         height: 150,
         tooltipSettings: { template: 'BulletGraphTooltip' } 
    });
   });

{% endhighlight %}

The following screenshot displays **Bullet Graph** with a customized **Tooltip** including a header and contents such as current value and target value in different colors.

![](User-Interaction_images/User-Interaction_img3.png) 

