---
layout: post
title: Methods-Events
description: methods and events in bullet graph
platform: typescript
control: BulletGraph	
documentation: ug
---

# Methods

## destroy()

**Destroy** method is used to destroy the bullet graph control.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
        //..//   
        });
       // Destroy Bullet graph
     sample.destroy(); 
    });
}

{% endhighlight %}


## redraw()

**Redraw** method is used to redraw the bullet graph with updated values.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
        //..//   
        });
       // Redraws the  Bullet graph
     sample.redraw(); 
    });
}

{% endhighlight %}

## setComparativeMeasureSymbol(index, measure)

To set the comparative measure in bullet graph, you can use **setComparativeMeasureSymbol** method.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
        //..//   
        });
    // set the value for comparative measure
     sample.setComparativeMeasureSymbol(1,7); 
    });
}

{% endhighlight %}

## setFeatureMeasureBarValue(index, measure)

To set the value for feature measure bar, you can use **setFeatureMeasureBarValue** method.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module BulletgraphComponent {
    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
        //..//   
        });
    // set the value for feature measure bar.
     sample.setFeatureMeasureBarValue(1,8); 
    });
}

{% endhighlight %}


# Events

## drawCaption

**drawCaption** event will fire before rendering bullet graph caption.

{% highlight javascript %}
 
<script>

//drawCaption event for bullet graph
  $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawCaption: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

## drawCategory

**drawCategory** event will fire while rendering the category.

{% highlight javascript %}

<script> 
//drawCategory event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawCategory: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawComparativeMeasureSymbol

**drawComparativeMeasureSymbol** event fires on rendering the comparative measure symbol.

{% highlight javascript %}
 
<script>
//drawComparativeMeasureSymbol event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawComparativeMeasureSymbol: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawFeatureMeasureBar

**drawFeatureMeasureBar** event fires on rendering the feature measure bar.

{% highlight javascript %}
 
<script>
//drawFeatureMeasureBar event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawFeatureMeasureBar: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawIndicator

**drawIndicator** event fires on rendering the indicator of the bullet graph.

{% highlight javascript %}
 
<script>
//drawIndicator event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawIndicator: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawLabels

**drawLabels** event fires on rendering the bullet graph labels.

{% highlight javascript %}
 
<script>
//drawLabels event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawLabels: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawTicks

**drawTicks** event fires while drawing the ticklines of the bullet graph.

{% highlight javascript %}
 
<script>
//drawTicks event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawTicks: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## drawQualitativeRanges

**drawQualitativeRanges** event fires while rendering the qualitative ranges.

{% highlight javascript %}
 
<script>
//drawQualitativeRanges event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
              drawQualitativeRanges: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}

## load

**load** event fires on loading the bullet graph.

{% highlight javascript %}
 
<script>
//load event for bullet graph
$(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"), {
             load: function () {
                 //..//
                }
            });
        });
</script>

{% endhighlight %}
