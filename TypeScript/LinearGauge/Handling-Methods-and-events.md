---
layout: post
title: Handling methods and events
description: methods and events
platform: typescript
control: Linear Gauge
documentation: ug
---


##Events


### drawBarPointers

Triggers while the bar pointer are being drawn on the gauge, you can use `drawBarPointers` event.

{% highlight javascript %}

<script>

//drawBarPointers event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawBarPointers: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### drawCustomLabel

Triggers while the customLabel are being drawn on the gauge, you can use `drawCustomLabel` event.





{% highlight javascript %}

<script>

//drawCustomLabel event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawCustomLabel: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}





### drawIndicators

Triggers while the Indicator are being drawn on the gauge, you can use `drawIndicators` event.







{% highlight javascript %}

<script>

//drawIndicators event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawIndicators: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### drawLabels

Triggers while the label are being drawn on the gauge, you can use `drawLabels` event.







{% highlight javascript %}

<script>

//drawLabels event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawLabels: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### drawMarkerPointers

Triggers while the marker are being drawn on the gauge, you can use `drawMarkerPointers` event.








{% highlight javascript %}

<script>

//drawMarkerPointers event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawMarkerPointers: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### drawRange

Triggers while the range are being drawn on the gauge, you can use `drawRange` event.







{% highlight javascript %}

<script>

//drawRange event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawRange: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### drawTicks

Triggers while the ticks are being drawn on the gauge, you can use `drawTicks` event.







{% highlight javascript %}

<script>

//drawTicks event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              drawTicks: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### init

Triggers when the gauge is initialized, you can use `init`event.








{% highlight javascript %}

<script>

//init event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              init: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### load

Triggers while the gauge start to Load, you can use `load` event.







{% highlight javascript %}

<script>

//load event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              load: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}





### mouseClick

Triggers when the left mouse button is clicked, you can use `mouseClick` event.









{% highlight javascript %}

<script>

//mouseClick event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              mouseClick: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### mouseClickMove

Triggers when clicking and dragging the mouse pointer over the gauge pointer, you can use `mouseClickMove` event.








{% highlight javascript %}

<script>

//mouseClickMove event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              mouseClickMove: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}






### mouseClickUp


Triggers when the mouse click is released, you can use `mouseClickUp` event.








{% highlight javascript %}

<script>

//mouseClickUp event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              mouseClickUp: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### renderComplete

Triggers while the rendering of the gauge completed, you can use `renderComplete` event.







{% highlight javascript %}

<script>

//renderComplete event for linear gauge
  $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#gauge"), {
              renderComplete: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


## Methods


### destroy()

`Destroy` the linear gauge all events bound using this._on will be unbind automatically and bring the control to pre-init state.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.destroy(); 
    });
});
}

{% endhighlight %}




### getBarDistanceFromScale()

To get bar distance from scale in number, you can use `getBarDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getBarDistanceFromScale(); 
    });
});
}

{% endhighlight %}


### getBarPointerValue()

To get Bar Pointer Value in number, you can use `getBarPointerValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getBarPointerValue(); 
    });
});
}

{% endhighlight %}


### getBarWidth()

To get Bar Width in number, you can use `getBarWidth`method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getBarWidth(); 
    });
});
}

{% endhighlight %}



### getCustomLabelAngle()

To get CustomLabel Angle in number, you can use `getCustomLabelAngle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getCustomLabelAngle(); 
    });
});
}

{% endhighlight %}




### getCustomLabelValue()

To get CustomLabel Value in string, you can use `getCustomLabelValue` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getCustomLabelValue(); 
    });
});
}

{% endhighlight %}



### getLabelAngle()

To get Label Angle in number, you can use `getLabelAngle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getLabelAngle(); 
    });
});
}

{% endhighlight %}





### getLabelPlacement()

To get LabelPlacement in number, you can use `getLabelPlacement` method.







{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getLabelPlacement(); 
    });
});
}

{% endhighlight %}




### getLabelStyle()

To get LabelStyle in number, you can use `getLabelStyle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getLabelStyle(); 
    });
});
}

{% endhighlight %}




### getLabelXDistanceFromScale()

To get Label XDistance From Scale in number, you can use `getLabelXDistanceFromScale` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getLabelXDistanceFromScale(); 
    });
});
}

{% endhighlight %}





### getLabelYDistanceFromScale()

To get PointerValue in number, you can use `getLabelXDistanceFromScale` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getLabelYDistanceFromScale(); 
    });
});
}

{% endhighlight %}







### getMajorIntervalValue()

To get Major Interval Value in number, you can use `getMajorIntervalValue` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getMajorIntervalValue(); 
    });
});
}

{% endhighlight %}


### getMarkerStyle()

To get MarkerStyle in number, you can use `getMarkerStyle` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getMarkerStyle(); 
    });
});
}

{% endhighlight %}



### getMaximumValue()

To get Maximum Value in number, you can use `getMaximumValue` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getMaximumValue(); 
    });
});
}

{% endhighlight %}


### getMinimumValue()

To get PointerValue in number, you can use `getMinimumValue` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getMinimumValue(); 
    });
});
}

{% endhighlight %}


### getMinorIntervalValue()

To get Minor Interval Value in number, you can use `getMinorIntervalValue` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getMinorIntervalValue(); 
    });
});
}

{% endhighlight %}


### getPointerDistanceFromScale()

To get Pointer Distance From Scale in number, you can use `getPointerDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getPointerDistanceFromScale(); 
    });
});
}

{% endhighlight %}


### getPointerHeight()

To get PointerHeight in number, you can use `getPointerHeight` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getPointerHeight(); 
    });
});
}

{% endhighlight %}


### getPointerPlacement()

To get Pointer Placement in String, you can use `getPointerPlacement` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getPointerPlacement(); 
    });
});
}

{% endhighlight %}


### getPointerValue()

To get PointerValue in number, you can use `getPointerValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getPointerValue(); 
    });
});
}

{% endhighlight %}



### getPointerWidth()

To get PointerWidth in number, you can use `getPointerWidth` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getPointerWidth(); 
    });
});
}

{% endhighlight %}


### getRangeBorderWidth()

To get Range Border Width in number, you can use `getRangeBorderWidth` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeBorderWidth(); 
    });
});
}

{% endhighlight %}



### getRangeDistanceFromScale()

To get Range Distance From Scale in number, you can use `getRangeDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeDistanceFromScale(); 
    });
});
}

{% endhighlight %}


### getRangeEndValue()

To get Range End Value in number, you can use `getRangeEndValue` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeEndValue(); 
    });
});
}

{% endhighlight %}



### getRangeEndWidth()

To get Range End Width in number, you can use `getRangeEndWidth` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeEndWidth(); 
    });
});
}

{% endhighlight %}




### getRangePosition()

To get Range Position in number, you can use `getRangePosition` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangePosition(); 
    });
});
}

{% endhighlight %}



### getRangeStartValue()

To get Range Start Value in number, you can use `getRangeStartValue` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeStartValue(); 
    });
});
}

{% endhighlight %}







### getRangeStartWidth()

To get Range Start Width in number, you can use `getRangeStartWidth` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getRangeStartWidth(); 
    });
});
}

{% endhighlight %}



### getScaleBarLength()

To get ScaleBarLength in number, you can use `getScaleBarLength` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleBarLength(); 
    });
});
}

{% endhighlight %}


### getScaleBarSize()

To get Scale Bar Size in number, you can use `getScaleBarSize` method.






{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleBarSize(); 
    });
});
}

{% endhighlight %}


### getScaleBorderWidth()

To get Scale Border Width in number, you can use `getScaleBorderWidth` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleBorderWidth(); 
    });
});
}

{% endhighlight %}


### getScaleDirection()

To get Scale Direction in number, you can use `getScaleDirection` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleDirection(); 
    });
});
}

{% endhighlight %}



### getScaleLocation()

To get Scale Location in object, you can use `getScaleLocation` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleLocation(); 
    });
});
}

{% endhighlight %}



### getScaleStyle()

To get Scale Style in string, you can use `getScaleStyle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getScaleStyle(); 
    });
});
}

{% endhighlight %}



### getTickAngle()

To get Tick Angle in number, you can use `getTickAngle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickAngle(); 
    });
});
}

{% endhighlight %}



### getTickHeight()

To get Tick Height in number, you can use `getTickHeight` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickHeight(); 
    });
});
}

{% endhighlight %}


### getTickPlacement()

To get getTickPlacement in number, you can use `getTickPlacement` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickPlacement(); 
    });
});
}

{% endhighlight %}


### getTickStyle()

To get Tick Style in string, you can use `getTickStyle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickStyle(); 
    });
});
}

{% endhighlight %}


### getTickWidth()

To get Tick Width in number, you can use `getTickWidth` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickWidth(); 
    });
});
}

{% endhighlight %}

### getTickXDistanceFromScale()

To get get Tick XDistance From Scale in number, you can use `getTickXDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickXDistanceFromScale(); 
    });
});
}

{% endhighlight %}



### getTickYDistanceFromScale()

To get Tick YDistance From Scale in number, you can use `getTickYDistanceFromScale` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.getTickYDistanceFromScale(); 
    });
});
}

{% endhighlight %}



### scales()

Specifies the scales, you can use `scales` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.scales(); 
    });
});
}

{% endhighlight %}



### setBarDistanceFromScale()

To set setBarDistanceFromScale, you can use `setBarDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setBarDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### setBarPointerValue()

To set setBarPointerValue, you can use `setBarPointerValue`method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setBarPointerValue(); 
    });
});
}

{% endhighlight %}


### setBarWidth()

To set setBarWidth, you can use `setBarWidth` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setBarWidth(); 
    });
});
}

{% endhighlight %}


### setCustomLabelAngle()

To set setCustomLabelAngle, you can use `setCustomLabelAngle` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setCustomLabelAngle(); 
    });
});
}

{% endhighlight %}



### setCustomLabelValue()

To set setCustomLabelValue, you can use `setCustomLabelValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setCustomLabelValue(); 
    });
});
}

{% endhighlight %}



### setLabelAngle()

To set setLabelAngle, you can use `setLabelAngle` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setLabelAngle(); 
    });
});
}

{% endhighlight %}




### setLabelPlacement()

To set setLabelPlacement, you can use `setLabelPlacement`method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setLabelPlacement(); 
    });
});
}

{% endhighlight %}



### setLabelStyle()

To set setLabelStyle, you can use `setLabelStyle` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setLabelStyle(); 
    });
});
}

{% endhighlight %}



### setLabelXDistanceFromScale()

To set setLabelXDistanceFromScale, you can use `setLabelXDistanceFromScale` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setLabelXDistanceFromScale(); 
    });
});
}

{% endhighlight %}



### setLabelYDistanceFromScale()

To set setLabelYDistanceFromScale, you can use `setLabelYDistanceFromScale` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setLabelYDistanceFromScale(); 
    });
});
}

{% endhighlight %}



### setMajorIntervalValue()

To set setMajorIntervalValue, you can use `setMajorIntervalValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setMajorIntervalValue(); 
    });
});
}

{% endhighlight %}





### setMarkerStyle()

To set setMarkerStyle, you can use `setMarkerStyle`method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setMarkerStyle(); 
    });
});
}

{% endhighlight %}




### setMaximumValue()

To set setMaximumValue, you can use `setMaximumValue` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setMaximumValue(); 
    });
});
}

{% endhighlight %}



### setMinimumValue()

To set setMinimumValue, you can use `setMinimumValue` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setMinimumValue(); 
    });
});
}

{% endhighlight %}



### setMinorIntervalValue()

To set setMinorIntervalValue, you can use `setMinorIntervalValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setMinorIntervalValue(); 
    });
});
}

{% endhighlight %}



### setPointerDistanceFromScale()

To set setPointerDistanceFromScale, you can use `setPointerDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setPointerDistanceFromScale(); 
    });
});
}

{% endhighlight %}




### setPointerHeight()

To set PointerHeight, you can use `setPointerHeight` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setPointerHeight(); 
    });
});
}

{% endhighlight %}




### setPointerPlacement()

To set setPointerPlacement, you can use `setPointerPlacement` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setPointerPlacement(); 
    });
});
}

{% endhighlight %}




### setPointerValue()

To set PointerValue, you can use `setPointerValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setPointerValue(); 
    });
});
}

{% endhighlight %}





### setPointerWidth()

To set PointerWidth, you can use `setPointerWidth` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setPointerWidth(); 
    });
});
}

{% endhighlight %}




### setRangeBorderWidth()

To set setRangeBorderWidth, you can use `setRangeBorderWidth` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeBorderWidth(); 
    });
});
}

{% endhighlight %}




### setRangeDistanceFromScale()

To set setRangeDistanceFromScale, you can use `setRangeDistanceFromScale` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeDistanceFromScale(); 
    });
});
}

{% endhighlight %}




### setRangeEndValue()

To set setRangeEndValue, you can use `setRangeEndValue` method.





{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeEndValue(); 
    });
});
}

{% endhighlight %}




### setRangeEndWidth()

To set setRangeEndWidth, you can use `setRangeEndWidth` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeEndWidth(); 
    });
});
}

{% endhighlight %}




### setRangePosition()

To set setRangePosition, you can use `setRangePosition` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangePosition(); 
    });
});
}

{% endhighlight %}



### setRangeStartValue()

To set setRangeStartValue, you can use `setRangeStartValue` method.


{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeStartValue(); 
    });
});
}

{% endhighlight %}




### setRangeStartWidth()

To set setRangeStartWidth, you can use `setRangeStartWidth` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setRangeStartWidth(); 
    });
});
}

{% endhighlight %}





### setScaleBarLength()

To set setScaleBarLength, you can use `setScaleBarLength` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleBarLength(); 
    });
});
}

{% endhighlight %}



### setScaleBarSize()

To set setScaleBarSize, you can use `setScaleBarSize` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleBarSize(); 
    });
});
}

{% endhighlight %}




### setScaleBorderWidth()

To set setScaleBorderWidth, you can use `setScaleBorderWidth` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleBorderWidth(); 
    });
});
}

{% endhighlight %}




### setScaleDirection()

To set setScaleDirection, you can use `setScaleDirection` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleDirection(); 
    });
});
}

{% endhighlight %}



### setScaleLocation()

To set setScaleLocation, you can use `setScaleLocation` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleLocation(); 
    });
});
}

{% endhighlight %}





### setScaleStyle()

To set setScaleStyle, you can use `setScaleStyle` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setScaleStyle(); 
    });
});
}

{% endhighlight %}



### setTickAngle()

To set setTickAngle, you can use `setTickAngle` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setTickAngle(); 
    });
});
}

{% endhighlight %}



### setTickHeight()

To set setTickHeight, you can use `setTickHeight` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
 
     sample.setTickHeight(); 
    });
});
}

{% endhighlight %}




### setTickPlacement()

To set setTickPlacement, you can use `setTickPlacement` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
     sample.setTickPlacement(); 
    });
});
}

{% endhighlight %}



### setTickStyle()

To set setTickStyle, you can use `setTickStyle` method.




{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
     sample.setTickStyle(); 
    });
});
}

{% endhighlight %}




### setTickWidth()

To set setTickWidth, you can use `setTickWidth` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });       
     sample.setTickWidth(); 
    });
});
}

{% endhighlight %}




### setTickXDistanceFromScale()

To set setTickXDistanceFromScale, you can use `setTickXDistanceFromScale` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
     sample.setTickXDistanceFromScale(); 
    });
});
}

{% endhighlight %}




### setTickYDistanceFromScale()

To set setTickYDistanceFromScale, you can use `setTickYDistanceFromScale` method.



{% highlight html %}
 
<div id="LinearGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module LinearGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.LinearGauge($("#LinearGauge1"),{
        //..//   
        });
       
     sample.setTickYDistanceFromScale(); 
    });
});
}

{% endhighlight %}




