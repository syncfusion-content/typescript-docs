---
layout: post
title: Public Methos and Events
description: Learn how to add public methos and events to Sunburstchart .
platform: ts
control: Sunburst Chart
documentation: ug

---

## Methods


### redraw()

**redraw** the entire sunburst. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.


#### Example


{% highlight html %}
 
<div id="Sunburst">Sunburst</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SunburstChartComponent {
    $(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
        //..//   
        });
       // Redraws the Sunburst
     sample.redraw(); 
    });
});
}

{% endhighlight %}


### destroy ()

**destroy** the sunburst


#### Example

{% highlight html %}
 
<div id="Sunburst">Sunburst</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SunburstChartComponent {
    $(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
        //..//   
        });
       // Destroys the Sunburst
     sample.destroy(); 
    });
});
}

{% endhighlight %}


## Events

### load

Fires before loading, you can use **load** event.

#### Example

{% highlight javascript %}
 
//load event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              load: function () {
                 //..//
                }
            });
        });

{% endhighlight %}



### preRender

Fires before rendering sunburst, you can use **preRender** event. 


#### Example


{% highlight javascript %}
 
//preRender event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              preRender: function () {
                 //..//
                }
            });
        });

{% endhighlight %}



### loaded

Fires after rendering sunburst, you can use **loaded** event.  


#### Example


{% highlight javascript %}
 
//loaded event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              loaded: function () {
                 //..//
                }
            });
        });

{% endhighlight %}


### dataLabelRendering

Fires before rendering the data label, you can use **dataLabelRendering**event. 


#### Example


{% highlight javascript %}
 
//data label rendering event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              dataLabelRendering: function () {
                 //..//
                }
            });
        });

{% endhighlight %}


### segmentRendering

Fires before rendering each segment, you can use **segmentRendering** event. 


#### Example


{% highlight javascript %}
 
//segment rendering event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              segmentRendering: function () {
                 //..//
                }
            });
        });


{% endhighlight %}



### titleRendering

Fires before rendering sunburst title, you can use **titleRendering** event.  


#### Example


{% highlight javascript %}
 
//title rendering event for sunburst

$(function () {
 var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              titleRendering: function () {
                 //..//
                }
            });
        });

{% endhighlight %}



### tooltipInitialize


Fires during initialization of tooltip, you can use **tooltipInitialize** event.  


#### Example


{% highlight javascript %}
 
//tooltip initialize event for sunburst

$(function () {
var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              tooltipInitialize: function () {
                 //..//
                }
            });
        });

{% endhighlight %}



### pointRegionClick

Fires after clicking the point in sunburst, you can use **pointRegionClick** event. 


#### Example


{% highlight javascript %}
 
//point region click event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              pointRegionClick: function () {
                 //..//
                }
            });
        });

{% endhighlight %}


### pointRegionMouseMove

Fires while moving the mouse over sunburst points, you can use **pointRegionMouseMove** event. 

#### Example


{% highlight javascript %}
 
//point region mouse move event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
            pointRegionMouseMove: function () {
                 //..//
                }
            });
        });

{% endhighlight %}


### drillDownClick

Fires when clicking the point to perform drilldown, you can use **drillDownClick** event.  


#### Example


{% highlight javascript %}
 
//drill down click event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              drillDownClick: function () {
                 //..//
                }
            });
        });


{% endhighlight %}


### drillDownBack

Fires when resetting drilldown points, you can use **drillDownBack** event.  


#### Example


{% highlight javascript %}
 
//drill down back event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              drillDownBack: function () {
                 //..//
                }
            });
        });

{% endhighlight %}



### drillDownReset


Fires after resetting the sunburst points, you can use **drillDownReset** event.  


#### Example


{% highlight javascript %}
 
//drill down reset event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              drillDownReset: function () {
                 //..//
                }
            });
        });

{% endhighlight %}

### legendItemRendering


Fires before rendering the legend item, you can use **legendItemRendering** event. 


#### Example


{% highlight javascript %}
 
//legend item rendering event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              legendItemRendering: function () {
                 //..//
                }
            });
        });
{% endhighlight %}


### legendItemClick


Fires when clicking the legend item, you can use **legendItemClick** event.


#### Example


{% highlight javascript %}
 
//legend item click event for sunburst

$(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"), {
              legendItemClick: function () {
                 //..//
                }
            });
        });

{% endhighlight %}

