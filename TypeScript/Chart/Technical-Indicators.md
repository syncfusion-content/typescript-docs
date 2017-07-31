---
layout: post
title: Technical Indicators
description: What are the different types of technical indicators supported in Essential Chart for financial analysis.
platform: Typescript
control: Chart
documentation: ug
---

# Technical Indicators

EjChart control supports 10 types of technical indicators. 

## Bind data to render the indicator

You can bind the series [`dataSource`](../api/ejchart#members:indicators-datasource) to the indicator by setting the specific series name to the indicator by using the [`indicators.seriesName`](../api/ejchart#members:indicators-seriesname) property.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
              //  ...
              //Initializing Series
              series:[{
                  dataSource: chartData,
                  xName: "xDate",
                  high: "High",
                  low: "Low",
                  open: "Open",
                  close: "Close", 
                  //Set name to series
                  name: 'Hilo',
                  //  ...
            }],

            //Initializing Indicators    
            indicators: [{
                //Set Hilo series dataSource to indicator using seriesName
                seriesName: "Hilo",
                //  ...
	     }],
            //  ...
     });
    });
}

{% endhighlight %}


Also, you can add data to the indicator directly by using the [`dataSource`](../api/ejchart#members:indicators-datasource) option of the indicator.  

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            //  ...
            //Initializing Indicators    
            indicators: [{
                   //Add dataSource to indicator directly
                    dataSource: chartData,
                    xName: "xDate",
                    high: "High",
                    low: "Low",
                    open: "Open",
                    close: "Close",                
                    //  ...
	       }],
            //  ...
     });

{% endhighlight %}

	
## Indicator Types

### Accumulation Distribution

To create an Accumulation Distribution indicator, set the [`indicators.type`](../api/ejchart#members:indicators-type) as **"accumulationdistribution"**. Accumulation Distribution require **‘volume’** field additionally with the [`dataSource`](../api/ejchart#members:indicators-datasource) to calculate the signal line.

{% highlight javascript %}


          var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // Initializing Series
              series:[{
                       name: "Hilo",
                       dataSource: chartData,
                       xName: "xDate",
                       high: "High",
                       low: "Low",
                       open: "Open",
                       close: "Close",
                       //Add additional volume field to data source for accumulation distribution
                       volume: "Volume",
                       //  ...
                   }],
               //Initializing Indicators    
               indicators: [{
                     seriesName: "Hilo",
                     //Set indicator type
                     type: "accumulationdistribution", 
                     //  ...
	        }],
            // ...   
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img1.png)


### Average True Range (ATR)

You can create an ATR indicator by setting the [`indicators.type`](../api/ejchart#members:indicators-type) as **"atr"** in the [`indicators`](../api/ejchart#members:indicators). 

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...
            //Initializing Indicators    
            indicators: [{
                 //Set indicator type
                 type: "atr", 
                 //  ...
	      }],
            // ...   
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img2.png)

### Bollinger Band 

Bollinger Band indicator is created by setting the [`indicators.type`](../api/ejchart#members:indicators-type) as **"bollingerband"**. It contains three lines, namely upper band, lower band and signal line. Bollinger Band default value of the period is 14 and standardDeviations is 2.

{% highlight javascript %}


          var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: " bollingerband", 
                   //  ...
	         }],
            // ...   
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img3.png)


### Exponential Moving Average (EMA)

To render an EMA indicator, you have to set the [`indicators.type`](../api/ejchart#members:indicators-type) as **"ema"**.  

{% highlight javascript %}


          var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "ema", 
                   //  ...
	         }],
            // ...   
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img4.png)


### Momentum 

Momentum Technical indicator is created by setting the [`indicators.type`](../api/ejchart#members:indicators-type) as **"momentum"**. The momentum indicator renders two lines, namely upper band and signal line. Upper band always rendered at the value 100 and the signal line is calculated based on the momentum of the data.

{% highlight javascript %}


          var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "momentum", 
                   //  ...
	         }],
            // ... 
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img5.png)


### Moving Average Convergence Divergence (MACD)

To render an MACD indicator, you have to set the [`indicators.type`](../api/ejchart#members:indicators-type) as **"macd"**.  MACD indicator contains MACD line, Signal line and Histogram column. Histogram is used to differentiate MACD and signal line.

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "macd", 
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img6.png)


#### macdType

By using the [`macdType`](../api/ejchart#members:indicators-macdtype) enumeration property, you can change the MACD rendering as *line*, *histogram* or *both*. 

{% highlight javascript %}


        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   type: "macd", 
                   //Set macd draw type
                   macdType: "histogram", 
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img7.png)


### Relative Strength Index (RSI)

To render the RSI indicator, set the [`indicators.type`](../api/ejchart#members:indicators-type) as **"rsi"**. It contains three lines, namely upper band, lower band and signal line. Upper and lower band always render at value 70 and 30 respectively and signal line is calculated based on the **RSI** formula.

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "rsi",
                   //  ...
	         }],
            // ...
        });


{% endhighlight %}


![](Technical-Indicators_images/Technical-Indicators_img8.png)


### Simple Moving Average (SMA)

To render the SMA indicator, you should specify the [`indicators.type`](../api/ejchart#members:indicators-type) as **"sma"**.  

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "sma",
                   //  ...
	         }],
            // ...
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img9.png)


### Stochastic 

For the Stochastic indicator, you need to set the [`indicators.type`](../api/ejchart#members:indicators-type) as **"stochastic"**. The Stochastic indicator renders four lines namely, upper line, lower line, stochastic line and the signal line. Upper line always rendered at value 80 and the lower line is rendered at value 20. Stochastic and Signal Lines are calculated based on the stochastic formula.

{% highlight javascript %}


        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...            
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "stochastic",
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img10.png)


### Triangular Moving Average (TMA)

To render the TMA indicator, you should specify the [`indicators.type`](../api/ejchart#members:indicators-type) as **"tma"**. 

{% highlight javascript %}


        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "tma",
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img11.png)


## Enable Tooltip 

To display the indicator tooltip, use [`visible`](../api/ejchart#members:indicators-tooltip) option of the [`indicators.tooltip`](../api/ejchart#members:indicators-tooltip). Also, you can change and customize the tooltip color, border, format and font properties similar to the series tooltip.

{% highlight javascript %}


         var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //  ...
                   tooltip: {
                        //Enable tooltip for indicator
                        visible: true
                      },
	         }],
            // ...  
        });


{% endhighlight %}

![](Technical-Indicators_images/Technical-Indicators_img12.png)



