---
layout: post
title: Trendlines in Essential Typescript Chart
description: What are the different types of trendlines available in chart.
platform: typescript
control: Chart
documentation: ug
---

# Trendlines

EjChart can generate Trendlines for Cartesian type series *(Line, Column, Scatter, Area, Candle, HiLo etc.)* except bar type series. You can add more than one trendline object to the [`trendlines`](../api/ejchart#members:series-trendlines) option.

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Enable Trendline to chart series
                       visibility: "visible", type: "linear"
                     }],
                //...
              }]          
             //...  
        });
    });
}


{% endhighlight %}

![](Trendlines_images/Trendlines_img1.png)

## Customize the trendline styles

A trendline can be customized by using the properties such as [`fill`](../api/ejchart#members:series-trendlines-fill), [`width`](../api/ejchart#members:series-trendlines-width), **dashArray** and **opacity**. The default type of trendline is **"linear"**.

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                         //...
                         //Customize the Trendline styles
                         fill: '#99CCFF', width: 3, opacity: 1, dashArray: '2,3'
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img2.png)



## Types of Trendline

EjChart supports the following type of Trendlines.

* Linear
* Exponential
* Logarithmic
* Power 
* Polynomial
* MovingAverage

### Linear

To render Linear Trendline, you have to set the [`type`](../api/ejchart#members:series-trendlines-type) as **"linear"**. 

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "linear"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img3.png)


### Exponential

Exponential Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) as **"exponential"**. 

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "exponential"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img4.png)


### Logarithmic

Logarithmic Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) as **"Logarithmic"**.  

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "logarithmic"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img5.png)


### Power

Power Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) of the trendline as **"power"**. 

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "power"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img6.png)


### Polynomial

Polynomial Trendline can be rendered by setting the trendline [`type`](../api/ejchart#members:series-trendlines-type) as **"polynomial"**.  You can change the polynomial order by using the **polynomialOrder** of the trendlines. It ranges from 2 to 6.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type
                       type: "polynomial"
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img7.png)



### MovingAverage

MovingAverage Trendline can be rendered by setting the [`type`](../api/ejchart#members:series-trendlines-type) of the trendline as **"movingAverage"**. 

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //Change Trendline type and set [`period`](../api/ejchart#members:series-trendlines-period) for moving average
                       type: "movingAverage", period: 3
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img8.png)

## Forecasting

**Trendline forecasting** is the prediction of future/past situations.  **Forecasting** can be classified into two types as follows.

  * Forward Forecasting
  * Backward Forecasting

### Forward Forecasting

The value set for [`forwardForecast`](../api/ejchart#members:series-trendlines-forwardForecast) is used to determine the distance moving towards the future trend.

{% highlight javascript %}

       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //...
                       //Set forward forecasting value
                       forwardForecast: 5
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img9.png)



### Backward Forecasting

The value set for the [`backwardForecast`](../api/ejchart#members:series-trendlines-backwardForecast) is used to determine the past trends.

{% highlight javascript %}

           var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //...
                       //Set forward forecasting value
                       backwardForecast: 5
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img10.png)


## Trendlines Legend

To display the legend item for trendline, use the [`name`](../api/ejchart#members:series-trendlines-name) property. You can interact with the trendline legends similar to the series legends *(show/hide trendlines on legend click)*.  

{% highlight javascript %}

           var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            series:[{
                  trendlines: [{
                       //...
                       //Set Trendline name to display in the legend
                       name: 'Linear'
                     }],
                //...
              }]          
             //...  
        });


{% endhighlight %}

![](Trendlines_images/Trendlines_img11.png)
