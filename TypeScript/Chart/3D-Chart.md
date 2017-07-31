---
layout: post
title: 3D Chart types available in Typescript Chart
description: Learn about the different types of 3D charts supported by Syncfusion Essential JavaScript Chart and how to customize the 3D view.
platform: typescript
control: Chart
documentation: ug
---

# 3D Chart

Essential 3D Chart for JavaScript allows you to view 8 chart types in 3D view such as [`Bar`](chart-types#bar-chart), [`StackingBar`](chart-types#stacked-bar-chart), [`StackingBar100`](chart-types#stacked-bar-chart-1), [`Column`](chart-types#column-chart), [`Stacked Column`](chart-types#stacked-column-chart), [`100% Stacked Column`](chart-types#stacked-column-chart-1), [`Pie`](chart-types#pie-chart), [`Doughnut`](chart-types#doughnut-chart).


## 3D Column Chart

For rendering a 3D Column Chart, specify the series [`type`](../api/ejchart#members:series-type) as **"column"** in the chart series and set [`enable3D`](../api/ejchart#members:enable3d) option as **true** in the chart.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
             series: [{
                //Set chart type to series
                 type: 'column',         
                 //  ...         
            }],
            
              // Enable 3D Chart
              enable3D: true,
              // ...          
        });
    });
}


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img1.png)


## 3D Bar Chart

You can create a 3D Bar Chart by setting the series [`type`](../api/ejchart#members:series-type) as **"bar"** in the chart series and enable [`enable3D`](../api/ejchart#members:enable3d) option in the chart.

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
             series: [{
                //Set chart type to series
                 type: 'bar',         
                 //  ...         
            }],
            
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img2.png)


## 3D Stacked Column Chart

Stacking Column 3DChart is rendered by specifying the series [`type`](../api/ejchart#members:series-type) as **"stackingColumn"** in the chart series and enable [`enable3D`](../api/ejchart#members:enable3d) option in the chart.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series1
                 type: 'stackingColumn',         
                 // ...         
             },{
                //Set chart type to series2
                 type: 'stackingColumn',         
                 //  ...         
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img3.png)


## 3D 100% Stacked Column Chart

100% Stacking Column 3DChart is rendered by specifying the series [`type`](../api/ejchart#members:series-type) as **"stackingColumn100"** in the chart series and enable [`enable3D`](../api/ejchart#members:enable3d) option in the chart.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series1
                 type: 'stackingColumn100',         
                 // ...         
             },{
                //Set chart type to series2
                 type: 'stackingColumn100',         
                 //  ...         
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img4.png)


## 3D Stacked Bar Chart

To create Stacking Bar 3DChart, set the series [`type`](../api/ejchart#members:series-type) as **"stackingBar"** in the chart series and enable [`enable3D`](../api/ejchart#members:enable3d) option in the chart.

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series1
                 type: 'stackingBar',         
                 // ...         
             },{
                //Set chart type to series2
                 type: 'stackingBar',         
                 //  ...         
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img5.png)


## 3D 100% Stacked Bar Chart

You can create 100% Stacking Bar 3DChart by setting the series [`type`](../api/ejchart#members:series-type) as **"stackingbar100"** in the chart series and enable [`enable3D`](../api/ejchart#members:enable3d) option in chart.

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series1
                 type: 'stackingBar100',         
                 // ...         
             },{
                //Set chart type to series2
                 type: 'stackingBar100',         
                 //  ...         
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img6.png)


## 3D Pie Chart

To render the Pie Chart in 3D view, enable the **enbel3D** option in the chart and set the series [`type`](../api/ejchart#members:series-type) as **"pie"** in the chart series.  

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series
                 type: 'pie',         
                 // ...                     
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img7.png)

## 3D Doughnut Chart

To render the Doughnut Chart in 3D view, enable the **enbel3D** option in the chart and set the series [`type`](../api/ejchart#members:series-type) as **"doughnut"** in the chart series. 

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
            series: [{
                //Set chart type to series
                 type: 'doughnut',         
                 // ...                     
             }],
             
             // Enable 3D Chart
             enable3D: true,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img8.png)


## Configure 3D Chart

### 3D View

To render the EjChart in 3D view, set the [`enable3D`](../api/ejchart#members:enable3d) option as *true* in the chart.
 
{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
               //Enable 3DChart
               enable3D: true,    
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img9.png)



 
### Placing Bar / Column kind of series side-by-side
 
 The [`sideBySideSeriesPlacement`](../api/ejchart#members:sidebysideseriesplacement) defines the appearance of the different sets of data on the 3D Chart. When this property is enabled, the data is displayed side by side, otherwise it is displayed along the depth of the axis.  
 
{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
               //Enable SideBySideSeriesPlacement for 3DChart
                sideBySideSeriesPlacement: true,	
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img10.png)


### Setting Axis Wall Size

In 3DChart, Cartesian axes lines are represented as walls and it defines the width of the 3D wall. 3D Pie and Doughnut Chart does not support [`wallSize`](../api/ejchart#members:wallsize) because they don’t have axes.  

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...           
              //Change 3DChart axis wall size
               wallSize: 10,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img11.png)


### 3D Depth

By using the [`depth`](../api/ejchart#members:depth) property, you can view the 3D Chart from the front view of the series to the background wall.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
             //Change 3DChart depth value
             depth: 120,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img12.png)


### Rotating and Tilting 3D Chart

To spin the 3D Chart on mouse dragging, enable [`enableRotation`](../api/ejchart#members:enablerotation) option in the chart. The [`tilt`](../api/ejchart#members:tilt) property specifies the angle of the slope of the 3D Chart. The positive and negative values are declared to the side where the slope is present. The [`rotation`](../api/ejchart#members:rotation) option is used to rotate the 3D chart towards left or right side of the chart. The direction of the chart depends upon the positive and negative values of the angle.  

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...     
                     
             //Change 3DChart tilt value
             tilt: 10,
             
             //Enable 3DChart  rotation  on mouse dragging 
             enableRotation: true,
             
             //Change 3DChart rotation on chart load 
             rotation: 40,

             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img13.png)


### PerspectiveAngle	

The [`perspectiveAngle`](../api/ejchart#members:perspectiveangle) specifies the appearance of the height, width, depth and wall of the 3D Chart. When the perspectiveAngle is decreased, the 3D object appears very close to the viewer. But when it is increased, the 3D object appears far away from the viewer.   

{% highlight javascript %}

         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...          
                
              //Change 3DChart perspective angle
               perspectiveAngle: 150,
             // ...          
        });


{% endhighlight %}


![](3D-Chart_images/3D-Chart_img14.png)
