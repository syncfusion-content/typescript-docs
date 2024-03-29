---
layout: post
title: Markers and data labels in Syncfusion Essential Typescript Chart
description: Learn how to add markers and data point labels to a Chart series.
platform: typescript
control: Chart
documentation: ug
---

# Data Markers

Data markers are used to provide information about the data point to the user. You can add a shape and label to adorn each data point.

## Add Shapes

You can add shapes to any chart types but they are often used with line, area and spline series to indicate each data point. It is highlighted when you hover the mouse on the shape.

Shapes can be added to the chart by enabling the [`visible`](../api/js/ejchart#members:series-marker-datalabel-visible) option of the [`marker`](../api/js/ejchart#members:series-marker) property. There are different shapes you can add to the chart by using the shape option such as rectangle, circle, diamond etc.

The following code example explains on how to enable series marker and add shapes,

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...
            //Adding shapes to series	
            series: [{
                // ....
                marker: {
                    shape: 'Diamond',
                    visible: true
                }
            },
             {
                 // ... 
                 marker: {
                     shape: 'Triangle',
                     visible: true
                 }
             },
              {
                  // ...
                  marker: {
                      shape: 'Hexagon',
                      visible: true
                  }
              }],

           // ....
    });
 });
}


{% endhighlight %}

![Marker Shapes](Data-Markers_images/Data-Markers_img1.png)



## Add image as marker

Apart from the shapes, you can also add images to mark the data point by using the [`imageUrl`](../api/js/ejchart#members:series-marker-imageurl) option.

The following code example illustrates this,

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            series: [{
                // ...
                marker: {
                 // Enable and customize the marker shape and size
                    visible: true,
                // In order to set imageUrl, set shape as ‘image’ .
                    shape: "image",
                    imageUrl: "sun_annotation.png",
                    size: {width: 20, height: 20}
                }
            }],
           // ...
    });


{% endhighlight %}

![Marker Image](Data-Markers_images/Data-Markers_img2.png)


## Add labels

Data label can be added to a chart series by enabling the [`visible`](../api/js/ejchart#members:series-marker-datalabel-visible) property in the [`dataLabel`](../api/js/ejchart#members:series-marker-datalabel) option. The labels appear at the top of the data point, by default.

The following code example shows how to enable data label and set its horizontal and vertical text alignment. 

{% highlight javascript %}


     var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            series: [{
                // ...
                marker: {
                        dataLabel: {
                      //Set text alignment to data label text	
                            visible: true,
                            horizontalTextAlignment: "center",
                            verticalTextAlignment: "far"
                        }
                    }
            }],
           // ...
    });


{% endhighlight %}

![DataLabel Visibility](Data-Markers_images/Data-Markers_img3.png)


Label content can be formatted by using the template option. Inside the template, you can add the placeholder text *"point.x"* and *"point.y"* to display corresponding data points x & y value.

You can adorn the labels with background shapes by setting *shape* option.

The following code example shows how to add background shapes and set template to data label.

{% highlight html %}


<div id="template">
     <div id="left">
	<img src="../images/chart/icon_investments.png"/>
     </div>
     <div id="right">
          <div id="point">#point.y#%</div>
     </div>
</div>

{% endhighlight %}

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            series: [{
               // ...
               marker: {
		            dataLabel: {
			           visible: true,
                     //Set template to data label
            			template: 'template'
		              }}		
               }, {
	           // ...
               marker: {
		             dataLabel: {
			                visible: true,
                          //Add background shape to the data label
                            shape: 'Rectangle',
                            border: { width: 1, color: "red" }			     
                         }}
                    },{
                // ...
               marker: {
		            dataLabel: {
			           visible: true
		             }}               
              }],

           // ...
    });


{% endhighlight %}

![DataLabel Template](Data-Markers_images/Data-Markers_img4.png)


The appearance of the labels can be customized by using the [`font`](../api/js/ejchart#members:series-marker-datalabel-font) and [`offset`](../api/js/ejchart#members:series-marker-datalabel-offset) options. The [`offset`](../api/js/ejchart#members:series-marker-datalabel-offset) option is used to move the labels vertically. Also, labels can be rotated by using the [`rotate`](../api/ejchart#members:series-marker-datalabel-rotate) option.

The following code example shows how to rotate data label text and customize the font.

{% highlight javascript %}


     var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            series: [{
             // ...
               marker: {
                        dataLabel: {
                            visible: true,
                           //Rotate data label and customize the font
                            angle: "300",    
                            offset: 15,
                            font: { color: "black", size:"13px" }
                         }
                    }		
              }], 
           // ...
    });


{% endhighlight %}

![DataLabel Rotation and Font](Data-Markers_images/Data-Markers_img5.png)


You can position the label to the top, center or bottom position of the segment by using the [`textPosition`](../api/js/ejchart#members:series-marker-datalabel-textposition) option for the chart types such as column, bar, stacked bar, stacked column, 100% stacked bar, 100% stacked column, candle and OHLC.

The following code example shows how to set textPosition to display data label in the middle of the column rectangle.

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ... 
	        series:[{
                  // ....
                   marker: {
                       dataLabel: {
                           visible: true,
                         // Place the data label text position in the centre of the rectangle
                           textPosition: "middle"
                          // ...
                       } } 
               }],            

	    // .....
    });


{% endhighlight %}

![DataLabel Position](Data-Markers_images/Data-Markers_img6.png)


The label can be positioned inside or outside the perimeter of the series by using the [`labelPosition`](../api/js/ejchart#members:series-labelposition) option for the chart types such as Pie and Doughnut, .

The following code example shows how to set the *labelPosition*,

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ... 
	        series:[{
                   points: [{ x: 'India', y: 24, text: 'India 24%' },
                            { x: 'Japan', y: 25, text: 'Japan 25%' },
                            { x: 'Australia', y: 20, text: 'Australia 20%' },
                            { x: 'USA', y: 35, text: 'USA 35%' },
                            { x: 'China', y: 23, text: 'China 23%' },
                            { x: 'Germany', y: 27, text: 'Germany 27%' },
                            { x: 'France', y: 22, text: 'France 22%' }],

                   marker: {
                       dataLabel: {
                           visible: true,
                           shape: 'rectangle',
                           font: {color: "white"}
                       }
                   },
                   type: 'doughnut',
                   //Display data label outside position 
                   labelPosition: 'outside'
               }],            
	    // ...
    });


{% endhighlight %} 

![Pie and Doughnut DataLabel](Data-Markers_images/Data-Markers_img7.png)


The following screenshot displays the labels when the [`labelPosition`](../api/js/ejchart#members:series-labelposition) is set as *inside* position.

![Inside LabelPosition](Data-Markers_images/Data-Markers_img8.png)


The following screenshot displays the labels when the [`labelPosition`](../api/js/ejchart#members:series-labelposition) is set as *outsideExtended* position.

![OutsideExtended LabelPosition](Data-Markers_images/Data-Markers_img9.png)


The label can be wrapped for pie, doughnut, funnel, and pyramid series by setting the enableWrap property. 

{% highlight javascript %} 

var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {

        // . . .   

    series:[
    {
                //. . .
            marker: {
                 
                       dataLabel: {
                                 
                             // enable the dataLabel
                          
                             visible: true,

                             // enable the wrapping option

                             enableWrap: true,
           
                             // set the maximumLabelWidth of the data label

                             maximumLabelWidth: 32
               
                                //. . .

                      }
               }
    
             // . . .

        ]}

     // . . .

});


{% endhighlight %} 

![DataLabel Wrap](Data-Markers_images/Data-Markers_img13.png)


## Customize specific points

By using the ejChart, you can also customize the individual/specific markers with different colors, shapes and also with different images.

There are two ways to achieve this based on how the data is fed to the series.

When the data is provided by using the [`points`](../api/js/ejchart#members:series-points) option, you can add marker for each data point or specific point by using the [`marker`](../api/js/ejchart#members:series-marker) option as illustrated in the following code example.

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...     
            series: [{
                    // ...
                    points: [  { x: 'Jan', y: 35 }, { x: 'Feb', y: 28 },   { x: 'Mar', y: 34 },
                      { x: 'Apr', y: 32 },{ x: 'May', y: 40 },  { x: 'Jun', y: 32 },
                      { x: 'Jul', y: 35 },  { x: 'Aug', y: 55,
                       marker: {
                         //Enable and customize the data label for a point
                            dataLabel: {
                                visible: true,
                                offset: -10,
                                shape: "upArrow", font: { color: "white" , size: '11px' },
                                margin: { left: 15, right: 15, top: 10, bottom: 10 },
                                fill: "green"
                           } } },

                          { x: 'Sep', y: 38 },{ x: 'Oct', y: 30 },
                          { x: 'Nov', y: 25,
                                  marker: {
                                    //Enable and customize the data label for a point
                                     dataLabel: {
                                        visible: true,
                                        offset: -22,
                                        verticalTextAlignment: 'near',
                                        shape: "downArrow", font: { color: "white", size: '11px' },
                                        margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                                        fill: "red"
                           } } },  { x: 'Dec', y: 32 }],

                     }],
                 // ...
    });


{% endhighlight %}

![DataLabel Customization](Data-Markers_images/Data-Markers_img10.png)

When the data is bound to the series by using the [`dataSource`](../api/js/ejchart#members:series-datasource) option, you can customize the points in the [`seriesRendering`](../api/ejchart#members:events-seriesrendering) event as illustrated in the following code example,

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
           // ...
            series: [{
                         //Add datasource and set xName and yName 
                         dataSource: chartData, 
                          xName: "month", 
                          yName: "sales"
            }],
            
           //Fires on rendering the series
            seriesRendering: "onSeriesRender",

             // ...

    });

    //Define the seriesRendering client side event
  
     function onSeriesRender(sender) {
 
        
        //Enable and customize the dataLabel for a point using event

            sender.data.series.points[7].marker = {
               dataLabel: {
                    visible: true,
                    offset: -10,
                    shape: "upArrow", font: { color: "white", size: '11px' },
                    margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                    fill: "green"
                }};

            sender.data.series.points[10].marker = {
                 //Enable and customize the dataLabel for a point using event
                dataLabel: {
                        visible: true,
                        offset: -22,
                        verticalTextAlignment: 'near',
                        shape: "downArrow", font: { color: "white", size: '11px' },
                        margin: { left: 15, right: 15, top: 10, bottom: 10 },                    
                        fill: "red"
                }};
        }

{% endhighlight %}

![DataLabel Customize on SeriesRender](Data-Markers_images/Data-Markers_img10.png)


## Connect Line

This feature is used to connect label and data point by using a line. It can be enabled only for Pie, Doughnut, Pyramid and Funnel chart types. Connector line types can be set as *bezier* or *line* by using the [`type`](../api/js/ejchart#members:series-marker-datalabel-connectorline-type) option.

 The following code example illustrates this,

{% highlight javascript %}


     var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            series: [{
		      // ...
		       marker: {
                   dataLabel: {
                             visible: true,
                             // Set connector line type and customize the color,
                             connectorLine: { type: 'bezier', color: 'black' }
                             // ...
                         }  },
                         // ...
                         labelPosition: 'outsideExtended',
                 }],

           // ...
    });


{% endhighlight %}

![Connector Line](Data-Markers_images/Data-Markers_img11.png)


## Smart labels

Overlapping of the labels can be avoided by enabling the [`enableSmartLabels`](../api/js/ejchart#members:series-enablesmartlabels) property. The default value is *true* for *accumulation type series* and *false* for *other series types*.

The following code example shows how to enable smart labels,

{% highlight javascript %}


     var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...      
            //Initializing Series	
            series: [{
                points: [{ x: 'Other Personal', y: 94658, text: 'Other Personal, 88.47%' },
                             { x: 'Medical care', y: 9090, text: 'Medical care, 8.49%' },
		                     { x: 'Housing', y: 2577, text: 'Housing, 2.40%' },
                             { x: 'Transportation', y: 473, text: 'Transportation, 0.44%' },
                             { x: 'Education', y: 120, text: 'Education, 0.11%' },
                             { x: 'Electronics', y: 70, text: 'Electronics, 0.06%' }],
           	    marker:{
		              dataLabel:{
				          visible: true,
				          shape: 'none',
				          connectorLine: { type: 'bezier', color: 'black' },
				          font: { size: '14px' }
                       }},
               	       border: { width: 2, color: 'white' },
		               type: 'pie',
                       labelPosition: "outsideExtended",
                       //Display data label outside position and enable smart labels
                       enableSmartLabels: true
                 }],
           // ...
    });


{% endhighlight %}

![EnableSmartLabels](Data-Markers_images/Data-Markers_img12.png)


