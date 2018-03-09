---
layout: post
title: Legend
description: legend
platform: Typescript
control: PivotTreeMap
documentation: ug
---

#Legend

##Legend visibility

The legend shows the value range differences and color occurrence in the respective leaf node while hovering it with the cursor.

N> By default, the legend is visible in the pivot tree map.

![](Legend_images/Legend_img1.png)

You can disable the legend by setting the **showLegend** property to **false**. The following code example shows how to disable the legend:

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotTreeMap($("#PivotTreeMap1"), { 
        renderSuccess: function (args) {
            let treemapTarget = $('#PivotTreeMap1TreeMapContainer').data("ejTreeMap");
            treemapTarget.model.showLegend = false;
            treemapTarget.refresh();
        }
    });
});

{% endhighlight %}

![](Legend_images/Legend_img2.png)