---
layout: post
title:  Stacked Headers
description: Stacked Headers
documentation: ug
platform: typescript
keywords: stacked headers,kanban stacked headers
---
# Stacked Headers

The stacked headers helps you to group the logical columns in Kanban. It can be shown by setting `showStackedHeader` as true and by defining [`stackedHeaderRows`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows).

## Adding Stacked header columns

To stack columns in stacked header, you need to define [`column`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows-stackedheadercolumns-column) property in [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows-stackedheadercolumns) with field names of visible columns.

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module KanbanComponent {
    $(function () {
       var data = new ej.DataManager(window.kanbanData).executeLocal(new ej.Query().take(20));
       var sample = new ej.Kanban($("#Kanban"), {
                        dataSource: data,
                        columns: [
                            { headerText: "Backlog", key: "Open" },
                            { headerText: "In Progress", key: "InProgress" },
                            { headerText: "Testing", key: "Testing" }
                        ],
                        keyField: "Status", 
                        fields: {
                        primaryKey: "Id",
                        content: "Summary",
                        },
                        stackedHeaderRows: [{
                        stackedHeaderColumns: [{
                            headerText: "Unresolved",
                            column: "Backlog,In Progress"
                        }, {
                            headerText: "Resolved",
                            column: "Testing,Done"
                        }]
                    }]

                });
         });
}


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Stacked_Headers_images/stacked_header_img1.png)