---
layout: post
title: Levels
description: Learn how to customize various levels in SunburstChart
platform: ts
control: SunburstChart
documentation: ug
---

## Levels

Sunburst chart is used to display hierarchical data. You can add more than one hierarchical data by using the `levels` property of Sunburst chart. Each level of the hierarchy is represented by circle.
The following code snippet illustrates 

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
         levels: [
			{
                //... to represent the hierarchical data in different levels 
                   }
            ],  	
            // ...
        });
    });
}
       
{% endhighlight %}

## GroupMemberPath

It is the string property that is used to map the group category value in the dataSource .
You can define the levels as shown in the below code example

{% highlight javascript %}

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
         levels: [
			{ groupMemberPath: "Level 1" },
            { groupMemberPath: "Level 2" },
            { groupMemberPath: "Level 3" },
            ], 	
            // ...
        });
    });  
  
     
{% endhighlight %}

The following screenshot illustrates the Sunburst Chart with different levels



![](Levels_images/Levels_img1.png)
