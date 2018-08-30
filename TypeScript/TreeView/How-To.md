---
layout: post
title: How-To
description: how to
platform: Typescript
control: TreeView
documentation: ug
---


# How To

## Update the modified data from tree to database

TreeView allow you to get the updated tree data after performing such operation like node editing, drag and drop, add and remove node. Using [getTreeData](https://help.syncfusion.com/api/js/ejtreeview#methods:gettreedata) method you can get the updated tree data. 

Refer the sample from the link [Updated tree data](http://jsplayground.syncfusion.com/3f1qqqm1#) to know how to get updated data from TreeView.

You can also get the updated data source for remote data binding after performing the operation like editing, selecting/unselecting, expanding/collapsing, checking/unchecking and removing node. You cannot get the updated data source when you perform operation like drag and drop, adding node for remote data binding.

The updated data source also contains custom attributes ("ContactTitle", "OrderID", "EmployeeID", "Freight") if you return these from server.

Refer the sample from the [link](http://jsplayground.syncfusion.com/Sync_aeirbejs) to know more about how to get updated data with custom attributes from TreeView for remote data binding.

## TreeView context menu to process node operations

TreeView allow you to perform some tree operation like add, remove, update, move, check, uncheck, select node dynamically by using built-in methods and properties. Using those methods and properties, you can trigger it through context menu item click action to manipulate node. 

Refer the sample from the link [TreeContextMenu](http://jsplayground.syncfusion.com/paehr5xx#) to know how to use context menu to perform tree operations. 

## Sorted data using refresh method

TreeView allow you to refresh the entire tree data by using [refresh](https://help.syncfusion.com/api/js/ejtreeview#methods:refresh) method. Refer the sample from the link [Sorted tree data](http://jsplayground.syncfusion.com/ded1kjs4#) to know how to update entire tree data.

## Persist updated data after edit, add and remove node

TreeView allow you to persist the updated data after performing node manipulation. By using persistence option, you can sustain on page refresh.

The [nodeAdd](https://help.syncfusion.com/api/js/ejtreeview#events:nodeadd), [nodeCut](https://help.syncfusion.com/api/js/ejtreeview#events:nodecut), [nodeDelete](https://help.syncfusion.com/api/js/ejtreeview#events:nodedelete) and [nodePaste](https://help.syncfusion.com/api/js/ejtreeview#events:nodepaste) events occurs based on Treeview node manipulation. The [beforeAdd](https://help.syncfusion.com/api/js/ejtreeview#events:beforeadd), 
[beforeCut](https://help.syncfusion.com/api/js/ejtreeview#events:beforecut), [beforeDelete](https://help.syncfusion.com/api/js/ejtreeview#events:beforedelete) and [beforePaste](https://help.syncfusion.com/api/js/ejtreeview#events:beforepaste) events are triggered before the TreeView component node manipulation.

Refer the sample from the link [PersistData](http://jsplayground.syncfusion.com/szaem5fo#) to know how to persist updated tree data after refresh.

## Filtering nodes in TreeView

You can able to filter TreeView nodes based on node text. Refer the sample from the link [FilterTreeNodes](http://jsplayground.syncfusion.com/vbxs3mi0#) to know how to filter tree nodes based on the node text.

## AngularJS data binding to update data while add and remove node

TreeView allow you to bind and update tree data in mapped data component while add and removing node using AngularJS binding. Refer the sample from the link [AngularDataBinding](http://jsplayground.syncfusion.com/vcxy2cke#) to know how to update data using AngularJS binding.

## Set Tooltip for TreeView nodes

TreeView allow you to set tooltip option to TreeView nodes by using [fields.linkAttribute](https://help.syncfusion.com/api/js/ejtreeview#members:fields-linkattribute) property of TreeView. Refer the sample from the link [Tooltip](http://jsplayground.syncfusion.com/nbdo3l5g#) to know how to set tooltip for TreeView nodes.

## Auto hide/show the expand/collapse icon of TreeView

You can able to display expand icon on mouse entering into TreeView and hide while leaving from the TreeView. Refer the sample [AutoHide](http://jsplayground.syncfusion.com/wrm34bii#) to know how to hide/show the expand/collapse icons automatically based on mouse position.

## Customize the expand/collapse icons of TreeView

You can able to customize the TreeView expand and collapse icon by using “cssClass” property of TreeView. Refer the sample [CustomizeIcons](http://jsplayground.syncfusion.com/jeqtepz0#) to know how to customize the expand/collapse icons.

