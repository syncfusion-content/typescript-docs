---
layout: post
title: TreeMapLevels
description: treemaplevels
platform: typescript
control: TreeMap
documentation: ug
---

# TreeMapLevels

The `levels` of **TreeMap** can be categorized into two types as,

* FlatLevel
* Hierarchical Level

Following customization options are available to customize the treemap level as per your requirements.

* To specify the background color for the group, you can use `groupBackground` property.

* To specify the border color for the group, you can use `groupBorderColor` property.

* To maintain the border thickness for the group, you can use `groupBorderThickness` property.

* You can specify the gaps between groups using `groupGap` property.

* You can specify the padding using `groupPadding` property.

* For specifying the header height, you can use `headerHeight` property.

* You can customize the header template using `headerTemplate` property.

* To specify the label position, you can use `labelPosition` property.

* To specify the label template for treemap, you can use `labelTemplate` property.

* You can specify the label visibility using `labelVisibilityMode` property.

* You can control the label visibility using `showLabels` property.

* For controlling text overflow, you can use `textOverflow` property.

## Flat Level

### GroupPath

You can use `groupPath` property for every flat level of the **TreeMap** control. It is a path to a field on the source object that serves as the **“Group”** for the level specified. You can group the data based on the `groupPath` in the **TreeMap** control. When the `groupPath` is not specified, then the items are not grouped and the data is displayed in the order specified in the `dataSource`.

### GroupGap

You can use `groupGap` property to separate the items from every flat level and to differentiate the levels mentioned in the **TreeMap** control.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module treeMapcomponent {

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                dataSource: population_data,
                colorValuePath: "Growth",
                weightValuePath: "Population",
                levels: [
                     { groupPath: "Continent", groupGap: 5}              
                ]

            });
        });

}

{% endhighlight %}



![](TreeMapLevels_images/TreeMapLevels_img1.png)

Try it: [FlatLevel](http://jsplayground.syncfusion.com/plnqu1fu)

## Hierarchical Level

**TreeMap** Hierarchical level is used to define levels for hierarchical data collection that contains tree-structured data.

{% highlight javascript %}

        $(function ($) {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                dataSource: population_data,
                weightValuePath: "Population",
            });
        });

        var population_data =  [
            {Asia:[
            {Region: "Southern Asia", Growth: 1.32, Population: 1749046000 },
            {Region: "Eastern Asia", Growth: 0.57, Population: 1620807000 },
            {Region: "South-Eastern Asia", Growth: 1.20, Population: 618793000 },
            {Region: "Western Asia", Growth: 1.98, Population: 245707000 },
            {Region: "Central Asia", Growth: 1.43, Population: 64370000 }
            ] } ,
            {America:[
            {Region: "South America", Growth: 1.06, Population: 406740000 },
            {Region: "Northern America", Growth: 0.85, Population: 355361000 },
            {Region: "Central America", Growth: 1.40, Population: 167387000 },
            ]},
            {Africa:[
            {Region: "Eastern Africa", Growth: 2.89, Population: 373202000 },
            {Region: "Western Africa", Growth: 2.78, Population: 331255000 },
            {Region: "Northern Africa", Growth: 1.70, Population: 210002000 },
            {Region: "Middle Africa", Growth: 2.79, Population: 135750000 },
            {Region: "Southern Africa", Growth: 0.91, Population: 60425000 }
            ]}
        ];



{% endhighlight %}



![](TreeMapLevels_images/TreeMapLevels_img2.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/treemap/hierarchical) here to view our online demo sample with Hierarchical levels.
