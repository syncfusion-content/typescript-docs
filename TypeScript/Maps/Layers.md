---
layout: post
title: Layers
description: layers
platform: typescript
control: Maps
documentation: ug
---

# Layers

Map is maintained through `layers` and it can accommodate one or more layers.

## Multilayer

The Multilayer support allows you to load multiple shape files in a single container, enabling maps to display more information.

### Adding Multiple Layers in the Map

The shape layers is the core layer of the map. The multiple layers can be added in the shape layers as `subLayers` within the shape layers.

## SubLayer

The subLayer is the collection of shape layers. 

In this example, World Map shape is used as shape data by utilizing the “**WorldMap.json**” file in the following folder structure obtained from downloaded Maps_GeoJSON folder.

..\ Maps_GeoJSON\

You can assign the complete contents in “**WorldMap.json**” file to new JSON object. For better understanding, a JS file “**WorldMap.js”** is already created to store JSON data in JSON object “usMap”

**[usa.js]**

{% highlight javascript %}

    var world_map = //Paste all the content copied from the JSON file// 

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module MapComponenet {

    $(function () {
        var mapSample = new ej.datavisualization.Map($("#map"), {
            layers: [
            {
                shapeData: world_map,
                shapeSettings: {
                    fill: "#9CBF4E",
                    strokeThickness: "0.5",
                    stroke: "White"
                },
                subLayers: [{
                    shapeData: usMap,
                    shapeSettings: {
                        fill: "orange",
                        strokeThickness: "1",
                        stroke: "White"
                    }
                }]
            }]
        });
    }); 
}

{% endhighlight %}


![](Layers_images/Layers_img1.png)



