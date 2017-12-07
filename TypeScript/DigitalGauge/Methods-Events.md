---
layout: post
title: Methods and Events in Digital Gauge
description: explains the methods and events in digital gauge
platform: typescript
control: Digital Gauge
documentation: ug
---

## Methods





### destroy()



To destroy the digital gauge



{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.destroy(); 
    });
});
}

{% endhighlight %}






### exportImage(fileName, fileType)


To export Digital Gauge as Image




{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.exportImage(); 
    });
});
}

{% endhighlight %}






### getPosition(itemIndex)


Gets the location of an item that is displayed on the gauge.




{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.getPosition(); 
    });
});
}

{% endhighlight %}






### getValue(itemIndex)

ClientSideMethod getValue Gets the value of an item that is displayed on the gauge



{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalrGauge1"),{
        //..//   
        });
 
     sample.getValue(); 
    });
});
}

{% endhighlight %}







### refresh()


Refresh the digital gauge widget




{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.refresh(); 
    });
});
}

{% endhighlight %}





### setPosition(itemIndex, value)


ClientSideMethod Set Position Sets the location of an item to be displayed in the gauge



{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.setPosition(); 
    });
});
}

{% endhighlight %}





### setValue(itemIndex, value)

ClientSideMethod SetValue Sets the value of an item to be displayed in the gauge.



{% highlight html %}
 
<div id="DigitalGauge1"></div> 

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DigitalGaugeComponent {
    $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#DigitalGauge1"),{
        //..//   
        });
 
     sample.setValue(); 
    });
});
}

{% endhighlight %}






## Events





### init

Triggers when the gauge is initialized.

{% highlight javascript %}

<script>

//init event for Digital gauge
  $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#gauge"), {
              init: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}








### itemRendering

Triggers when the gauge item rendering.


{% highlight javascript %}

<script>

//itemRendering event for Digital gauge
  $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#gauge"), {
              itemRendering: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}







### load

Triggers when the gauge is start to load.


{% highlight javascript %}

<script>

//load event for Digital gauge
  $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#gauge"), {
              load: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}




### renderComplete

Triggers when the gauge render is completed.


{% highlight javascript %}

<script>

//renderComplete event for Digital gauge
  $(function () {
        var sample = new ej.datavisualization.DigitalGauge($("#gauge"), {
              renderComplete: function () {
                 //..//
                }
            });
        });
       
</script>

{% endhighlight %}











