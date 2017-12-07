---
layout: post
title: Public Methods and Events
description: Public Methods and Events
platform: Typescript
control: Sparkline
documentation: ug
---


## Methods


### redraw()


Redraws the entire sparkline. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.

{% highlight html %}
 
<div id="sparkline">Sparkline</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SparklineComponent {
    $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"),{
        //..//   
        });
       // Redraws the Sparkline
     sample.redraw(); 
    });
});
}

{% endhighlight %}




## Events



### load


Fires before loading the sparkline.



{% highlight javascript %}

<script>

//load event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
              load: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### loaded


Fires after loaded the sparkline.

{% highlight javascript %}

<script>

//loaded event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
              loaded: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### tooltipInitialize


Fires before rendering trackball tooltip. You can use this event to customize the text displayed in trackball tooltip.



{% highlight javascript %}

<script>

//tooltip initialize event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
              tooltipInitialize: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### seriesRendering

Fires before rendering a series. This event is fired for each series in Sparkline.



{% highlight javascript %}

<script>

//seriesRendering event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
           seriesRendering: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### pointRegionMouseMove


Fires when mouse is moved over a point. 

{% highlight javascript %}

<script>

//pointRegionMouseMove event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
          pointRegionMouseMove: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}






### pointRegionMouseClick


Fires on clicking a point in sparkline. You can use this event to handle clicks made on points.



{% highlight javascript %}

<script>

//pointRegionMouseClick event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
           pointRegionMouseClick: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### sparklineMouseMove


Fires on moving mouse over the sparkline.



{% highlight javascript %}

<script>

//mouse move event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
           sparklineMouseMove: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### sparklineMouseLeave


Fires on moving mouse outside the sparkline.



{% highlight javascript %}

<script>

//mouse leave event for sparkline
  $(function () {
        var sample = new ej.datavisualization.Sparkline($("#Sparkline"), {
           sparklineMouseLeave: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



