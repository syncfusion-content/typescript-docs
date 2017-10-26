---
layout: post
title: Multiple-Drag-and-Drop
description: multiple drag and drop
platform: Typescript
control: TreeView
documentation: ug
---


# Drag and Drop Multiple Nodes

TreeView supports to drag and drop multiple nodes by specifying [allowMultiSelection](https://help.syncfusion.com/api/js/ejtreeview#members:allowmultiselection) as true along with [allowDragAndDrop](https://help.syncfusion.com/api/js/ejtreeview#members:allowdraganddrop) as true. It allows you to drag and drop multiple nodes in TreeView.

{% highlight html %}

	<!--create the TreeView wrapper-->
	<table>
		<tr>
			<td>
				<div id="treeViewDrag"></div>
			</td>
			<td>
				<div id="treeViewDrop"></div>
			</td>
		</tr>
	</table>

{% endhighlight %}

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
	
			allowMultiSelection: true,
	
			allowDragAndDrop: true,
	
			fields: { dataSource: tree1, id: "id", parentId: "parent", text: "text" },
	
		});
	var tree1 = new ej.TreeView($("#treeViewDrop"), {

			allowMultiSelection: true,
	
			allowDragAndDrop: true,
	
			fields: { dataSource: tree2, id: "id", parentId: "parent", text: "text" }
	
		});
	
	}); 
}

{% endhighlight %}

For more details about multiple drag and drop in TreeView, refer the sample [here](http://jsplayground.syncfusion.com/Sync_1mo2awgk).