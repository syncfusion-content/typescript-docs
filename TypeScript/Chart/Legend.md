---
layout: post
title: Chart legend
description: How to cutomize the legend in Essential Typescript Chart.
platform: js
control: Chart
documentation: ug
---

# Legend

The legend contains the list of chart series and Trendlines that appear in a chart. 

## Legend Visibility

By default, the legend is enabled in the chart. You can enable or disable it by using the [`visible`](../api/js/ejchart#members:legend-visible) option of the legend.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
         // ...
         legend: {
            //Visible chart legend
            visible: true
        },
        //...
     });
    });
}

{% endhighlight %}

![](Legend_images/Legend_img1.png)


## Legend title

To add the title to the legend, you have to specify the [`legend.title.text`](../api/js/ejchart#members:legend-title-text) option.

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
              legend: {
                //...
                title: {
                   //Add title to the chart legend
	               text: "Countries",
				
		         }  },

            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img2.png)


## Position and Align the Legend

By using the [`position`](../api/js/ejchart#members:legend-position) option, you can position the legend at *left*, *right*, *top* or *bottom* of the chart. The legend is positioned at the **bottom** of the chart, by default.

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                // ...  
                //Place the legend at top of the chart
                position: 'top',

            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img3.png)

**Legend Alignment**

You can align the legend to the *center*, *far* or *near* based on its position by using the [`alignment`](../api/js/ejchart#members:legend-alignment) option.

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //The below two settings will place the legend at the top-right corner of the chart.
                alignment: 'far',
                position: 'top', 
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img4.png)


## Arrange legend items in the rows and columns

You can arrange the legend items horizontally and vertically by using the [`rowCount`](../api/js/ejchart#members:legend-rowcount) and [`columnCount`](../api/js/ejchart#members:legend-columncount) options of the legend.

* When only the [`rowCount`](../api/js/ejchart#members:legend-rowcount) is specified, the legend items are arranged according to the [`rowCount`](../api/js/ejchart#members:legend-rowcount) and number of columns may vary based on the number of legend items.

* When only the [`columnCount`](../api/js/ejchart#members:legend-columncount) is specified, the legend items are arranged according to the [`columnCount`](../api/js/ejchart#members:legend-columncount) and number of rows may vary based on the number of legend items.

* When both the options are specified, then the one which has higher value is given preference. For example, when the [`rowCount`](../api/js/ejchart#members:legend-rowcount) is 4 and [`columnCount`](../api/js/ejchart#members:legend-columncount) is 3, legend items are arranged in 4 rows.

* When both the options are specified and have the same value, the preference is given to the [`columnCount`](../api/js/ejchart#members:legend-columncount) when it is positioned at the top/bottom position. The preference is given to the [`rowCount`](../api/js/ejchart#members:legend-rowcount) when it is positioned at the left/right position.
 

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //Arrange legend items in 4 rows and approximately 4 columns. Column couldn’t may vary based on number of items. 
                rowCount: 4,
                columnCount: 4 
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img5.png)


## Customization

### Legend shape

To change the legend icon shape, you have to specify the shape in the [`shape`](../api/js/ejchart#members:legend-shape) property of the legend. When you want the legend icon to display the prototype of the series, you have to set the **seriesType** as shape.

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Change legend shape
                 shape: 'seriesType',
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img6.png)


### Legend items size and border

You can change the size of the legend items by using the [`itemStyle.width`](../api/js/ejchart#members:legend-itemstyle-width) and [`itemStyle.height`](../api/js/ejchart#members:legend-itemstyle-height) options. To change the legend item border, use [`border`](../api/js/ejchart#members:legend-border) option of the legend itemStyle.

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Change legend items border, height and width
                itemStyle: {width: 13, height: 13, border: { color: "#FF0000", width: 1 } },
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img7.png)

### Legend size

By default, legend takes 20% of the **height** horizontally when it was placed on the top or bottom position and 20% of the **width** vertically while placing on the left or right position of the chart. You can change this default legend size by using the [`size`](../api/js/ejchart#members:legend-size) option of the legend.  

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...
            legend: { 
                 //...
                 //Change legend size
                 size:{width: '550', height: '100'}
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img8.png)


### Legend Item Padding

You can control the spacing between the legend items by using the [`itemPadding`](../api/js/ejchart#members:legend-itempadding) option of the legend.  The default value is 10. 

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Add space between each legend item
                itemPadding: 15,
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img9.png)

### Legend border

You can customize the legend border by using the [`border`](../api/js/ejchart#members:legend-border) option in the legend. 

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Set border color and width to legend
                border: {color: "#FFC342", width: 2},
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img10.png)

### Scrollbar for legend

You can enable or disable the legend scrollbar by using the [`enableScrollbar`](../api/js/ejchart#members:legend-enablescrollbar) option of the legend. When you disable the scrollbar option, the legend does not consider the [`default size`](legend.html#legend-size) and chart draws in the remaining space. If you have specified the **size** to the legend with the scrollbar disabled, then the legends beyond this limit will get clipped. The default value of [`enableScrollbar`](../api/js/ejchart#members:legend-enablescrollbar) option is **true**.  

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Enable scrollbar option in for legend
                enableScrollbar: true,
                size:{width: '430', height: '80'},
            }
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img11.png)

### Customize the legend text

To customize the legend item text and title you can use the [`legend.font`](../api/js/ejchart#members:legend-font) and [`legend.title`](../api/js/ejchart#members:legend-title) options. You can change the legend title alignment by using the [`textAlignment`](../api/js/ejchart#members:legend-title-textalignment) option of the legend title.

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
            legend: {
                //...
                //Customize the legend item text
                font: { fontFamily: 'Segoe UI', fontStyle: 'Normal', fontWeight: 'Bold', size: '15px' },
                title: {
                    //...
		            textAlignment: "center",
                    //Customize the legend title text
	                font: { fontFamily: 'Segoe UI', fontStyle: 'Italic', 
                                        fontWeight: 'Bold', size: '12px' },
	             }            
             },
            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img12.png)

### LegendItems Text Overflow

**Trim**

You can trim the legend item text when its width exceeds the [`legend.textWidth`](../api/js/ejchart#members:legend-textwidth), by specifying [`textOverflow`](../api/js/ejchart#members:legend-textoverflow) as **"trim"**. The original text will be displayed on mouse hover.

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            
            // ...             
            legend: {
               //trim the legend text
		        textOverflow: 'trim', 
		        textWidth: 34
	          } 

            // ...             
        });


{% endhighlight %}

![](Legend_images/Legend_img13.png) 


**Wrap**

By specifying [`textOverflow`](../api/js/ejchart#members:legend-textoverflow) as **"wrap"**, you can wrap the legend text by word.

![](Legend_images/Legend_img14.png)

**WrapAndTrim**

You can wrap and trim the legend text by specifying [`textOverflow`](../api/js/ejchart#members:legend-textoverflow) as **"wrapAndTrim"**. The original text will be displayed on mouse hover.

![](Legend_images/Legend_img15.png)
   

## Handle the legend item clicked

You can get the legend item details such as *index*, *bounds*, *shape* and *series* by subscribing the [`legendItemClick`](../api/js/ejchart#events:legenditemclick) event on the chart. When the legend item is clicked, it triggers the event and returns the [`legend information`](../api/js/ejchart#events:legenditemclick). 

{% highlight javascript %}


        var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {

            legend: {
                   //...
              },
              
           //Subscribe the legend item click event
            legendItemClick: "onLegendClicked",
            
            //...
        });
        
     function onLegendClicked(sender) {
        //Get legend item details on legend item click.
        var legendItem = sender.data;
      }

{% endhighlight %}


## Series selection on legend item click

You can select a specific series or point while clicking on the corresponding legend item through disabling the [`toggleSeriesVisibility`](../api/js/ejchart#members:legend-toggleseriesvisibility) option of the legend. The default value of toggleSeriesVisibility option is **true**. To customize the series selection refer to the series [`selection`](../api/js/ejchart#members:series-selectionsettings).

{% highlight javascript %}


       var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
            // ...             
                legend: {
                   //...
                   //Disable series collapsing on legend item clicked
                   toggleSeriesVisibility: false,
               },
           //...
      });
      

{% endhighlight %}

![](Legend_images/Legend_img16.png)



## Collapsing legend item

You can collapse the specific series/point legend item displaying in the chart, by setting the [`visibleOnLegend`](../api/js/ejchart#members:series-visibleonlegend) as *"hidden"* in the point or series.

{% highlight javascript %}


    var chartSample = new ej.datavisualization.Chart($("#chartContainer"), {
     
          //Initializing Series
          series:[{
             points: [{ x: 'Albania', y: 60.1 },
                     //...
                     //Collapse the point's legend item in the legend collection
                     { x: 'New Zealand', y: 82.8, visibleOnLegend:'hidden' }]
                  }],
         legend: { visible: true}
     });
      
{% endhighlight %}

![](Legend_images/Legend_img17.png)