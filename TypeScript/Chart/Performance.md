---
layout: post
title: Performance tips 
description: How to improve the performance of Essential Typescript Chart
platform: typescript
control: Chart
documentation: ug
---

# Performance 

* When there are large number of points to load, you can enable canvas rendering mode in chart. Canvas rendering is faster than SVG because it does not involve manipulating DOM elements as much as SVG rendering.   

{% highlight javascript %}
 /// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#container"), {
            
            //  ...
            //Enable Canvas rendering mode
            enableCanvasRendering: true,         

            // ...
      });
    });
}

{% endhighlight %}

* Instead of enabling data markers and labels when there are large number of data points, you can use **trackball** and **tooltip** to view point information.

## Lazy Loading

Lazy loading feature provides an effective way for loading data on demand by scrolling and viewing a smaller range of data from a larger collection.

{% highlight javascript %}

      var chartsample = new ej.datavisualization.Chart($("#container"), {
   
            primaryXAxis:
            {
                
                  scrollbarSettings: {

                              // enable the scrollbar

                              visible: true,  
       
                              // enable the resize option 

                              canResize: true,
       
                              range: {

                                       min: “2009/1/1”,
 
                                       max: “2014/1/1”
  
                              }        
                  }    
            },    
            // . . .	
      });

{% endhighlight %}

![](Performance_images/Perform_img1.png)