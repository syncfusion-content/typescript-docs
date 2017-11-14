---
layout: post
title:  Drag and Drop
description: Drag and Drop
documentation: ug
platform: typescript
keywords: drag and drop,kanban drag and drop
---

# Drag and Drop

By default [`allowDragAndDrop`](https://help.syncfusion.com/api/js/ejkanban#members:allowdraganddrop) is true.Cards can be transited from one column to another column, by dragging and dropping. And it has drop position indicator which enables easier positioning of cards

N> To transit cards to other swim lanes through Drag and Drop, please refer [here](https://help.syncfusion.com/js/kanban/swimlanes#drag-and-drop-between-swim-lanes).

## Prioritization of cards

Prioritizing cards is easy with drag-and-drop re-ordering that helps you to categorize most important work at the top.Cards can be categorized with priority by mapping specific database field into [`priority`](https://help.syncfusion.com/api/js/ejkanban#members:fields-priority) property.

`RankId` defined in the dataSource which is consist priority of cards. The `RankId` will be changed while card ordering changes through `Drag and Drop` and `Editing`.

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
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                    primaryKey: "Id",
                    priority: "RankId"
                }
        });
    });
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Drag_and_Drop_images/drag_and_drop_img1.png)

N> For Drag and Drop event handling , please refer this [API](https://help.syncfusion.com/api/js/ejkanban#events:carddrag).
