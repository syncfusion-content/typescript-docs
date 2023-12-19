---
layout: post
title: Layout support in TypeScript TreeMap Control | Syncfusion
description: Learn here all about layout support in Syncfusion Essential TypeScript TreeMap Control, its elements, and more.
platform: typescript
control: TreeMap
documentation: ug
---

# Layout support in TypeScript TreeMap

You can decide on the visual representation of nodes belonging to all the [JavaScript TreeMap](https://www.syncfusion.com/javascript-ui-controls/js-treemap) levels using the `itemsLayoutMode` property of the TreeMap.

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



![TypeScript TreeMap Squarified](Layout_images/Layout_img1.png)

Try it: [Squarified](https://jsplayground.syncfusion.com/q1pc13k3)

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



![TypeScript TreeMap SliceAndDiceAuto](Layout_images/Layout_img2.png)

Try it: [SliceAndDiceAuto](https://jsplayground.syncfusion.com/eotkjoag)

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



![TypeScript TreeMap SliceAndDiceHorizontal](Layout_images/Layout_img3.png)

Try it: [SliceAndDiceHorizontal](https://jsplayground.syncfusion.com/hrvachsi)

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



![TypeScript TreeMap SliceAndDiceVertical](Layout_images/Layout_img4.png)

Try it: [SliceAndDiceVertical](https://jsplayground.syncfusion.com/brtks3m2)
