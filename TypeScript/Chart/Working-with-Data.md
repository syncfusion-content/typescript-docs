---
layout: post
title: Data binding
description: Learn how to bind Chart with JSON data from a remote server or locally in client browser.
platform: typescript
control: Chart
documentation: ug
---

# Working with Data

## Local Data

There are two ways to provide local data to chart.

1. You can bind the data to the chart by using the [`dataSource`](../api/ejchart#members:series-datasource) property of the series and then you need to map the X and Y value with the [`xName`](../api/ejchart#members:series-xname) and [`yName`](../api/ejchart#members:series-yname) properties respectively.

N> For the **OHLC** type series, you have to map four dataSource fields ([`high`](../api/ejchart#members:series-high), [`low`](../api/ejchart#members:series-low), [`open`](../api/ejchart#members:series-open) and [`close`](../api/ejchart#members:series-close)) to bind the data source and for the **bubble** series you have to map the [`size`](../api/ejchart#members:series-size) field along with the [`xName`](../api/ejchart#members:series-xname) and [`yName`](../api/ejchart#members:series-yname). 


{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
     var chartData = [
          { month: 'Jan', sales: 35 }, { month: 'Feb', sales: 28 },  { month: 'Mar', sales: 34 },
          { month: 'Apr', sales: 32 },{ month: 'May', sales: 40 },{ month: 'Jun', sales: 32 },
          { month: 'Jul', sales: 35 },  { month: 'Aug', sales: 55 }, { month: 'Sep', sales: 38 },
          { month: 'Oct', sales: 30 }, { month: 'Nov', sales: 25 }, { month: 'Dec', sales: 32 }];

      $(function () {
        var chartsample = new ej.datavisualization.Chart($("#Chart"), {
                    
          series: [{
                // ... 
         	//Add datasource and set xName and yName 
                dataSource: chartData, 
                xName: "month", 
                yName: "sales"		
             }]

             // ...
        });
   });

{% endhighlight %}

![](Working-with-Data_images/Working-with-Data_img1.png)


2.You can also plot data to chart using [`points`](../api/ejchart.html#members:series-points) option in the series. Using this property you can customize each and every point in the data.

{% highlight javascript %}

   $(function () {
        var chartsample = new ej.datavisualization.Chart($("#Chart"), {
           // ...

           //Initializing Series
           series: [{
               //Adding data points using x and y field of points
               points: [{ x: "John", y: 10000 }, { x: "Jake", y: 12000 }, { x: "Peter", y: 18000 },
                        { x: "James", y: 11000 }, { x: "Mary", y: 9700 }],
               // ...
           }],
            // ...

      });
   });


{% endhighlight %}

![](Working-with-Data_images/Working-with-Data_img2.png)

## Remote Data

You can bind the remote data to the chart by using the DataManager and you can use the [`query`](../api/ejchart#members:series-query) property of the series to filter the data from the dataSource.


{% highlight javascript %}

        //Remote URL           
        var dataManger = new ej.DataManager({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        // Query creation
        var query = ej.Query().from("Orders").take(6);
      $(function () {
        var chartsample = new ej.datavisualization.Chart($("#Chart"), {
            series: [{
                type: 'column',
                dataSource: dataManger,
                xName: "ShipCity",
                yName: "Freight",
                query: query,
            }],
        });
      });

{% endhighlight %}

![](Working-with-Data_images/Working-with-Data_img3.png)




