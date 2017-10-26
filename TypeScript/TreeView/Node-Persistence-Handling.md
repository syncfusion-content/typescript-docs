---
layout: post
title: State-Persistence
description: State Persistence
platform: typescript
control: TreeView
documentation: ug
---

# State Persistence

TreeView state can be persisted by using [enablePersistence](https://help.syncfusion.com/api/js/ejtreeview#members:enablepersistence). In which entire modal has been persisted excluding data source in order to maintain performance. 

The model values of below are maintained through Id basis of tree node.

* **selected**
* **checked**
* **expanded/collapsed state**

N>  "Ul-li" template option, state has been persisted by index.

TreeView stores its model in local storage / cookies of browser before page refreshes and reinitialized with their stored model after refresh.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
 
module TreeViewComponent {

        var localData = [

        { id: 1, text: "Item 1" },

        { id: 2, text: "Item 2" },

        { id: 3, text: "Item 3" },

        { id: 4, text: "Item 4" },

        { id: 5, parent: 1, text: "Item 1.1" },

        { id: 6, parent: 1, text: "Item 1.2" },

        { id: 7, parent: 1, text: "Item 1.3" },

        { id: 8, parent: 3, text: "Item 3.1" },

        { id: 9, parent: 3, text: "Item 3.2" },

        { id: 10, parent: 5, text: "Item 1.1.1" }

        ];

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                enablePersistence: true,

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });
}

{% endhighlight %}

