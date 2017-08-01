---
layout: post
title: Multiple chart series
description: Learn how to render different types of series in chart.
platform: typescript
control: Chart
documentation: ug
---

# Chart Series

## Multiple Series

In EjChart, you can add multiple series object in the [`series`](../api/ejchart.html#members:series) options. The series are rendered in the order it is added to the [`series`](../api/ejchart.html#members:series) option, by default. You can change this order by using the [`zOrder`](../api/ejchart.html#members:series-zorder) option.  

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
          // ...  
          //Adding Multiple Series
          series: [{   // Add first series
              points: [{ x: "USA", y: 50 },
                       // ...
                  ],
                type: 'column',
                // ...
             },
            {       // Add second series
              points: [{ x: "USA", y: 70 },
                       // ...
                   ],                
                 type: 'column'
                 // ...
             },
            {      // Add third series
              points: [{ x: "USA", y: 45 },
                       // ...
                  ],                
                type: 'column'
                // ...
            }],
            
        // ...
    });
 });
}

{% endhighlight %}

![](Chart-Series_images/Chart-Series_img1.png)


### Customizing all series together

By using the [`commonSeriesOptions`](../api/ejchart.html#members:series-commonseriesoptions), you can customize the series options for all the series commonly, instead of setting the options directly on each series object. 

N> The inline properties of the series has the first priority and override the commonSeriesOptions.

The following code example explains on how to enable marker, tooltip and animation for the chart series by using the commonSeriesOptions.

{% highlight javascript %}


    var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
          //  ...
          
           //Initializing Common Properties for all the series
            commonSeriesOptions: {
                type: 'line',
                enableAnimation: true,
                tooltip: {
                    visible: true,
                    template: 'Tooltip'
                },
                marker: {
                    shape: 'circle',
                    size:
                    {
                        height: 10, width: 10
                    },
                    visible: true
                },
                border: { width: 2 }
            },
            
            series: [{
                    // ...         
                },{                
                    //  ...         
              }],
              
            //  ...
      });


{% endhighlight %} 

![](Chart-Series_images/Chart-Series_img2.png)


## Combination Series

EjChart allows you to render the combination of different series in the chart. 

{% highlight javascript %}


     var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
          //  ...
          
           series: [{
                //Set chart type to series1
                 type: 'column',         
               // ...         
            },{
                //Set chart type to series2
                 type: 'line',         
               //  ...         
            }],
              
            //  ...   
      });


{% endhighlight %}

![](Chart-Series_images/Chart-Series_img3.png)

### Limitation of combination chart

* [`Bar`](chart-types#bar-chart), [`StackingBar`](chart-types#stacked-bar-chart), and [`StackingBar100`](chart-types#stacked-bar-chart-1) cannot be combined with the other Cartesian type series.

* Cartesian type series cannot be combined with the accumulation series ([`pie`](chart-types#pie-chart), [`doughnut`](chart-types#doughnut-chart), [`funnel`](chart-types#funnel-chart), and [`pyramid`](chart-types#pyramid-chart)).

* [`Polar`](chart-types#polar) and [`Radar`](chart-types#radar-chart) series cannot be combined with the accumulation and Cartesian type series.

When the combination of Cartesian and accumulation series types are added to the series option, the series that are similar to the first series are rendered and other series are ignored. The following code example illustrates this,  


{% highlight javascript %}


    var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
          //  ...
          
          //Adding Multiple Series
          series: [{    // Add line series
                 points: [{ x: "Jan", y: 45 },
                    // ...
                 ],
                 type: 'line',
                 // ...
               },
               {       // Add [Pie](chart-types#pie-chart) series
                points: [{ x: "Jan", y: 70 },
                  // ...
                ],                
              type: 'pie'
                // ...
            }],

            //  ...   
      });


{% endhighlight %}

![](Chart-Series_images/Chart-Series_img4.png)

