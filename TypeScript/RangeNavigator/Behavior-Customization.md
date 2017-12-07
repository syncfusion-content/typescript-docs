---
layout: post
title: Behavior-Customization
description: Behavior Customization
platform: typescript
control: RangeNavigator
documentation: ug
---

### Behavior Customization

**RangeNavigator** allows you to customize the control using events. You can change the range for selected data of the **RangeNavigator** using events.

#### Deferred update

If you set **enableDeferredUpdate**to true, the **rangeChanged** event gets fired after dragging and dropping the slider. By default the **enableDeferredUpdate**is true. If **enableDeferredUpdate**is false then the **rangeChanged** event gets fired while dragging the slider.


{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

 $(function () {

var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
   //...
        enableDeferredUpdate: true,
   //...	
  });
 });
}

{% endhighlight %}


![](Behavior-Customization_images/Behavior-Customization_img1.png) 


#### Handle Events

**loaded:** function

This event is handled when the **RangeNavigator** gets loaded. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 

{% highlight javascript %}


    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
    // ...             
    loaded: function(sender) {
        sender.model.isResponsive = false;
    },
    //...
    });
    });


{% endhighlight %}


**rangeChanged**: function

This event gets fired whenever the selected range changes in **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.selectedRangeSettings, you can access the start and end value of range for the selected region. 

{% highlight javascript %}


   var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
    // ...             
    rangeChanged: function(sender) {
        console.log(sender.selectedRangeSettings.start);
    },
    // ...             
    });
    });


{% endhighlight %}

#### Use of ZoomCoordinates

**RangeNavigator** is used along with the controls like chart and grid to view the selected data. To update chart/grid, whenever the selected range changes in **RangeNavigator**, you can use **rangeChanged** event of **RangeNavigator** and then update the chart/grid with the selected data in this event. 

You can easily update the data for chart by assigning the **zoomFactor** and **zoomPosition** of the **RangeNavigator** to the chart axis.

{% highlight javascript %}


   var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
    // ...             
    rangeChanged: onChartLoaded
        // ...             
    });
    });
    // setting zoom factor and position for chart axis in rangeChanged event.
    function onChartLoaded(sender) {
        var chartObj = $("#container").data("ejChart");
        if (chartObj != null) {
            chartObj.model.axes[0].zoomPosition = sender.zoomPosition;
            chartObj.model.axes[0].zoomFactor = sender.zoomFactor;
        }
        $("#container").ejChart("redraw");
    }


{% endhighlight %}



![](Behavior-Customization_images/Behavior-Customization_img2.png) 

#### Thumb Template

You can customize Thumb template by using **leftThumbTemplate** and **rightThumbTemplate** property. You can add the required template as a "div" element with an "id" to the web page and assign the id or assign the HTML string to this property under **navigatorStyleSettings**.

{% highlight html %}

 
<script type="text/x-jsrender" id="left" >
           <svg height="24" width="32" style="fill:#DD4A4A;stroke:black;">
                <path d="M2 2 L2 22 L22 22 L32 12 L22 2 Z" />
           </svg>
</script>
<script type="text/x-jsrender" id="right">
           <svg height="24" width="32" style="fill:#DD4A4A;stroke:black; ">
               <path d="M2 12 L12 22 L32 22 L32 2 L12 2 Z" />
           </svg>
</script>
<script type="text/javascript" language="javascript">
           $(function () {
               var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
               // ...             
                    navigatorStyleSettings: {
                          leftThumbTemplate: 'left',
                          rightThumbTemplate: 'right',
                    },
               // ...   
             });
          });
</script>


{% endhighlight %}



The following screenshot displays the **RangeNavigator** using thumb template.

![](Behavior-Customization_images/Behavior-Customization_img3.png) 
