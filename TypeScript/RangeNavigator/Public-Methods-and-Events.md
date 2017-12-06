---
layout: post
title: Populate-Data
description: Populate Data
platform: typescript
control: RangeNavigator
documentation: ug
---

## Methods








### _destroy ()









destroy the range navigator widget



{% highlight ts %}

<div id="range"></div> 

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RangeNavigatorComponent {
    $(function () {
         var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
        //..//   
        });
       // destroy the range navigator
     sample.destroy(); 
    });
});
}


{% endhighlight %}








## Events








### load









Fires on load of range navigator.


{% highlight ts %}

<script>

//load event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              load: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### loaded









Fires after range navigator is loaded.

{% highlight ts %}

<script>

//loaded event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              loaded: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}









### rangeChanged









Fires on changing the range of range navigator.


{% highlight ts %}

<script>

//rangeChanged event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              rangeChanged: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### scrollChanged



Fires on changing the scrollbar position of range navigator.




{% highlight ts %}

<script>

//scrollChanged event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              scrollChanged: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}





### scrollStart



Fires on when starting to change the scrollbar position of range navigator.



{% highlight ts %}

<script>

//scrollStart event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              scrollStart: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### selectedRangeStart




Fires on when starting to change the slider position of range navigator.






{% highlight ts %}

<script>

//selectedRangeStart event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              selectedRangeStart: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### selectedRangeEnd 




Fires when the selection  ends in the range navigator





{% highlight ts %}

<script>

//selectedRangeEnd event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              selectedRangeEnd: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### scrollEnd



Fires on changes ending the scrollbar position of range navigator.





{% highlight ts %}

<script>

//scrollEnd event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.RangeNavigator($("#range"), {
              scrollEnd: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



