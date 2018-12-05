---
layout: post
title: Syncfusion EJ1 Maps - Public Methods and Events
description: Public methods and events
platform: typescript
control: Maps
documentation: ug
---


## Methods

### navigateTo(latitude, longitude, level)


Method for navigating to specific shape based on latitude, longitude and zoom level.




{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.navigateTo(); 
    });
});
}

{% endhighlight %}



### pan(direction)


Method to perform map panning



{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.pan(); 
    });
});
}

{% endhighlight %}



### refresh()


Method to reload the map.




{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.refresh(); 
    });
});
}

{% endhighlight %}



### refreshLayers()


Method to reload the shapeLayers with updated values




{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.refreshLayers(); 
    });
});
}

{% endhighlight %}



### refreshNavigationControl(navigation)


Method to reload the navigation control with updated values.




{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.refreshNavigationControl(); 
    });
});
}

{% endhighlight %}



### zoom(level, isAnimate)


Method to perform map zooming.




{% highlight html %}
 
<div id="map"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module MapComponent {
    $(function () {
        var sample = new ej.datavisualization.Map($("#map"),{
        //..//   
        });
 
     sample.zoom(); 
    });
});
}

{% endhighlight %}




## Events

### markerSelected


Triggered on selecting the map markers.


{% highlight javascript %}

<script>

//markerSelected event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              markerSelected: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### mouseLeave


Triggers while leaving the hovered map shape


{% highlight javascript %}

<script>

//mouseLeave event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              mouseLeave: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### mouseover


Triggers while hovering the map shape.


{% highlight javascript %}

<script>

//mouseover event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              mouseover: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### onRenderComplete


Triggers once map render completed.


{% highlight javascript %}

<script>

//onRenderComplete event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              onRenderComplete: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### panned


Triggers when map panning ends.


{% highlight javascript %}

<script>

//panned event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              panned: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### shapeSelected


Triggered on selecting the map shapes.


{% highlight javascript %}

<script>

//shapeSelected event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              shapeSelected: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### zoomedIn


Triggered when map is zoomed-in.


{% highlight javascript %}

<script>

//zoomedIn event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              zoomedIn: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### zoomedOut


Triggers when map is zoomed out.



{% highlight javascript %}

<script>

//zoomedOut event for Map 
  $(function () {
        var sample = new ej.datavisualization.Map($("#map"), {
              zoomedOut: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>

