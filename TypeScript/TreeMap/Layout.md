---
layout: post
title: Layout
description: layout
platform: typescript
control: TreeMap
documentation: ug
---

# Layout

You can decide on the visual representation of nodes belonging to all the treemap levels using the `itemsLayoutMode` property of the TreeMap.

There are four different **TreeMap** layouts such as

* Squarified
* SliceAndDiceAuto
* SliceAndDiceHorizontal
* SliceAndDiceVertical

## Squarified

**Squarified** layout creates rectangles with best aspect ratio.

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
                  { groupPath: "Continent", groupGap: 5 }
                ],
                itemsLayoutMode:"squarified"
            });
        });
}

{% endhighlight %}



![](Layout_images/Layout_img1.png)

Try it: [Squarified](http://jsplayground.syncfusion.com/q1pc13k3)

## SliceAndDiceAuto

**SliceAndDiceAuto** layout creates rectangles with high aspect ratio and displays them sorted both horizontally and vertically.

{% highlight javascript %}


       $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...             
                itemsLayoutMode:"sliceanddiceauto",
                // ...             
            });
        });


{% endhighlight %}



![](Layout_images/Layout_img2.png)

Try it: [SliceAndDiceAuto](http://jsplayground.syncfusion.com/eotkjoag)

## SliceAndDiceHorizontal

**SliceAndDiceHorizontal** layout creates rectangles with high aspect ratio and displays them sorted horizontally.

{% highlight javascript %}

       $(function () {

          var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...   
                itemsLayoutMode:"sliceanddicehorizontal",
                // ...   
            });
        });



{% endhighlight %}



![](Layout_images/Layout_img3.png)

Try it: [SliceAndDiceHorizontal](http://jsplayground.syncfusion.com/hrvachsi)

## SliceAndDiceVertical

**SliceAndDiceVertical** layout creates rectangles with high aspect ratio and displays them sorted vertical.

{% highlight javascript %}

        $(function () {

          var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...   
                itemsLayoutMode:"sliceanddicevertical",
                // ...   
            });
        });



{% endhighlight %}



![](Layout_images/Layout_img4.png)

Try it: [SliceAndDiceVertical](http://jsplayground.syncfusion.com/brtks3m2)
