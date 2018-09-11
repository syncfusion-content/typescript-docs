---
layout: post
title: Drag-and-Drop
description: drag and drop
platform: Typescript
control: TreeView
documentation: ug
---

# Drag and drop 

To perform drag and drop operation in TreeView, specify [allowDragAndDrop](https://help.syncfusion.com/api/js/ejtreeview#members:allowdraganddrop) as true. It allows you to drag and drop node in all level of same TreeView.

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
        var tree = new ej.TreeView($("#treeView"), {

                allowDragAndDrop: true,

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });
 }

{% endhighlight %}

N> TreeView provides much easier option to drop the dragged nodes at any levels by indicator lines with icons.

## Position Indicators

TreeView provides much easier option to drop the dragged nodes at any levels by indicator lines with icons such as line, plus/minus and restrict icons while dragging and dropping the nodes. It represents exact position where the node to be dropped as sibling or child. Refer below screen shot of position indicator.

<table>
<tr>
<th>
Indicators</th><th>
description</th></tr>
<tr>
<td>
Plus icon<br/><br/></td><td>
represents the dragged node to be added as child of targeted node<br/><br/></td></tr>
<tr>
<td>
Minus with restrict icon<br/><br/></td><td>
represents the dragged node not to be dropped at the hovered region<br/><br/></td></tr>
<tr>
<td>
In between icon<br/><br/></td><td>
represents the dragged node to be dropped in between the nodes as siblings<br/><br/></td></tr>
</table>

## Restriction

You can restrict the dragged nodes to be dropped at siblings or children’s level by using [allowDropSibling](https://help.syncfusion.com/api/js/ejtreeview#members:allowdropsibling) and [allowDropChild](https://help.syncfusion.com/api/js/ejtreeview#members:allowdropchild) property.

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
        var tree = new ej.TreeView($("#treeView"), {

                allowDragAndDrop: true,

                allowDropSibling: true, // allows to drop sibling

                allowDropChild: false, // restricts to drop as child

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });
      }

{% endhighlight %}

## Drag and Drop between Trees

You can drag and drop tree nodes between two TreeView by setting [allowDragAndDrop]You can drag and drop tree nodes between two TreeView by setting [allowDragAndDrop](https://help.syncfusion.com/api/js/ejtreeview#members:allowdraganddrop) as true along with [allowDragAndDropAcrossControl](https://help.syncfusion.com/api/js/ejtreeview#members:allowdraganddropacrosscontrol) as true.
The [nodeDrag](https://help.syncfusion.com/api/js/ejtreeview#events:nodedrag), [nodeDragStart](https://help.syncfusion.com/api/js/ejtreeview#events:nodedragstart), [nodeDragStop](https://help.syncfusion.com/api/js/ejtreeview#events:nodedragstop) and 
[nodeDropped](https://help.syncfusion.com/api/js/ejtreeview#events:nodedropped) event occurs based on Treeview node drag and drop state. 

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

        var tree1 = [

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

        var tree2 = [

        { id: 11, text: "Item 5" },

        { id: 12, text: "Item 6" },

        { id: 13, text: "Item 7" },

        { id: 14, text: "Item 4" },

        { id: 15, parent: 11, text: "Item 5.1" },

        { id: 16, parent: 11, text: "Item 5.2" },

        { id: 17, parent: 11, text: "Item 5.3" },

        { id: 18, parent: 13, text: "Item 7.1" },

        { id: 19, parent: 13, text: "Item 7.2" },

        { id: 10, parent: 15, text: "Item 5.1.1" }

        ];

    $(function () {
        var tree = new ej.TreeView($("#treeViewDrag"), {

                allowDragAndDrop: true,

                allowDragAndDropAccessControl: true,

                allowDropSibling: true, // allows to drop sibling

                allowDropChild: true, // allows to drop as child

                fields: { dataSource: tree1, id: "id", parentId: "parent", text: "text" }

            });
       var tree = new ej.TreeView($("#treeViewDrop"), {
                allowDragAndDrop: true,

                allowDragAndDropAccessControl: true,

                allowDropSibling: true, // allows to drop sibling

                allowDropChild: true, // allows to drop as child

                fields: { dataSource: tree2, id: "id", parentId: "parent", text: "text" }

            });

        });
    }

{% endhighlight %}

For more details about drag and drop between TreeView, refer the sample [here](http://jsplayground.syncfusion.com/40z0fek2#). 

## Auto Node Structuring

You may not need to have two TreeView to be in same structured node while drag and drop the nodes between them. But after the node has been dropped, it should get structure of the TreeView node in which dropped. By default TreeView auto structure the node whenever you drop a node from different tree.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

        var tree1 = [

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

        var tree2 = [

        { id: 11, text: "Item 5" },

        { id: 12, text: "Item 6" },

        { id: 13, text: "Item 7" },

        { id: 14, text: "Item 4" },

        { id: 15, parent: 11, text: "Item 5.1" },

        { id: 16, parent: 11, text: "Item 5.2" },

        { id: 17, parent: 11, text: "Item 5.3" },

        { id: 18, parent: 13, text: "Item 7.1" },

        { id: 19, parent: 13, text: "Item 7.2" },

        { id: 10, parent: 15, text: "Item 5.1.1" }

        ];

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeViewDrag").ejTreeView({

                allowDragAndDrop: true,

                allowDragAndDropAccessControl: true,

                allowDropSibling: true, // allows to drop sibling

                allowDropChild: true, // allows to drop as child

                fields: { dataSource: tree1, id: "id", parentId: "parent", text: "text" },

                showCheckbox: true

            });

            $("#treeViewDrop").ejTreeView({

                allowDragAndDrop: true,

                allowDragAndDropAccessControl: true,

                allowDropSibling: true, // allows to drop sibling

                allowDropChild: true, // allows to drop as child

                fields: { dataSource: tree2, id: "id", parentId: "parent", text: "text" }

            });

        });
}

{% endhighlight %}

For more details about drag and drop between TreeView, refer the sample [here](http://jsplayground.syncfusion.com/u0vqjm0e#). 

N>  Auto node structure applicable for well-structured node object.

