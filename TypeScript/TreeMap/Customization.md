---
layout: post
title: Customization
description: customization
platform: typescript
control: TreeMap
documentation: ug
---

# Customization

**TreeMap** control supports color customization to determine the exact combination of colors for tree nodes displayed in **TreeMap** and tooltip support to display additional information of treemap data.

## Color

You can customize the colors of the leaf nodes of **TreeMap** using the ColorMapping support of the **TreeMap**. 

ColorMapping is categorized into three different types such as,

* `uniColorMapping`
* `rangeColorMapping`
* `desaturationColorMapping`

### Uni Color Mapping

You can color, all the leaf nodes with the same color by setting the `color` value of the `uniColorMapping` property of the **TreeMap**.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module treeMapcomponent {
    

       $(function () {

            var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...   
                uniColorMapping: {
                    color: "Crimson"
                },         
                // ...   
            });
        });

}

{% endhighlight %}



![](Customization_images/Customization_img1.png)

Try it: [UniColorMapping](http://jsplayground.syncfusion.com/2v542ver)

### Range Color Mapping

You can group the leaf nodes based on the range of the data’s color values. You can set a unique color for every ranges. To achieve this, specify the `to` and `from` values as range bound and `color` or `gradient colors` values to fill the leaf nodes of the particular range, through the `range color mapping` property of the **TreeMap**.

{% highlight javascript %}

        $(function () {

            var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...   
                rangeColorMapping: [
                        { color: "#77D8D8", from: "0", to: "1" },
                        { color: "#AED960", from: "0", to: "2" },
                        { color: "#FFAF51", from: "0", to: "3" },
                        { color: "#F3D240", from: "0", to: "4" }
                ],
                // ...   
            });
        });



{% endhighlight %}



![](Customization_images/Customization_img2.png)

Try it: [RangeColorMapping](http://jsplayground.syncfusion.com/cbcyugjn)

### Desaturation Color Mapping

You can differentiate all the leaf nodes using the `desaturation color mapping` property of the **TreeMap**. Differentiation is achieved, even though same color is applied for all the leaf nodes by varying the opacity of the leaf nodes based on the color value specified in the color value range using `rangeMinimum` and `rangeMaximum` value of the data collection. You can also bound the opacity range by setting `from` and `to` property of the `desaturationColorMapping`.

{% highlight javascript %}


        $(function () {

           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                // ...  
                desaturationColorMapping: {
                        color: "DeepSkyBlue", from: "1", to: "0.2", rangeMinimum: "0",  
                        rangeMaximum: "4"                        
                },
                // ...  
            });
        });


{% endhighlight %}



![](Customization_images/Customization_img3.png)

Try it: [DesaturationColorMapping](http://jsplayground.syncfusion.com/qoh2upwr)

## Tooltip

You can enable the tooltip support for the TreeMap by setting the `showTooltip` property to true. By default, it takes the property of the bound object that is referred to in the groupPath and displays its content when the corresponding node is tapped. The `tooltipTemplate` is a **HTML** element that is used to expose the custom template for the tooltip.

## Leaf Item Setting

You can customize the **Leaf level TreeMap items** using `leafItemSettings`. In `leftItemSettings` following customization options are available.

* You can specify the border color using `border brush` property.

* For customizing border thickness, you can use `border thickness` property.

* To customize the gap between the leaf items, you can use `gap` property.

* You can specify the label template for the leaf item using `item template` property.

* The Label and tooltip values take the property of bound object that is referred in the `labelPath` when defined.

* You can specify the position of the leaf labels using `labelPosition` property.

* You can control the mode of label visibility of the labels using `labelVisibilityMode` property.

* To show or hide the visibility of the leaf item labels you can use `showLabels` property.

* For specifying over flow action of left item labels you can use `textOverflow` property.

{% highlight javascript %}

    <script type="text/javascript">
        $(function () {
           var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
                dataSource: population_data,
                colorValuePath: "Growth",
                weightValuePath: "Population",
                rangeColorMapping: [
                        { color: "#77D8D8", from: "0", to: "1" },
                        { color: "#AED960", from: "0", to: "2" },
                        { color: "#FFAF51", from: "0", to: "3" },
                        { color: "#F3D240", from: "0", to: "4" }
                ],                   
                levels: [
                  { groupPath: "Continent", groupGap: 5}
                ],

                leafItemSettings: { labelPath: "Region" },
                showTooltip:true,
                tooltipTemplate:'template' 
            });
        });
    </script>
    
    <script  id="template" type="application/jsrender">
        <div  style="margin-left:17px;margin-top:-45px;">      
            <div style="height:auto;width:auto;background:black;border-radius:3px;opacity:0.6">
                <div style="margin-top:-20px;margin-left:9px;padding-top:3px;margin-right:9px;">
                    <label style="margin-top:-20px;font-weight:normal;font-size:12px;color:white;font-family:Segoe UI;">{{:Region}}</label>
                </div>
                <div style="height:10px;"></div>
                <div style="margin-top:-10px;margin-left:9px;margin-right:9px;padding-bottom:3px;">
                    <label style="margin-top:-10px;font-weight:normal;font-size:14px;color:white;font-family:segoe ui light;">{{:Population}}</label>
                </div>
            </div>
        </div>            
    </script>


{% endhighlight %}



![](Customization_images/Customization_img4.png)

Try it: [LeafItemSettings](http://jsplayground.syncfusion.com/gec0w4gb)

## Border Brush

You can able to customize the border color of the treemap using the property `borderBrush`. 

{% highlight javascript %}
 
//To set borderBrush API value during initialization 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {borderBrush:'white'});

{% endhighlight %}

## Border Thickness

For customizing the border thickness of the treemap, you can use the `borderThickness` property.

{% highlight javascript %}
 
//To set borderThickness API value during initialization 
  var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {borderThickness:1});

{% endhighlight %}

## Dock Position

You can position the legend at top, bottom, left and right side of the treemap as per your requirement. For changing the position as per your requirement, you can use `dockPosition` property.

<ts name="ej.datavisualization.TreeMap.DockPosition"/>
Specifies the dockPosition for legend

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">top</td>			
			<td class="description">specifies the top position</td>
		</tr>
		<tr>
			<td class="name">bottom</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">right</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">left</td>			
			<td class="description">specifies the left position</td>
		</tr>
	</tbody>
</table>

{% highlight javascript %}
 
//To set dockPosition API value during initialization 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {legendSettings:{ dockPosition: "top"}});

{% endhighlight %}

## Clicking and Dragging

You can select the single treemap element on click and drag. To click and drag treemap items, you have to enable the `draggingOnSelection` property.

{% highlight javascript %}
 
//To set draggingOnSelection API value during initialization 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {draggingOnSelection:false});
{% endhighlight %}

For selecting the group element of treemap while clicking and dragging, you can use `draggingGroupOnSelection` property.

{% highlight javascript %}
 
//To set draggingGroupOnSelectionAPI value during initialization 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {draggingGroupOnSelection:false});
{% endhighlight %}

## Fill with Gradient

You can customize that whether gradient color have to be applied for treemap or not. This can be customized using the property `enableGradient`.

{% highlight javascript %}
 
//To set enableGradient API value during initialization 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {enableGradient:true});

{% endhighlight %}

## Responsive Treemap

You can customize whether treemap have to be responsive or not while resizing the container. For making treemap responsive you can use `enableResize` or `isResponsive` property.

{% highlight javascript %}
 
//To set enableResize API value during initialization 
  var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {enableResize:false});

{% endhighlight %}

## GroupColorMapping

You can customize the color of the each group using `groupColorMapping` property. To use group color mapping, kindly specify `groupId` and `rangeColorMapping` inside the `groupColorMapping`. 

{% highlight javascript %}

//To set groupColorMapping API value during initialization 
  var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}]}] });

{% endhighlight %}

## GroupSelectionMode

You can specifies the selection mode of the treemap using `groupSelectionMode` property. You can set either group selection mode value as `Default` or  `Multiple`. 

{% highlight javascript %}

// Set the selection mode during initialization.                                        
          var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {groupSelectionMode:'default'});

{% endhighlight %}

## Header

You can specify the header for the parent item using the property `header`. This is applicable only for hierarchical data source. 

{% highlight javascript %}

//To set header API value during initialization 
  var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {header:"Country"});

{% endhighlight %}

## Specifying HierarchicalDatasource

You can specify whether data source bound for the treemap is hierarchical or not using the property `isHierarchicalDatasource`.

{% highlight javascript %}

//To set isHierarchicalDatasource API value during initialization 
  var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {isHierarchicalDatasource : true});

{% endhighlight %}

## Localization

You can specify the name of the culture based on which treemap is localized. To achieve this you can use the treemap property `locale`.

{% highlight javascript %}
         
   //Sets the locale value
   var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {
       locale="en-US"
       });   

{% endhighlight %}

## Treemap Items

You can specify the treemap items which you want to display in the treemap using the property `treeMapItems`.

{% highlight javascript %}

// Set the treeMapItems during initialization. 
 var treeMapSample = new ej.datavisualization.TreeMap($("#treeMap"), {treeMapItems:[]});
  
{% endhighlight %}

