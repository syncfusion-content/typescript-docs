---
layout: post
title: Events-and-Public-Methods
description: events and public methods
platform: typescript
control: Circular Gauge
documentation: ug
---

# Methods and Events

## Public Methods

### Destroying the Circular Gauge

The `destroy` method is used to destroy the **CircularGauge** widget. All events bound using this._on will be unbind automatically and bring the control to pre-init state.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });
       // destroy the CircularGauge
     sample.destroy(); 
    });
});
}


{% endhighlight %}

### Getting Back Needle Length

The `getBackNeedleLength` method is used to get the needle length of **CircularGauge**.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getBackNeedleLength(); 
    });
});
}

{% endhighlight %}

### Getting Custom Label Angle

The `getCustomLabelAngle` method is used to get the angle of custom label.

{% highlight javascript %}
 
<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getCustomLabelAngle(); 
    });
});
}


{% endhighlight %}

### Getting Custom Label value

The `getCustomLabelValue` method is used to get the value of custom label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getCustomLabelValue(); 
    });
});
}

{% endhighlight %}

### Getting Label Angle

The `getLabelAngle` method is used to get angle of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getLabelAngle(); 
    });
});
}

{% endhighlight %}

### Getting Label Distance From Scale

The `getLabelDistanceFromScale` method is used to get the distance value from scale for label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getLabelDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Getting Label Placement

The `getLabelPlacement` method is used to get placement of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getLabelPlacement(); 
    });
});
}

{% endhighlight %}

### Getting Label Style

The `getLabelStyle` method is used to get style of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getLabelStyle(); 
    });
});
}

{% endhighlight %}

### Getting Major Interval Value

The `getMajorIntervalValue` method is used to get major interval value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMajorIntervalValue(); 
    });
});
}

{% endhighlight %}

### Getting Maker Distance From Scale

The `getMarkerDistanceFromScale` method is used to get distance from scale value of marker.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMarkerDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Getting Maker Style

The `getMarkerStyle` method is used to get distance from scale value of marker.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMarkerStyle(); 
    });
});
}

{% endhighlight %}

### Getting Maximum Value

The `getMaximumValue` method is used to get maximum value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMaximumValue(); 
    });
});
}

{% endhighlight %}

### Getting Minimum Value

The `getMinimumValue` method is used to get minimum value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMinimumValue(); 
    });
});
}

{% endhighlight %}

### Getting Minor Interval Value

The `getMinorIntervalValue` method is used to get minor interval value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getMinorIntervalValue(); 
    });
});
}

{% endhighlight %}

### Getting Needle Style

The `getNeedleStyle` method is used to get style of needle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getNeedleStyle(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Cap Border Width

The `getPointerCapBorderWidth` method is used to get border width of pointer cap.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerCapBorderWidth(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Cap Radius

The `getPointerCapRadius` method is used to get radius of pointer cap.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerCapRadius(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Length

The `getPointerLength` method is used to get pointer length.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerLength(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Needle Type

The `getPointerNeedleType` method is used to get needle type of pointer.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerNeedleType(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Placement

The `getPointerPlacement` method is used to get placement of pointer.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerPlacement(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Value

The `getPointerValue` method is used to get pointer value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerValue(); 
    });
});
}

{% endhighlight %}

### Getting Pointer Value

The `getPointerWidth` method is used to get pointer width.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getPointerWidth(); 
    });
});
}

{% endhighlight %}

### Getting Range Border Width

The `getRangeBorderWidth` method is used to get border width of range.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangeBorderWidth(); 
    });
});
}

{% endhighlight %}

### Getting Range Distance From Scale

The `getRangeDistanceFromScale` method is used to get range distance from scale.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangeDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Getting Range End Value

The `getRangeEndValue` method is used to get end value of range.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangeEndValue(); 
    });
});
}

{% endhighlight %}

### Getting Range Position

The `getRangePosition` method is used to get range position.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangePosition(); 
    });
});
}

{% endhighlight %}

### Getting Range Size

The `getRangeSize` method is used to get range size.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangeSize(); 
    });
});
}

{% endhighlight %}

### Getting Range Start Value

The `getRangeStartValue` method is used to get range start value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getRangeStartValue(); 
    });
});
}

{% endhighlight %}

### Getting Scale Bar Size

The `getScaleBarSize` method is used to get scale bar size.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getScaleBarSize(); 
    });
});
}

{% endhighlight %}

### Getting Scale Border Width

The `getScaleBorderWidth` method is used to get border width of scale.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getScaleBorderWidth(); 
    });
});
}

{% endhighlight %}

### Getting Scale Direction

The `getScaleDirection` method is used to get scale direction.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getScaleDirection(); 
    });
});
}

{% endhighlight %}

### Getting Scale Radius

The `getScaleRadius` method is used to get scale radius.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getScaleRadius(); 
    });
});
}

{% endhighlight %}

### Getting Start Angle

The `getStartAngle` method is used to get start angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getStartAngle(); 
    });
});
}

{% endhighlight %}

### Getting Sub Gauge Location

The `getSubGaugeLocation` method is used to get location of subGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getSubGaugeLocation(); 
    });
});
}

{% endhighlight %}

### Getting Sweep Angle

The `getSweepAngle` method is used to get sweep angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getSweepAngle(); 
    });
});
}

{% endhighlight %}

### Getting Tick Angle

The `getTickAngle` method is used to get tick angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickAngle(); 
    });
});
}

{% endhighlight %}

### Getting Tick Distance From Scale

The `getTickDistanceFromScale` method is used to get tick distance from scale value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Getting Tick Height

The `getTickHeight` method is used to get tick height.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickHeight(); 
    });
});
}

{% endhighlight %}

### Getting Tick Placement

The `getTickPlacement` method is used to get tick placement.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickPlacement(); 
    });
});
}

{% endhighlight %}

### Getting Tick Style

The `getTickStyle` method is used to get tick style.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickStyle(); 
    });
});
}

{% endhighlight %}

### Getting Tick Width

The `getTickWidth` method is used to get tick width.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.getTickWidth(); 
    });
});
}

{% endhighlight %}

### Setting IncludeFirstValue

The `includeFirstValue` method is used to set includeFirstValue.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.includeFirstValue(); 
    });
});
}

{% endhighlight %}

### Redrawing Circular Gauge

The `redraw` method is used to redraw the Circular Gauge widget.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.redraw(); 
    });
});
}

{% endhighlight %}

### Setting Back Needle Length

The `setBackNeedleLength` method is used to set the needle length of **CircularGauge**.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setBackNeedleLength(); 
    });
});
}

{% endhighlight %}

### Setting Custom Label Angle

The `setCustomLabelAngle` method is used to set the angle of custom label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setCustomLabelAngle(); 
    });
});
}

{% endhighlight %}

### Setting Custom Label value

The `setCustomLabelValue` method is used to set the value of custom label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setCustomLabelValue(); 
    });
});
}

{% endhighlight %}

### Setting Label Angle

The `setLabelAngle` method is used to set angle of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setLabelAngle(); 
    });
});
}

{% endhighlight %}

### Setting Label Distance From Scale

The `setLabelDistanceFromScale` method is used to set the distance value from scale for label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setLabelDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Setting Label Placement

The `setLabelPlacement` method is used to set placement of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setLabelPlacement(); 
    });
});
}

{% endhighlight %}

### Setting Label Style

The `setLabelStyle` method is used to set style of label.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setLabelStyle(); 
    });
});
}

{% endhighlight %}

### Setting Major Interval Value

The `setMajorIntervalValue` method is used to set major interval value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMajorIntervalValue(); 
    });
});
}

{% endhighlight %}

### Setting Maker Distance From Scale

The `setMarkerDistanceFromScale` method is used to set distance from scale value of marker.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMarkerDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Setting Maker Style

The `setMarkerStyle` method is used to set distance from scale value of marker.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMarkerStyle(); 
    });
});
}

{% endhighlight %}

### Setting Maximum Value

The `setMaximumValue` method is used to set maximum value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMaximumValue(); 
    });
});
}

{% endhighlight %}

### Setting Minimum Value

The `setMinimumValue` method is used to set minimum value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMinimumValue(); 
    });
});
}

{% endhighlight %}

### Setting Minor Interval Value

The `setMinorIntervalValue` method is used to set minor interval value of CircularGauge.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setMinorIntervalValue(); 
    });
});
}

{% endhighlight %}

### Setting Needle Style

The `setNeedleStyle` method is used to set style of needle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setNeedleStyle(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Cap Border Width

The `setPointerCapBorderWidth` method is used to set border width of pointer cap.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerCapBorderWidth(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Cap Radius

The `setPointerCapRadius` method is used to set radius of pointer cap.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerCapRadius(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Length

The `setPointerLength` method is used to set pointer length.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerLength(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Needle Type

The `setPointerNeedleType` method is used to set needle type of pointer.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerNeedleType(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Placement

The `setPointerPlacement` method is used to set placement of pointer.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerPlacement(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Value

The `setPointerValue` method is used to set pointer value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerValue(); 
    });
});
}

{% endhighlight %}

### Setting Pointer Value

The `setPointerWidth` method is used to set pointer width.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setPointerWidth(); 
    });
});
}

{% endhighlight %}

### Setting Range Border Width

The `setRangeBorderWidth` method is used to set border width of range.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangeBorderWidth(); 
    });
});
}

{% endhighlight %}

### Setting Range Distance From Scale

The `setRangeDistanceFromScale` method is used to set range distance from scale.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangeDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Setting Range End Value

The `setRangeEndValue` method is used to set end value of range.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangeEndValue(); 
    });
});
}

{% endhighlight %}

### Setting Range Position

The `setRangePosition` method is used to set range position.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangePosition(); 
    });
});
}

{% endhighlight %}

### Setting Range Size

The `setRangeSize` method is used to set range size.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangeSize(); 
    });
});
}

{% endhighlight %}

### Setting Range Start Value

The `setRangeStartValue` method is used to set range start value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setRangeStartValue(); 
    });
});
}

{% endhighlight %}

### Setting Scale Bar Size

The `setScaleBarSize` method is used to set scale bar size.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setScaleBarSize(); 
    });
});
}

{% endhighlight %}

### Setting Scale Border Width

The `setScaleBorderWidth` method is used to set border width of scale.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setScaleBorderWidth(); 
    });
});
}

{% endhighlight %}

### Setting Scale Direction

The `setScaleDirection` method is used to set scale direction.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setScaleDirection(); 
    });
});
}

{% endhighlight %}

### Setting Scale Radius

The `setScaleRadius` method is used to set scale radius.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setScaleRadius(); 
    });
});
}

{% endhighlight %}

### Setting Start Angle

The `setStartAngle` method is used to set start angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setStartAngle(); 
    });
});
}

{% endhighlight %}

### Setting Sub Gauge Location

The `setSubGaugeLocation` method is used to set location of subGauge.

{% highlight javascript %}


<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setSubGaugeLocation(); 
    });
});
}

{% endhighlight %}

### Setting Sweep Angle

The `setSweepAngle` method is used to set sweep angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setSweepAngle(); 
    });
});
}

{% endhighlight %}

### Setting Tick Angle

The `setTickAngle` method is used to set tick angle.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickAngle(); 
    });
});
}

{% endhighlight %}

### Setting Tick Distance From Scale

The `setTickDistanceFromScale` method is used to set tick distance from scale value.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickDistanceFromScale(); 
    });
});
}

{% endhighlight %}

### Setting Tick Height

The `setTickHeight` method is used to set tick height.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickHeight(); 
    });
});
}

{% endhighlight %}

### Setting Tick Placement

The `setTickPlacement` method is used to set tick placement.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickPlacement(); 
    });
});
}

{% endhighlight %}

### Setting Tick Style

The `setTickStyle` method is used to set tick style.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickStyle(); 
    });
});
}

{% endhighlight %}

### Setting Tick Width

The `setTickWidth` method is used to set tick width.

{% highlight javascript %}

<div id="CoreCircularGauge"></div> 

module CircularGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#CoreCircularGauge"),{
        //..//   
        });       
     sample.setTickWidth(); 
    });
});
}

{% endhighlight %}


## Events

### Draw Custom Label

The `drawCustomLabel` event is triggered while custom labels are drawn on the gauge. 

{% highlight javascript %}

<script>

//drawCustomLabel event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawCustomLabel: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}


### Draw Indicators

The `drawIndicators` event is triggered while indicators are being drawn on the gauge. 

{% highlight javascript %}

<script>

//drawIndicators event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawIndicators: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}

### Draw Labels

The `drawLabels` event is triggered while labels are being drawn on the gauge. 

{% highlight javascript %}

<script>

//drawLabels event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawLabels: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}



### Draw Pointer Cap

The `drawPointerCap` event is triggered while pointer cap is being drawn on the gauge. 

{% highlight javascript %}

<script>

//drawPointerCap event for circular gauge
  $(function () {
       var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawPointerCap: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Draw Pointers

The `drawPointers` event is triggered while pointer cap is being drawn on the gauge. 

{% highlight javascript %}

<script>

//drawPointers event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawPointers: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Draw Range

The `drawRange` event is triggered when ranges starts to be drawn on the gauge. 

{% highlight javascript %}

<script>

//drawRange event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawRange: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Draw Ticks

The `drawTicks` event is triggered when ticks are being drawn on the gauge. 

{% highlight javascript %}

<script>

//drawTicks event for circular gauge
  $(function () {
         var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              drawTicks: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Load

The `load` event is triggered when gauge starts to load. 

{% highlight javascript %}

<script>

//load event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              load: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Mouse Click

The `mouseClick` event is triggered when left mouse button is clicked. 

{% highlight javascript %}

<script>

//mouseClick event for circular gauge
  $(function () {
        var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              mouseClick: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Mouse Click Move

The `mouseClickMove` event is triggered when clicking and dragging the mouse pointer over the gauge pointer. 

{% highlight javascript %}

<script>

//mouseClickMove event for circular gauge
  $(function () {
         var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              mouseClickMove: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Mouse Click Up

The `mouseClickUp` event is triggered when clicking and dragging the mouse pointer over the gauge pointer. 

{% highlight javascript %}

<script>

//mouseClickUp event for circular gauge
  $(function () {
         var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              mouseClickUp: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Render Complete

The `renderComplete` event is triggered when rendering of the gauge is completed.

{% highlight javascript %}

<script>

//renderComplete event for circular gauge
  $(function () {
       var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              renderComplete: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}

### Range Mouse Move

The `rangeMouseMove` event is triggered when moving mouse on ranges.

{% highlight javascript %}

<script>

//rangeMouseMove event for circular gauge
  $(function () {
       var sample = new ej.datavisualization.CircularGauge($("#gauge"), {
              rangeMouseMove: function () {
                 //..//
                }
            });
        });
       
</script>


{% endhighlight %}