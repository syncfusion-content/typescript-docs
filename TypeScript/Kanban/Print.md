---
layout: post
title:  Print with Kanban widget for Syncfusion Essential JS
description: How to enable print option in Kanban
documentation: ug
platform: typescript
---

# Print

 Set [‘allowPrinting’](https://help.syncfusion.com/api/js/ejkanban#members:allowprinting) as true, to enable Print icon in the Kanban toolbar.  You can use [‘print()’](https://help.syncfusion.com/api/js/ejkanban#methods:print) method from Kanban instance to print the Kanban.

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
            allowTitle: true,
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            allowPrinting: true,
        });
    });
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Printing_images/print_img1.png)


