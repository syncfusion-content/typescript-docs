---
layout: post
title: Tree-Node
description: tree node
platform: Typescript
control: TreeView
documentation: ug
---

# Tree Node

TreeView node is structured with expand/collapse arrow, checkbox, image and text as shown in below.

![](/js/TreeView/Tree-Node_images/Tree-Node_img1.png)


Also TreeView node object holds the following properties.

<table>
<tr>
<th>
Properties</th><th>
Data Type</th><th>
Description</th></tr>
<tr>
<td>
checked <br/><br/></td><td>
Boolean<br/><br/></td><td>
Checked state of the node<br/><br/></td></tr>
<tr>
<td>
count<br/><br/></td><td>
Number<br/><br/></td><td>
Number of child<br/><br/></td></tr>
<tr>
<td>
expanded<br/><br/></td><td>
Boolean<br/><br/></td><td>
Expanded state of the node<br/><br/></td></tr>
<tr>
<td>
index<br/><br/></td><td>
Number<br/><br/></td><td>
Index of the node <br/><br/></td></tr>
<tr>
<td>
level<br/><br/></td><td>
Number<br/><br/></td><td>
Level of the node<br/><br/></td></tr>
<tr>
<td>
id<br/><br/></td><td>
String<br/><br/></td><td>
Node id<br/><br/></td></tr>
<tr>
<td>
parentId<br/><br/></td><td>
String<br/><br/></td><td>
Parent id of the node<br/><br/></td></tr>
<tr>
<td>
selected<br/><br/></td><td>
Boolean<br/><br/></td><td>
Selected state of the node<br/><br/></td></tr>
</table>


## Get/Set Node Value

TreeView provides a set of options to configure all its properties by setting and getting values at initialization or dynamically.

To get the node value, you can use [getNode](https://help.syncfusion.com/api/js/ejtreeview#methods:getnode) method as shown in the below code example, in which on button click action the node value has retrieved.
Also you can get the text value of tree node by using [getText](https://help.syncfusion.com/api/js/ejtreeview#methods:gettext) method.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                fields: {
                    dataSource: [

                    {

                        id: 1, text: "Item 1",

                        child: [

                        { id: 4, text: "Item 1.1" },

                        { id: 5, text: "Item 1.2" }

                        ]

                    },

                    { id: 2, text: "Item 2" },

                    { id: 3, text: "Item 3" }

                    ]

                }

            });

        });
  }

        //bind below onClick action to button to get node at button click or else in any action

        function onClick() {
            var node = tree.getNode("1");

        }

{% endhighlight %}

N>  Existing TreeView instance can be created by [jQuery.data()](http://api.jquery.com/jQuery.data/#) and you can control the API’s of TreeView behavior.

To edit the node text, you can use [updateText](https://help.syncfusion.com/api/js/ejtreeview#methods:updatetext) method as shown below code example. 

{% highlight js %}

        //get node object using getNode method

        var node = tree.getNode("2");

        //sets text to existing node 

        tree.updateText(node.id, "updated Item");

{% endhighlight %}

## Get Parent Node

To get current parent node of a particular node, you can use the [getParent](https://help.syncfusion.com/api/js/ejtreeview#methods:getparent) method as shown in below code example 

{% highlight js %}


        //create an instance from an existing TreeView.

        // only after control creation we can get treeObj otherwise it throws exception.

        var node = tree.getParent("4");

{% endhighlight %}

## Get Node Index

To get node index you can use the [getNodeIndex](https://help.syncfusion.com/api/js/ejtreeview#methods:getnodeindex) as shown in below code example

You can use [getNodeByIndex](https://help.syncfusion.com/api/js/ejtreeview#methods:getnodebyindex) method to get TreeView node by using index position.

{% highlight js %}

        //create an instance from an existing TreeView.

        var node = tree.getNode("4");

        //gets the index of node 

        tree.getNodeIndex(node.id);

{% endhighlight %}

## Node Manipulations

You can perform following operation in tree nodes and the modified node values can be saved in database.

### Add or Remove nodes

To add/remove nodes programmatically, use [addNode](https://help.syncfusion.com/api/js/ejtreeview#methods:addnode) and [removeNode](https://help.syncfusion.com/api/js/ejtreeview#methods:removenode) methods of the TreeView.

{% highlight js %}

        //create an instance from an existing TreeView.

        tree.addNode(newNode, "2");

        //to remove node

        tree.removeNode("4");

{% endhighlight %}

You can able to add a new node after or before specific TreeView node by using [insertAfter](https://help.syncfusion.com/api/js/ejtreeview#methods:insertafter) and [insertBefore](https://help.syncfusion.com/api/js/ejtreeview#methods:insertbefore) methods.

{% highlight js %}

        //create an instance from an existing TreeView.

        var newNode = { id: 12, text: "Item 2.2" };

        //to add tree node after some element, which having id 2

        tree.insertAfter(newNode, "2");

        var newNode = { id: 13, text: "Item 2.3" };

        //to add tree node before some element, which having id 2

        tree.insertBefore(newNode, "2");

{% endhighlight %}

### Move node

You can also achieve cut and paste operation by using [moveNode](https://help.syncfusion.com/api/js/ejtreeview#methods:movenode) methods.

{% highlight js %}

        //create an instance from an existing TreeView.

        //to move tree node which having id 5, to child of node which having id 2.

        tree.moveNode("5", "2");

{% endhighlight %}

### Expand or Collapse node

Tree nodes can be expanded or collapsed by clicking the expand/collapse icon of the node or in code behind by using the following methods.

<table>
<tr>
<th>
Methods</th><th>
Description</th></tr>
<tr>
<td>
{{'[expandNode](https://help.syncfusion.com/api/js/ejtreeview#methods:expandnode)'| markdownify }} <br/><br/></td><td>
Expands the node with specified id<br/><br/></td></tr>
<tr>
<td>
{{'[collapseNode](https://help.syncfusion.com/api/js/ejtreeview#methods:collapsenode)'| markdownify }}<br/><br/></td><td>
Collapse the node with specified id <br/><br/></td></tr>
<tr>
<td>
{{'[expandAll](https://help.syncfusion.com/api/js/ejtreeview#methods:expandall)'| markdownify }}<br/><br/></td><td>
Expands all the node<br/><br/></td></tr>
<tr>
<td>
{{'[collapseAll](https://help.syncfusion.com/api/js/ejtreeview#methods:collapseall)'| markdownify }}<br/><br/></td><td>
Collapse all the node<br/><br/></td></tr>
</table>
Also you can get all the expanded nodes index in tree by using [getExpandedNodesIndex](https://help.syncfusion.com/api/js/ejtreeview#methods:getexpandednodesindex) method, which returns the array of expanded node indices. 

### Prevent multiple node expand

You can able to prevent multiple expand of TreeView nodes by specifying [enableMultipleExpand](https://help.syncfusion.com/api/js/ejtreeview#members:enablemultipleexpand) as false.

For example, if you want to allow only one node to be expanded in TreeView at a time. Refer the sample [here](http://jsplayground.syncfusion.com/zdtud5yw#).

{% highlight js %}

        // Initialize and bind the TreeView with enableMultipleExpand property

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                enableMultipleExpand: false,

                dataSource: localData,

                fields: {

                    id: "id",

                    text: "text",

                    parentId: "parent"

                }

            });

        });
}

{% endhighlight %}

### Get updated node collection

You can get the updated node values after manipulating or editing the node of TreeView to save at server end using [getTreeData](https://help.syncfusion.com/api/js/ejtreeview#methods:gettreedata) method. It returns the JSON data represented as in tree with modified structure.

You can also get the updated data source for remote data binding after performing the operation like editing, selecting/unselecting, expanding/collapsing, checking/unchecking and removing node. You cannot get the updated data source when you perform operation like drag and drop, adding node for remote data binding.

The updated data source also contains custom attributes if you return these from server.

{% highlight js %}

        //create an instance from an existing TreeView.

        //to get TreeView data

        tree.getTreeData();

{% endhighlight %}

## Editing

You can directly edit the tree node’s text in-place by double-click on the tree node or select the tree node and press F2 key. The editing works only if the [allowEditing](https://help.syncfusion.com/api/js/ejtreeview#members:allowediting) property is true in TreeView control. When editing is completed by focus out or “enter” key press, the modified node’s text is saved automatically. The [nodeEdit](https://help.syncfusion.com/api/js/ejtreeview#events:nodeedit) event will be triggered whenever edited the TreeView node.
Also [beforeEdit](https://help.syncfusion.com/api/js/ejtreeview#events:beforeedit) event will be triggered before the TreeView node change into editing mode.

{% highlight js %}

        // Initialize and bind the TreeView with allowEditing property

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

    $(function () {

        var tree = new ej.TreeView($("#treeView"), {

                allowEditing: true,

                dataSource: localData,

                fields: {

                    id: "id",

                    text: "text",

                    parentId: "parent"

                }

            });

        });
 }

{% endhighlight %}

## Selection

You can select a specific node by setting index value in [selectedNode](https://help.syncfusion.com/api/js/ejtreeview#members:selectednode) property or passing node’s id/element to [selectNode](https://help.syncfusion.com/api/js/ejtreeview#methods:selectnode) method.
To get the selected status of a given TreeView node you have to use [isSelected](https://help.syncfusion.com/api/js/ejtreeview#methods:isselected) method.  
The [nodeClick](https://help.syncfusion.com/api/js/ejtreeview#events:nodeclick) event will be triggered whenever TreeView node is clicked. The [beforeSelect](https://help.syncfusion.com/api/js/ejtreeview#events:beforeselect) event will be triggered before the TreeView node is selected. 
The [nodeSelect](https://help.syncfusion.com/api/js/ejtreeview#events:nodeselect)/[nodeUnselect](https://help.syncfusion.com/api/js/ejtreeview#events:nodeunselect) events will be triggered based on the TreeView node click operations. 

{% highlight js %}

        // Initialize and bind the TreeView with selectedNode property

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                selectedNode: 2,

                dataSource: localData,

                fields: {

                    id: "id",

                    text: "text",

                    parentId: "parent"

                }

            });

            //create an instance from an existing TreeView.

              //to select node

            tree.selectNode("4");

        });
}

{% endhighlight %}

## Ensure Visibility

To get the visibility status of the given TreeView node, you can use [isVisible](https://help.syncfusion.com/api/js/ejtreeview#methods:isvisible) method.
You can ensure the specified tree node is visible by using [ensureVisible](https://help.syncfusion.com/api/js/ejtreeview#methods:ensurevisible) method, which expands tree nodes and scrolls the TreeView control as necessary.
Also you can use [getVisibleNodes](https://help.syncfusion.com/api/js/ejtreeview#methods:getvisiblenodes) method to get currently visible nodes in TreeView.

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

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });
}

        function onClick() {

            //create an instance from an existing TreeView.

            tree.ensureVisible("10");

        }

{% endhighlight %}

