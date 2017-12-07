---
layout: post
title: Custom-labels
description: custom labels
platform: typescript
control: Circular Gauge
documentation: ug
---

# Custom labels

Custom labels are the texts that you can use them in any location of the **Gauge**.

## Adding Custom Label Collection

Custom labels collection is directly added to the scale object. Refer the following code to add `customLabels` collection in a **Gauge** control.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module CircularGaugeComponent {

 $(function () {
        //For circular gauge rendering
         var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            scales: [{
                showCustomLabels: true,
                customLabels: [{
                    color: "Red"
                }]
            }]
        })
    });
}

{% endhighlight %}

**Basic Customization**

You can customize custom labels using the properties such as `textAngle`, `color` and `font`.  **textAngle** attribute is used to display the custom labels in the specified angles and **color** attribute is used to display the custom labels in specified color. 

You can use `value` attribute to set the text value in the custom labels. To display the custom labels, set `showCustomLabels` as ‘true’. To set the location of the custom label in **Circular Gauge**, `position` property is used. By using `x` and `y` axis you can adjust the position of the custom labels.

Font option is also available on  custom labels. The basic three properties of fonts such as size, family and style can be achieved by `size`, `fontStyle` and `fontFamily` attributes. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
        // For Circular Gauge rendering
         var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
            scales: [{
                size: 10,
                shadowOffset: 10,
                showCustomLabels: true,
                showRanges: true,
                showScaleBar: true,
                radius: 150, size: 2,
                customLabels: [{
                    //For setting custom label text angle
                textAngle: 10,
                    //For setting custom label color
                color: "Red",
                    //For setting custom label value
                value: "CustomLabel1",
                    //For setting custom label font option
                font: {
                size: "18px",
                fontFamily: "Arial",
                fontStyle: "bold"
                },
                    position: { x: 180, y: 100 }
                }]
            }]
        });
    });

{% endhighlight %}



Execute the above code to render the following output.

![](Custom-labels_images/Custom-labels_img1.png)

## Multiple Custom Labels

You can set multiple custom labels in a single **Circular Gauge** by adding an array of custom label objects. Refer the following code example for multiple custom label functionality.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
          // For Circular Gauge rendering
          var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
              scales: [{
                  size: 10,
                  shadowOffset: 10,
                  showCustomLabels: true,
                  showRanges: true,
                  showScaleBar: true,
                  radius: 150, size: 2,
                  customLabels: [
                  //custom label1
                  {
                      textAngle: 10,
                      color: "Red",
                      value: "CustomLabel1",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      position: { x: 180, y: 100 }
                  },
                  //custom label2
                  {
                      textAngle: 10,
                      color: "Green",
                      value: "CustomLabel2",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      position: { x: 180, y: 250 }
                  }]
              }]
          });
      });



{% endhighlight %}



Execute the above code to render the following output.

![](Custom-labels_images/Custom-labels_img2.png)

## Outer Custom Label

**Outer Custom Label** is used to show custom labels outside the **gauge** control. The **Outer Custom Label** can be positioned with API called `outerCustomLabelPosition`. The value for this API is enumerable type and its possible values are,

* Right

* Left

* Top

* Bottom

When a custom label is to be displayed as an **Outer Custom Label**, set the API `positionType` as Outer. Refer to the following code example to get the **Outer Custom Label**.


{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
            var circularGaugeSample = new ej.datavisualization.CircularGauge($("#CircularGauge1"),{
              // Sets outer custom label position.
              outerCustomLabelPosition: "right",
              //Defines the tooltip object.
              tooltip: {
                  // Enables the custom label tooltip.
                  showCustomLabelTooltip: true,
              },
              // Customizes the scale options.
              scales: [{
                  showLabels: true,
                  radius: 150,
                  // Customizes the custom label options.
                  customLabels: [{
                      value: "Average Speed",
                      position: { x: 360, y: 30 },
                      color: "Red",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      positionType: "outer",
                  }],
                  // Customizes the pointers options.
                  pointers: [{
                      value: 60,
                      length: 100,
                  }]
              }]
          });
      });




{% endhighlight %}



Execute the above code to render the following output.

![](Custom-labels_images/Custom-labels_img3.png)

