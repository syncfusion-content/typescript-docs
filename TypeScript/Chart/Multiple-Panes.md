---
layout: post
title: Render Chart in multiple layouts
description: Learn how to split chart area into multiple plot areas and render different types of series in each area.                    
platform: typescript
control: Chart
documentation: ug
---

# Multiple panes

Chart area can be divided into multiple panes using the [`rowDefinitions`](../api/js/ejchart#members:rowdefinitions) and [`columnDefinitions`](../api/js/ejchart#members:columndefinitions) properties.

### Row Definitions

To split the chart area vertically into a number of rows, use [`rowDefinitions`](../api/js/ejchart#members:rowdefinitions) of the chart. 

* You can allocate space for each row by using the [`unit`](../api/js/ejchart#members:rowdefinitions-unit) option that determines whether the chart area should be split by *percentage* or *pixels* for the given [`rowHeight`](../api/js/ejchart#members:rowdefinitions-rowheight) value of the rowDefinitions.
 
* To associate a vertical axis to a row, specify the rowDefinitions **index** value to the [`rowIndex`](../api/js/ejchart#members:primaryyaxis-rowindex) property of the chart axis.

* To customize each row’s horizontal line, use [`lineColor`](../api/js/ejchart#members:rowdefinitions-linecolor) and [`lineWidth`](../api/js/ejchart#members:rowdefinitions-linewidth) property.


{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                    
               //  Splitting chart area into multiple rows
                rowDefinitions: [{
                    //  Split first row of the chart area
                    unit : 'percentage',                 
                    lineColor : 'Gray',
                    rowHeight : 50,
                    linewidth : 0
                }, {
                    //  Split second row of the chart area
                    unit : 'percentage',                 
                    lineColor : 'green',
                    rowHeight : 50,
                    linewidth : 0
                }],

                axes: [{
                          //Create secondary axis and bind it to second row of chart area
                           name: "yAxis1",
                           rowIndex: 1
                    }],   
               series: [{

                         //Binding vertical axis name
                         yAxisName: "yAxis1",
                         // ...
                }],        
            //  ...

        });
    });
}


{% endhighlight %}

![](Multiple-Panes_images/Multiple-Panes_img1.png)


**Row Span**

For spanning the vertical axis along multiple panes vertically, you can use [`rowSpan`](../api/js/ejchart#members:primaryyaxis-rowspan) property of axis. 

{% highlight javascript %}


       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                    
            rowDefinitions: [{

                         // ...
                  },{

                         // ...
                  }],
                   axes: [{

                          // ...
                    }],

                primaryYAxis: {
                    //  Span the PrimaryYAxis                    
                    rowSpan : 2,
                }, 

               series: [{
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

![](Multiple-Panes_images/Multiple-Panes_img2.png)

## Column Definitions

To split the chart area horizontally into a number of columns, use [`columnDefinitions`](../api/js/ejchart#members:columndefinitions) of the chart.

* You can allocate space for each column by using the [`unit`](../api/js/ejchart#members:columndefinitions-unit) option that determines whether the chart area should be split by *percentage* or *pixels* for the given [`columnWidth`](../api/js/ejchart#members:columndefinitions-columnwidth) value of the columnDefinitions.
 
* To associate a horizontal axis to a column, specify the columnDefinitions **index** value to the [`columnIndex`](../api/js/ejchart#members:primaryxaxis-columnspan) property of the chart axis.
 
{% highlight javascript %}

 
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                    
               //  Splitting chart area into multiple columns
                columnDefinitions: [{
                    //  Split first column of the chart area
                    unit : 'percentage', 
                    columnWidth : 50,
                }, {
                    //  Split second column of the chart area
                    unit : 'percentage',                 
                    columnWidth : 50,
                }],

                axes: [{
                          //Create secondary axis and bind it to second column of chart area 
                           name: "xAxis1",
                           columnIndex: 1
                    }],   
               series: [{

                         //Binding horizontal axis name
                         xAxisName: "xAxis1",
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

![](Multiple-Panes_images/Multiple-Panes_img3.png)


**Column Span**

For spanning the horizontal axis along multiple panes horizontally, you can use [`columnSpan`](../api/js/ejchart#members:primaryxaxis-columnspan) property of axis. 

{% highlight javascript %}

 
       var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                    
               columnDefinitions: [{

                          // ...
                  },{

                          // ...
                  }],
                   axes: [{

                          // ...
                    }],

                primaryXAxis: {
                    //  Span the PrimaryXAxis                    
                    columnSpan : 2,
                }, 

               series: [{
                         // ...
                }],        
            //  ...

        });


{% endhighlight %}

![](Multiple-Panes_images/Multiple-Panes_img4.png)
