---
layout: post
title: Getting-Started
description: getting started
platform: Typescript
control: Gantt
documentation: ug
---

# Getting Started

This section explains briefly about how to create a Gantt chart in your application with TypeScript.

## Create your first Gantt in TypeScript

To get started Syncfusion TypeScript application refer [`this`](https://help.syncfusion.com/typescript/overview) page for basic control integration and script references.

In this tutorial, you can learn how to create a simple Gantt chart, add tasks or subtasks, and set relationship between tasks during the design phase of a software project. The following screenshot displays the desired output after completing this tutorial,

![](Getting-Started_images/Getting-Started_img4.png)

It is necessary to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (app.ts file), so that you will get the intelliSense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the jquery.d.ts file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

## Adding script references

Create an HTML file and add the following template to the HTML file.

To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file. So the complete boilerplate code is

{% highlight html %}

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">

    <head>

        <title>Getting Started with Gantt Control for Aurelia</title>

        <!-- style sheet for default theme(flat azure) -->
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

        <!--scripts-->
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js "></script>
    </head>

    <body>
        <!--Add  Gantt control here-->
    </body>

    </html>

{% endhighlight %}

## Initialize the Gantt 

Add a **&lt;div&gt;** element with in the &lt;Body&gt; tag.

{% highlight html %}

 <div class="cols-sample-area">
    <div id="GanttContainer"></div>
 </div>
 <script type="text/javascript" src="gantt/gantt.js"></script>

{% endhighlight %}

{% highlight javascript %}

    projectData = [
    {
        taskID:1,
        taskName: "Project Schedule",
        startDate: "02/03/2014",
        endDate: "03/07/2014",
        subtasks: [
            {
                taskID:2,
                taskName: "Planning",
                startDate: "02/03/2014",
                endDate: "02/07/2014"               
            },
            ]
            //...
    }
    ];

{% endhighlight %}

Initialize the Gantt with data source created in the last step.

{% highlight js %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            dataSource: projectData,
            taskIdMapping: "taskID",
            allowDragAndDrop: true,
            taskNameMapping: "taskName",
            startDateMapping: "startDate",
            progressMapping: "progress",
            durationMapping: "duration",
            endDateMapping: "endDate",
            childMapping: "subtasks"
                //...
        });
    });
}

{% endhighlight %}

A Gantt chart is created as shown in the following screen shot.

![](Getting-Started_images/Getting-Started_img5.png)

## Enable Toolbar

Gantt control contains toolbar options to edit, search, expand or collapse all records, indent, outdent, delete, and add a task. You can enable toolbar using the [`toolbarSettings`](http://help.syncfusion.com/js/api/ejgantt#members:toolbarsettings "toolbarSettings") property.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            toolbarSettings: {
                showToolbar: true,
                toolbarItems: ["add", "edit", "delete", "update", "cancel", "indent", "outdent", "expandAll", "collapseAll", "search"]
            },
            //...
        });
    });
}

{% endhighlight %}

The following screen shot displays a Tool bar in Gantt chart control:

![](Getting-Started_images/Getting-Started_img6.png)

N>  Add, edit, delete, indent and outdent options are enabled when enabling the allowEditing, allowAdding, allowDelete, allowIndent and allowOutdent properties in the edit Options.

## Enable Sorting

The Gantt control has sorting functionality to arrange the tasks in ascending or descending order based on a particular column.

### Multicolumn Sorting

Enable the multicolumn sorting in Gantt by setting [`allowMultiSorting`](http://help.syncfusion.com/js/api/ejgantt#members:allowmultisorting "allowMultiSorting") as `true`. You can sort multiple columns in Gantt, by selecting the desired column header while holding the `CTRL` key.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            allowSorting: true,
            allowMultiSorting: true
                //...
        });
    });
}

{% endhighlight %}

## Enable Editing

You can enable editing using [`editSettings`](http://help.syncfusion.com/js/api/ejgantt#members:editsettings "editSettings") and [`allowGanttChartEditing`](http://help.syncfusion.com/js/api/ejgantt#members:allowganttchartediting "allowGanttChartEditing") options.

### Cell Editing

Modify the task details through the grid cell editing by setting the [`editMode`](http://help.syncfusion.com/js/api/ejgantt#members:editsettings-editmode "editSettings.editMode") as [`cellEditing`](http://help.syncfusion.com/js/api/ejgantt#members:editsettings-editmode "cellEditing").

### Normal Editing

Modify the task details through the edit dialog by setting the [`editMode`](http://help.syncfusion.com/js/api/ejgantt#members:editsettings-editmode "editSettings.editMode") as [`normal`](http://help.syncfusion.com/js/api/ejgantt#members:editsettings-editmode "normal").

### Taskbar Editing

Modify the task details through user interaction such as resizing and dragging the taskbar.

### Predecessor Editing

Modify the predecessor details of a task using mouse interactions by setting [`allowGanttChartEditing`](http://help.syncfusion.com/js/api/ejgantt#members:allowganttchartediting "allowGanttChartEditing") as `true` and setting the value for `predecessorMapping` property.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            allowGanttChartEditing: true,
            predecessorsMapping: "predecessor",
            editSettings: {
                allowEditing: true,
                allowAdding: true,
                allowDeleting: true,
                allowIndent: true,
                editMode: "cellEditing"
            },
            //...
        });
    });
}

{% endhighlight %}

The following screen shot displays a Gantt chart control with Enable Editing options.

![](Getting-Started_images/Getting-Started_img7.png)

N>  Both cellEditing and  normal  editing operations are performed through double-click action.

## Enable Context Menu

You can enable the context menu in Gantt, by setting the [`enableContextMenu`](http://help.syncfusion.com/js/api/ejgantt#members:enablecontextmenu "enableContextMenu") as `true`.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            enableContextMenu: true,

            //...
        });
    });
}

{% endhighlight %}

The following screen shot displays Gantt chart in which Context menu option is enabled:

![](Getting-Started_images/Getting-Started_img8.png)

## Enable Column Menu

You can enable the column menu in Gantt, by setting the [`showColumnChooser`](http://help.syncfusion.com/js/api/ejgantt#members:showcolumnchooser "showColumnChooser") as `true`.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            showColumnChooser: true,

            //...
        });
    });
}

{% endhighlight %}

The following screen shot displays Gantt chart in which column chooser option is enabled:

![](Getting-Started_images/Getting-Started_img11.png)

## Provide tasks relationship

In Gantt, you have the predecessor support to show the relationship between two different tasks.

* **Start to Start (SS)** - You cannot start a task until the other task also starts.
* **Start to Finish (SF)** - You cannot finish a task until the other task finishes.
* **Finish to Start (FS)** - You cannot start a task until the other task completes.
* **Finish to Finish (FF)** - You cannot finish a task until the other task completes.

You can show the relationship in tasks, by using the [`predecessorMapping`](http://help.syncfusion.com/js/api/ejgantt#members:predecessormapping "predecessorsMapping")

, as shown in the following code example.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            predecessorsMapping: "predecessor",

            //...
        });
    });
}


{% endhighlight %}

The following screenshot displays the relationship between tasks.

![](Getting-Started_images/Getting-Started_img9.png)

## Provide Resources

In Gantt control, you can display and assign the resource for each task. Create a collection of `JSON` object, which contains id and name of the resource and assign it to [`resources`](http://help.syncfusion.com/js/api/ejgantt#members:resources "resources") property. Then, specify the field name for id and name of the resource in the resource collection to [`resourceIdMapping`](http://help.syncfusion.com/js/api/ejgantt#members:resourceidmapping "resourceIdMapping") and [`resourceNameMapping`](http://help.syncfusion.com/js/api/ejgantt#members:resourcenamemapping "resourceNameMapping") options. The name of the field, which contains the actual resources assigned for a particular task in the `dataSource` is specified using [`resourceInfoMapping`](http://help.syncfusion.com/js/api/ejgantt#members:resourceinfomapping "resourceInfoMapping").

1.Create the resource collection to be displayed in ejGantt

{% highlight javascript %}

projectResources =[{
        resourceId: 1,
        resourceName: "Project Manager"
    },{
        resourceId: 2,
        resourceName: "Software Analyst"
    },{
        resourceId: 3,
        resourceName: "Developer"
    },{
        resourceId: 4,
        resourceName: "Testing Engineer"
    }];

{% endhighlight %}

2.Initialize the Gantt with resources created in last step. 

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            resourceInfoMapping: "resourceId",
            resourceNameMapping: "resourceName",
            resourceIdMapping: "resourceId",
            resources: projectResources,
            //...
        });
    });
}

{% endhighlight %}

The following screenshot displays resource allocation for tasks in Gantt chart.

![](Getting-Started_images/Getting-Started_img10.png)

By following these steps, you have learned how to provide data source to Gantt chart, how to configure Gantt to set task relationships, assign resources for each task, and add toolbar with necessary buttons.

## Highlight Weekend

In Gantt, you can on or off weekends high lighting by setting the [`highlightWeekends`](/api/js/ejgantt#members:highlightweekends "highlightWeekends")

 as `true` or `false`.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />
module GanttComponent {
    $(function() {
        var ganttInstance = new ej.Gantt($("#GanttContainer"), {
            highlightWeekends = false
            //...
        });
    });
}

{% endhighlight %}

The following screen shot displays Gantt chart in which highlight weekends is disabled:

![](Getting-Started_images/Getting-Started_img12.png)
