---
layout: post
title: User Interaction
description: user interaction
platform: typescript
control: TreeMap
documentation: ug

---

# User Interaction

Users can interact with the **TreeMap** control by selecting either the leaf nodes or the groups.

## Selection

Selection support enables you to highlight the items on which the mouse tapping has occurred. You can select the following contents of the **TreeMap** control:

* Leaf Nodes
* Group

### Single Selection

To enable the selection of the leaf nodes, the `highlight on selection` property in `treemap` is set as **true**. When the selection occurs, the item is highlighted with a bounding rectangle around the selected leaf node.
The border can be customized with the `highlight border brush` and `highlight border thickness` properties.


{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module treeMapcomponent {

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                highlightOnSelection : true,
                highlightBorderBrush : "#3e3e3e",
                highlightBorderThickness : 1
                // ...                
            });
        });
}
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img1.png)        


### Group Selection

To enable the selection of leaf nodes, the `highlight group on selection` property in `treemap` is set as **true**. When the selection occurs, bounding rectangle highlights the selected group. The border can be customized with the `highlight group border brush` and `highlight group border thickness` properties.

{% highlight javascript %}

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                highlightGroupOnSelection : true,
                highlightBorderBrush : "#3e3e3e",
                highlightBorderThickness : 1
                // ...                
            });
        });
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img3.png)  
        

## MultiSelection

This feature enables you to select multiple leaf nodes or groups simultaneously. To enable this feature for leaf nodes, set `selectionMode` as "**multiple**" and for groups, set `group selection mode` as "**multiple**"
To select multiple items simultaneously, the mouse tap should be done along with a continuous press of the "**Control**" key.  

##### Selection (Multiple)

{% highlight javascript %}

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                highlightOnSelection : true,
                selectionMode: "multiple",
                // ...                
            });
        });
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img2.png) 


#### Group Selection (Multiple)

{% highlight javascript %}

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                highlightGroupOnSelection : true,
                groupSelectionMode: "multiple",
                // ...                
            });
        });
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img4.png)


## Drag On Selection

This feature enables you to highlight/select the leaf nodes or groups by the dragging the mouse pointer over the **TreeMap** items.

### Dragging On Selection

To enable this feature, set the `draggingOnSelection` to "**true**".

{% highlight javascript %}

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                draggingOnSelection : true,
                // ...                
            });
        });
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img5.png)

### Dragging Group On Selection

To enable this feature, set the `draggingGroupOnSelection` to "**true**".

{% highlight javascript %}

        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...
                draggingGroupOnSelection : true,
                // ...                
            });
        });
        
{% endhighlight %}

![](User-Interaction_images/User-Interaction_img6.png)