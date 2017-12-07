---
layout: post
title: Legend
description: legend for ranges in the Circular Gauge 
platform: typescript
control: Circular Gauge
documentation: ug
---

# Legend

The `legend` contains the list of the ranges that appear in the circular gauge  

## Legend Visibility

By default, the legend will not be displayed in the circular gauge. You can enable or disable it by using the `visible` property of the legend.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {
 $(function () {
    var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
  legend:{ 
     visible : true,
       },
            });
 });

}

{% endhighlight %}

![](Legend_images/Legend_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/flatlight/radialgauge/legend) here to view the online demo sample for  legend in the circular Gauge.

### Legend Text

The text displayed in the legend can be customized by using the `legendText` property present in the ranges of the circular gauge. When the legendText is not specified in the ranges, then the legend item for that particular range will not displayed. By default the legendText value is **null** . 

{% highlight javascript %}

    var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
              ranges: [{
                 legendText:"Light air",			
            }]
            //...

            // ...             
        });


{% endhighlight %}

## Position and Align the Legend

By using the `position` property, you can position the legend at *left*, *right*, *top* or *bottom* of the CircularGauge. The legend is positioned at the **bottom** of the circular gauge, by default.

{% highlight javascript %}

    var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                // ...  
                //Place the legend at top of the circular gauge
                position: 'top',

            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img2.png)

### Legend Alignment

You can align the legend to the *center*, *far* or *near* based on its position by using the `alignment` property.

{% highlight javascript %}


      var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //The below two settings will place the legend at the top-right corner of the circular gauge.
                alignment: 'far',
                position: 'top', 
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img3.png)

## Customization

### Legend Fill and Opacity

You can change the opacity and fill color of legend text using `opacity` and `fill` property of legend. 

{% highlight javascript %}

           var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //fill color of legend
                 fill: 'red',
                //opacity of legend
                 opacity: 0.8
            }
            // ...             
        });

{% endhighlight %}

### Legend shape

To change the legend item shape, you have to specify the desired shape in the `shape` property of the legend. By default, the shape of the legend is **circle**.It also supports rectangle,diamond,triangle,slider,line,pentagon,trapezoid and wedge shapes.

{% highlight javascript %}


           var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //Change legend shape
                 shape: 'slider',
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img4.png)


### Legend Item Size and Border

You can change the size of the legend items by using the `width` and `height` properties in the `itemStyle`. To change the legend item border, use `border` property of the legend itemStyle. The color and width of legend item border can be customized using border `color` and `width` property.

{% highlight javascript %}


            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //Change legend items border, height and width
                itemStyle: {width: 13, height: 13, border: { color: "#FF0000", width: 2 } },
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img5.png)

### Legend size

You can change the default legend size by using the `size` property of the legend. The height and width of legend size can customized using `height` and `width`property.

{% highlight javascript %}


            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...
            legend: { 
                 //...
                 //Change legend size
                 size:{width: '350', height: '100'}
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img6.png)


### Legend Item Padding

You can control the spacing between the legend items by using the `itemPadding` option of the legend.  The default value is 20. 

{% highlight javascript %}


            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //Add space between each legend item
                itemPadding: 30,
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img7.png)

### Legend border

You can customize the legend border by using the `border` option in the legend. The legend border can be customized using border `color` and `width` property. 

{% highlight javascript %}


           var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //Set border color and width to legend
                border: {color: "#FFC342", width: 2},
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img8.png)

### Font of the legend text

The `font` of the legend item text can be customized by using properties such as `fontFamily`, `fontStyle`, `fontWeight` and `size` of legend font.


{% highlight javascript %}


            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            // ...             
            legend: {
                //...
                //Customize the legend item text
                font: { fontFamily: 'Segoe UI', fontStyle: 'Normal', fontWeight: 'Bold', size: '15px' },
                         
             },
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img9.png)

## Events

### Legend Item Render

`LegendItemRender` event triggers before rendering the legend items. This event is triggered for each legend item in Circular gauge. You can use this event to customize legend item shape or add custom text to legend item dynamically

{% highlight javascript %}

    var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{

           
            //Subscribe the legendItemRender event
            legendItemRender: "onLegendRender",

            //...
        });

        function onLegendRender(sender) {
            //Get legend item details before rendering
            var legendItem = sender.data;

        }

{% endhighlight %}

### Legend Item Click

You can get the legend item details such as *RangeIndex, bounds and shape* by subscribing the `legendItemClick` event of the circular gauge. When the legend item is clicked, it triggers the event and returns the legend information 

{% highlight javascript %}

    var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
           
            //Subscribe the legend item click event
            legendItemClick: "onLegendClicked",

            //...
        });

        function onLegendClicked(sender) {
            //Get legend item details on legend item click.
            var legendItem = sender.data;
        }


{% endhighlight %}

