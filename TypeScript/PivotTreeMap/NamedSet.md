---
layout: post
title: Named Set
description: named set
platform: Typescript
control: PivotTreeMap
documentation: ug
---

# Named Sets

Named Sets is a multidimensional expression (MDX) that returns a set of dimension members, which can be created by combining cube data, arithmetic operators, numbers, and functions.

You can bind the Named Sets in PivotTreeMap by setting it's unique name in the `fieldName` property either in row or column axis and `isNamedSets` Boolean property to "true".

{% highlight html %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

$(function () {
    var sample = new ej.PivotTreeMap($("#PivotTreeMap1"), {
        dataSource: {
            data: "http://bi.syncfusion.com/olap/msmdpump.dll;Locale Identifier=1033;",
            catalog: "Adventure Works DW 2008 SE",
            cube: "Adventure Works",
            rows: [
                {
                    fieldName: "[Core Product Group]",
                    isNamedSets: true
                }
            ],
            columns: [
                {
                    fieldName: "[Customer].[Customer Geography]"
                }
            ],
            values: [
                {
                    measures: [
                        {
                            fieldName: "[Measures].[Customer Count]",
                        }
                    ],
                    axis: "columns"
                }
            ],
            filters: []
        }
    });
});


{% endhighlight %}

![](NamedSets_images/namedset.png)