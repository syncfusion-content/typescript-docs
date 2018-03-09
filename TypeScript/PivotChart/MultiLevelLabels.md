---
layout: post
title: Multi-level Labels
description: multilevellabels
platform: Typescript
control: PivotChart
documentation: ug
---

# Multi-level labels

Multi-level labels allows you to drill down to access the detailed level of data or drill up to see the summarized data by using the expander present in the OLAP chart.

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotChart($("#PivotChart1"), { 
		enableMultiLevelLabels: true
	});
});

{% endhighlight %}


## Relational

![](MultiLevelLabels_images/relational.png)

## OLAP

![](MultiLevelLabels_images/olap.png)

