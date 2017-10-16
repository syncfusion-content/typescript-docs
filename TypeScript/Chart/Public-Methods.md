---
layout: post
title: Public methods in Chart
description: Learn what are all the public methods available and what are all the parameters need to pass for those methods.                    
platform: typescript
control: Chart
documentation: ug
---

# Public Methods

### animate(options)
{:#methods:animate}


Animates the series and/or indicators in Chart. When parameter is not passed to this method, then all the series and indicators present in Chart are animated.

Following are the parameters that you can pass to this method.


#### Returns: void


<table class="params">
<thead>
<tr>
<th>Parameters</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">If an array collection is passed as parameter, series and indicator objects passed in array collection are animated.
<br/><br/>
Example

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
//animating series array
chartObj.animate(chartObj.model.series);
{% endhighlight %}

<br/>
If a series or indicator object is passed to this method, then the specific series or indicator is animated.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
//animating a specific indicator
chartObj.animate(chartObj.model.indicators[0]);
{% endhighlight %}
</td>
</tr>
</tbody>
</table>


### print()
{:#methods:print}

Prints the rendered chart.


#### Returns: void


#### Example


{% highlight js %}
// Print Chart
var chartObj = $("#container").data("ejChart");
chartObj.print();
{% endhighlight %}

If you wish to print multiple charts on a same page, then you need to pass the ID of those elements as arguments to the print method.

<div id="container1"></div> 
<div id="container2"></div> 

{% highlight js %}
// Print Chart
var chartObj = $("#container1").data("ejChart");
chartObj.print("container1","container2");
{% endhighlight %}


### export(type, URL, exportMultipleChart)
{:#methods:export}



Exports chart as an image or to an excel file. Chart can be exported as an image only when exportCanvasRendering option is set to true.

Following are the parameters that you can pass to this method,



#### Returns: object



<table class="params">
<thead>
<tr>
<th>Parameters</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Type of the export operation to be performed. Following are the two export types that are supported now,
<br/>
1. 'image'
2. 'excel'
<br/><br./>
Example

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export(‘image’);
{% endhighlight %}
</td>
</tr>
<tr>
<td class="name">URL</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">
URL of the service, where the chart will be exported to excel.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export("excel", 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport')
{% endhighlight %}
</td>
</tr>
<tr>
<td class="name">
exportMultipleChart</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">
When this parameter is true, all the chart objects initialized to the same document are exported to a single excel file. This is an optional parameter. By default, it is false.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export("excel", 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport', true)
{% endhighlight %}
</td>
</tr>
</tbody>
</table>




### redraw()
{:#methods:redraw}




Redraws the entire chart. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.


#### Returns: void


#### Example


{% highlight js %}
// Redraw Chart
var chartObj = $("#container").data("ejChart");
chartObj.redraw();
{% endhighlight %}


{% highlight js %}
 
$("#container").ejChart("redraw");      
{% endhighlight %}