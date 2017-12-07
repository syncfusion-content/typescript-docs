---
layout: post
title: Methods and Events
description: methods and events in treemap
platform: typescript
control: TreeMap
documentation: ug
---

## Methods

### refresh()


Method to reload treemap with updated values.



{% highlight html %}
 
<div id="treeMap"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"),{
        //..//   
        });
 
     sample.refresh(); 
    });
});
}

{% endhighlight %}



## Events

### treeMapItemSelected


Triggers on treemap item selected.


{% highlight javascript %}

<script>

//treeMapItemSelected event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              treeMapItemSelected: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### drillStarted


Triggers when drilldown is started



{% highlight javascript %}

<script>

//drillStarted event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              drillStarted: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### drillDownItemSelected


Triggers on treemap  drilldown  item  selected.




{% highlight javascript %}

<script>

//drillDownItemSelected event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              drillDownItemSelected: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### headerTemplateRendering


Triggers before rendering the treemap drilldown header template



{% highlight javascript %}

<script>

//headerTemplateRendering event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              headerTemplateRendering: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### refreshed


Triggers after refreshing the treemap items.


 
{% highlight javascript %}

<script>

//refreshed event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              refreshed: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### treeMapGroupSelected


Triggers when the group selection is performed on treemap items.


{% highlight javascript %}

<script>

//treeMapGroupSelected event for tree map
  $(function () {
        var sample = new ej.datavisualization.TreeMap($("#treeMap"), {
              treeMapGroupSelected: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

