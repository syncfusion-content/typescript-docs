---
layout: post
title: Checkboxes
description: checkboxes
platform: Typescript
control: TreeView
documentation: ug
---

# Checkboxes

TreeView consists of in-build checkbox option and it can be displayed to the left of the tree node by setting the [showCheckbox](https://help.syncfusion.com/api/js/ejtreeview#members:showcheckbox) property as true. It allows you to select more than one node at a time. 

## Indeterminate Checkboxes

TreeView supports tristate checkboxes in addition with standard two state checkboxes. By default TreeView has been enabled with tristate in checkboxes. You can enable 2-state checkboxes by using [autoCheckParentNode](https://help.syncfusion.com/api/js/ejtreeview#members:autocheckparentnode) as false.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
 

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                showCheckbox: true, // shows each node with checkboxes

                autoCheckParentNode: false,// enable 2-state checkboxes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });
}  

{% endhighlight %}

## Auto Checkable

By default checkbox state of child nodes depends up on parent node checkbox state and also parent node state gets updated based on child nodes state. You can turn off this option by setting [autoCheck](https://help.syncfusion.com/api/js/ejtreeview#members:autocheck) as false to make independent parent and child nodes checkboxes.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                showCheckbox: true, // shows each node with checkboxes

                autoCheck: false,// turns off auto check of parent and child nodes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });
    }

{% endhighlight %}

## Check or Uncheck Node

Tree node can be checked or unchecked using [checkNode](https://help.syncfusion.com/api/js/ejtreeview#methods:checknode) and [uncheckNode](https://help.syncfusion.com/api/js/ejtreeview#methods:unchecknode) methods while [showCheckbox](https://help.syncfusion.com/api/js/ejtreeview#members:showcheckbox) property is enabled in TreeView. Also you can get or set the checked nodes of TreeView using [checkedNodes](https://help.syncfusion.com/api/js/ejtreeview#members:checkednodes) property, which indicates the checked nodes index collection as array. The [nodeCheck](https://help.syncfusion.com/api/js/ejtreeview#events:nodecheck) and [nodeUncheck](https://help.syncfusion.com/api/js/ejtreeview#events:nodeuncheck) event occurs based on checkbox state.
You can use [isNodeChecked](https://help.syncfusion.com/api/js/ejtreeview#methods:isnodechecked) method to check the particular TreeView node is checked or unchecked. Also you can use [checkAll](https://help.syncfusion.com/api/js/ejtreeview#methods:checkall) method to check all the nodes in TreeView.

{% highlight js %}


        //to check node

        tree.checkNode("2");

        //to uncheck node

        tree.uncheckNode("2");

{% endhighlight %}


## Get Checked Nodes

To get checked nodes of TreeView, you can use [getCheckedNodes](https://help.syncfusion.com/api/js/ejtreeview#methods:getcheckednodes) method. It returns the collection of tree node.
Also you can get currently checked nodes indexes in TreeView by using [getCheckedNodesIndex](https://help.syncfusion.com/api/js/ejtreeview#methods:getcheckednodesindex) method.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {

                showCheckbox: true, // shows each node with checkboxes

                autoCheck: false,// turns off auto check of parent and child nodes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });
 }

        function onClick() {

            //to get checked nodes

            tree.getCheckedNodes();

        }

{% endhighlight %}

